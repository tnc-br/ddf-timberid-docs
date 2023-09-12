# 🖥 Analytics

### Cloud functions

Cloud functions will be used to give members and admins their permissions once they have been approved.&#x20;

User journeys\


| User journey                                | Database change                                                                                                          | Cloud function                                                                                                                                                                                                         |
| ------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Org admin approves new membership           | New member is added to the organzations DB including their information                                                   | <p>When an organization's document is updated, the cloud function determines what was changed. It will find the new user and update their token values: </p><ul><li>Role: member</li><li>Org: &#x3C;org_id> </li></ul> |
| Site admin approves new organization        | New org is added to the organization database with the user who proposed the organization as the only member and admin.  | <p>Cloud function triggered when a new document is created in the Organizations collection. It will update the new admin’s auth tokens:</p><ul><li>Role: admin</li><li>Org: &#x3C;org_id></li></ul>                    |
| Site admin approves new site admin          | New site admin ID is added to the site\_admin collection                                                                 | <p>Cloud function triggered when a new document is added to the site_admin collection. It will update the new site admins auth tokens:</p><ul><li>Role: site_admin</li><li>Org: &#x3C;unchanged></li></ul>             |
| Site admin removes member from organization | Member is removed from member list in the document corresponding to that organization in the organizations collection    | <p>Cloud function triggered with the organization's document is updated. Old members auth tokens are updated:</p><ul><li>Role: &#x3C;></li><li>Org: &#x3C;></li></ul>                                                  |
