# PureOrigin.API - C# Origin Launcher API
A .NET API Wrapper for the Origin Launcher API
Documentation is found below!

## Installation
Our stable build is available from NuGet through the ApexAPI metapackage:
- [PureOrigin.API](https://www.nuget.org/packages/PureOrigin.API/)

## Getting Started
Once you have added the NuGet Package to your Project, you will need to add the `using PureOrigin.API;` to your class header.
Then simply instance the OriginAPI class with your Origin Email and Password, like so:
```csharp
var API = new OriginAPI("example@email.com", "password");
```
Now you can easily make calls to the API.

## GetUserAsync()
If you already know a user's Guid or Username, you can use the `GetUserAsync()` method to return an `OriginUser` object.
- Username:
```csharp
var user = API.GetUserAsync("username");
```

## GetUsersAsync()
Same as `GetUserAsync()` but allows to search by generic terms.
- This will return any users who's username starts with `user`:
```csharp
var users = API.GetUsersAsync("user");
```
  
## GetAvatarUrlAsync()
If you're wanting to get a user's avatar, you can simply use `.GetAvatarUrlAsync();` and it will return said avatar's url.
```csharp
var user = API.GetUserAsync("username");
var url = await user.GetAvatarUrlAsync();
```

Thanks for using my wrapper <3 By Kanga#8041
