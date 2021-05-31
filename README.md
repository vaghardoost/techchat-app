# Techchat Application

Techchat is an application show a json datapack as android views
In Techchat App There is Only Services And a service is context of datapack to convert to views
### What Is Service?
service is an account in techchat and a script or code can work on it. service with id and token do login and received and send data to application users(here app called client) 
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
- <a href="https://github.com/vaghardoost/techchat-app/wiki/Datapack#caption">caption</a>
- <a href="https://github.com/vaghardoost/techchat-app/wiki/Datapack#hs-caption">photo</a>
- <a href="https://github.com/vaghardoost/techchat-app/wiki/Datapack#photo">hs-caption</a>
- <a href="https://github.com/vaghardoost/techchat-app/wiki/Datapack#hs-photp-caption">hs-photo-caption</a>
- <a href="https://github.com/vaghardoost/techchat-app/wiki/Datapack#photo-caption-lg">photo-caption-lg</a>
- <a href="https://github.com/vaghardoost/techchat-app/wiki/Datapack#photo-caption-sm">photo-caption-sm</a>
- <a href="https://github.com/vaghardoost/techchat-app/wiki/Datapack#slider">slider</a>
- <a href="https://github.com/vaghardoost/techchat-app/wiki/Datapack#pro-caption">pro-caption</a>
- <a href="https://github.com/vaghardoost/techchat-app/wiki/Datapack#pro-caption">audio</a>
- <a href="https://github.com/vaghardoost/techchat-app/wiki/Datapack#pro-caption">pairwise-photo-caption</a>
> the meaning of "hs" is **horizontal scroll**

> each of thease content have schema and rules

#### Now For Example A ***"Hello World"*** datapack is like this

if you send this for a client

```
{
  "id":"hello world",
  "content":[
    {
      "caption":{
        "text":"hello world"
      }
    }
  ]
}
```

client see that

<img src="https://github.com/vaghardoost/techchat-app/blob/main/hello%20world.jpg" width="240" height="520"/>

and if you append another content item on datapack thease contents converted to views and append to scroll view of content

techchat has many options:
- Forward clients messages from one service to another as Redirection
- Security encryption
- Service manage panel with login
- Datapack schema
- Service and Server Message exchanges

<a href="https://github.com/vaghardoost/techchat-app/blob/main/Techchat.apk">apk file of application</a>

read <a href="https://github.com/vaghardoost/techchat-app/wiki">techchat wiki</a> to learn more
