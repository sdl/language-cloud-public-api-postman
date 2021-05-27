# Language Cloud APIs for Postman

We provide a [Postman](https://www.postman.com/) collection for quick and easy usage of our RESTful APIs.

## Installation

You can download the Postman collection from [here](https://github.com/sdl/language-cloud-public-api-postman/blob/develop/postmanCollection.json?raw=true).

You have 3 options:
* Copy the collection URL from above and import it into Postman using `Import > Link`.
* Copy the entire file content and import it into Postman using `Import > Raw Text`.
* Save it as a `JSON` file on your computer and import it into Postman using `Import > File`.

![image](https://user-images.githubusercontent.com/10993097/118100979-c343a000-b3df-11eb-9a1c-e404f662b269.png)

## Configuration

The imported collection is already set up for you to get started as fast as possible. 

We make use of collection level variables and an inherited authentication mechanism.

For example, authentication is already set up to use the Bearer Token scheme and will use the token value provided by `{{lc-access-token}}` variable. This token is populated with the correct value, each time you `Obtain a client credentials access token`, via the Tests tab.

One thing you need to do before proceeding is to fill in the `{{lc_tenant}}` variable with your own tenant id. Prepend the id with LC- so the final value looks like this `LC-00000000000000000`.

Don't forget to save the collection!

![image](https://user-images.githubusercontent.com/10993097/118111273-250a0700-b3ec-11eb-910b-23cfd490695a.png)


### Authentication
To start working with the Language Cloud API, you first need to authenticate. 

You can find the authentication call under the `Authorization (Start Here)` folder. Fill in your `client_id` and `client_secret` and perform the request.

If the authentication is successful, the token will be extracted automatically from the response and saved to the `{{lc-access-token}}` variable.

![image](https://user-images.githubusercontent.com/10993097/118103532-b1173100-b3e2-11eb-97c0-92df2f3794ec.png)

### Usage

After you have authenticated successfully, you can start interacting with the Language Cloud API.

For example, we can get information about a project by using the **GetProject** request from the **Project** folder.

Simply fill in your `projectId` and click SEND. Optionally, you can supply values to the `fields` parameter to receieve only data that is of interest.

`IMPORTANT: make sure you are not sending any query parameters with default Postman values. If you are sending any parameters, make sure you are sending valid data or else you will get an API Error.`

![image](https://user-images.githubusercontent.com/10993097/119813507-09295980-bef2-11eb-970e-42119cf4ffd8.png)

![image](https://user-images.githubusercontent.com/10993097/118110695-68b04100-b3eb-11eb-8356-5bd6e21185c8.png)


