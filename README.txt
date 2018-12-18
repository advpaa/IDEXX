Hello and thank you for reading this.

Here couple of my comments:

1. I added the config for server address to won't repeat it every time - it makes the test better to support.

2. Dependencies:
 - site can be reached (no deployments at the time of test);
 - all users and data should exist to the moment of test and be the same as they hard-coded in the script (there are no extractors for links);
- because the script follows step-by-step schema, cookies are stored from the login through other steps (dependency on authorization).

3. From the very begging, jmeter needs installation of Plugins manager.
User needs to add Custom Thread Groups plugin from it to add Concurrency Thread Group.

4. Just in case: code assertions will help, but even i got the page with 200 ok, sometime it was a page with the error in the response body.

5. I wasn't sure what was 'check that user was created' in Step 6 - i just added assertion on the text on the home page that contains user's surname.

6. To prove that the script had no errors, i switched the thread to load for seconds instead minutes and you can find the report in the file folder.
