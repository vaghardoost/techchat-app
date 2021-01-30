# Techchat Application

Techchat is an application show a json datapack as android views
In Techchat App There is Only Services And a service is context of datapack to convert to views
### What Is Service?
service is a account in techchat and a acript or code can work on it. service with id and token do login and received and send data to application users(here app called client) 
### How To Transfare Data between Service and Client?
for use a service a script or a code should connect to server. Techchat use *socket.io* to transfer data and if you have a service account inside of techchat server , your code can login your service by id and token (here called start service) and then every client send a message to your service redirects to your code and your code can make a json datapack and send to client.

### What Is The "JSON Datapack"?
JSON Datapack is a JsonSchema and have rules to make as view. If you know about JsonSchema go here and see techchat datapack json schema.
A datapack contains 4 part:
-	id: name or identify of datapack used for client witch see datapack when send a message 
-	Enviroment: background image or color
-	Input: Keyboard or custom button to send any message
-	content: views shows scrolled
> in a datapack environment (here is env) and input are optional

most impotant part of datapack is content because datapack any content is a view to show
for first version of techchat we have 8 type content
- caption
- photo
- hs-caption
- hs-photo-caption
- photo-caption-lg
- photo-caption-sm
- slider
- procaption
> the meaning of "hs" is **horizontal scroll**

> each of thease content have schema and rules

#### Now For Example A ***"Hello World"*** datapack is like this

if you send this for a client

```
{
  "id":"hello world",
  "content":[
    {
      "caption":"hello world"
    }
  ]
}
```

client see that

<img src="https://github.com/vaghardoost/techchat-app/blob/main/hello%20world.jpg" width="240" height="520"/>

and if you append another content item on datapack thease contents converted to views and append to scroll view of content

techchat has a lot of rules

- Forward clients messages from one service to another as Redirection
- Security encryption
- Service manage panel with login
- Datapack schema
- Service and Server Message exchanges

application uploaded soon
