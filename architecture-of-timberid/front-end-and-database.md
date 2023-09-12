# ♒ Front End and Database

### FrontEnd design



### Database design&#x20;

The database is a [Cloud Firestore](https://firebase.google.com/docs/firestore) Database. Cloud Firestore is a flexible, scalable NoSQL cloud database. It leverages Firebase Authentication to eliminate a middle tier and allow secure direct read/writes from the front end.

The development database can be found [here](https://console.cloud.google.com/firestore/databases/-default-/data/query;collection=%2Fnew\_users?authuser=0\&project=river-sky-386919). The production database can be found [here](https://console.cloud.google.com/firestore/databases/-default-/data/query;collection=%2Fnew\_users?authuser=0\&project=timberid-prd).

The schema of the database is below.

| Document Collection  | Data                                                                                                                                                                                                                                                        | Visibility                                                                                                                                                                           |
| -------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| verified\_samples    | All data for a particular trusted sample including metadata like site of collection, and user who entered the sample, as well as the results.                                                                                                               | By default, only visible to the organization that entered the sample. Organization admin can choose to make it public.                                                               |
| unverified\_samples  | All data for a particular unverified sample with the same metadata as verified\_samples                                                                                                                                                                     | Same visibility as verified\_samples. The organization admin can make samples public                                                                                                 |
| new\_users           | <p>All data a new user enters when signing up for an account: </p><ul><li>Name</li><li>Email</li><li>Organization to join or name of new organization they are proposing is created </li><li>Date of account creation</li></ul>                             | New user data is only visible to the admins of the organization they are trying to join. If they are trying to create a new organization, that data is only visible by a site admin. |
| organizations        | Contains a list of documents with keys corresponding to each organization ID. Each document contains the members in the organization and their data (name, email, date joined), the org admins and their data (name, email, date joined), and the org name  | Each organization's data is only visible to the org admins and only an org’s admin can edit the org name, members or admins.                                                         |
| site\_admins         | A list of the site admins.                                                                                                                                                                                                                                  | Only visible and editable by site admins.                                                                                                                                            |

\
