import { Client, Vcs } from "@appwrite.io/console";

const client = new Client();

const vcs = new Vcs(client);

client
    .setEndpoint('https://cloud.appwrite.io/v1') // Your API Endpoint
;

const promise = vcs.createRepository('[INSTALLATION_ID]', '[NAME]', false);

promise.then(function (response) {
    console.log(response); // Success
}, function (error) {
    console.log(error); // Failure
});