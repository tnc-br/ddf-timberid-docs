# ♒ Client

## FrontEnd design

The Client consists of the Front End, which is written in Typescript and hosted using [Firebase Hosting](https://firebase.google.com/docs/hosting). This is a Firebase web application and directly reads and writes to the underlying backend [Firestore](https://firebase.google.com/docs/firestore).

The client surfaces the following functionality

1. LogIn/Signup with Password Reset
2. Viewing existing Samples (inprogress/completed and reference/untrusted)
3. Add or Edit Samples
4. Importing Samples
5. Viewing Sample Status and Analysis

### Login, Signup and Password Reset

TimberID uses built in Firebase functionality to sign up with Google or email/password.



{% @github-files/github-code-block url="https://github.com/tnc-br/ddf-sample-tracking/blob/653e92a308c2c4f5eee12354f46df64e7dfe7db5/sample_tracking/app/login/login.tsx#L36-L42" %}
