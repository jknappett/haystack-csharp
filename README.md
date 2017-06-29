# README #

### What is this repository for? ###

Connecting to Haystack 3.0 via SCRAM mechanism.

### How do I get set up? ###

Below is the main method found in HClient.cs. HClient is a very basic implementation and contains methods to create clients, get strings, and post strings. To use this you must pass in the uri, user, and pass as arguments when running the program. In the main method you can also see an example of the GetString method to get the information about the current client.
    
```
#!c#
public static void Main(string[] args)
{
  try
  {
    if (args.Length != 3)
    {
      Console.WriteLine("usage: HClient <uri> <user> <pass>");
      Environment.Exit(0);
    }

    HClient client = MakeClient(args[0], args[1], args[2]);
    Console.WriteLine(client.GetString("about", new Dictionary<string, string>(), "text/zinc"));
    Console.ReadKey();
  }
  catch (Exception e)
  {
    throw e;
  }
}
```


### Contribution guidelines ###

* Writing tests
* Code review
* Other guidelines

### Who do I talk to? ###

* Repo owner or admin
* Other community or team contact