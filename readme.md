# Kpakpato-api #

The primary goal of this project is to make it easier to build applications that use sms api technologies.

## Features ##

* Implementation for accessing the [orange ci sms api](http://help.github.com/forking/).


## Quick Start ##

Download the jar though Maven:

```xml

<repositories>
        <repository>
            <id>kpakpato-build</id>
            <name>kpakpato builds</name>
            <url>https://oss.sonatype.org/content/groups/public</url>
        </repository>
</repositories>

<dependency>
  <groupId>com.centonni</groupId>
  <artifactId>kpakpato-api</artifactId>
  <version>1.0-SNAPSHOT</version>
</dependency>
```
```java
public class TestKpakpato {

  public static void main(String[] args) throws Exception {
    //create an instance of the orange api with your credentials
        SmsAPI ssapi=new OrangeSmsAPI("your_client_id", "your_client_secret");
    //you can retrieve your authentication token
        AuthenticationToken token = ssapi.getToken();

        System.out.println("**** "+token);
  //Create a message context that will be used to send your sms
        MessageContext context=new MessageContext("tel:+225senderAddress", "senderName", "your message here");
  //send a sms to your receiver
        ssapi.sendSms(context, "tel:+225receiverAdress");

    }
}
```

## Contributing to Kpakpato-api ##

Here are some ways for you to get involved  :

* Create github tickets for bugs and new features and comment and vote on the ones that you are interested in.  
* Github is for social coding: if you want to write code, we encourage contributions through pull requests from [forks of this repository](http://help.github.com/forking/). If you want to contribute code this way, please reference a github ticket as well covering the specific issue you are addressing.
* Watch for upcoming articles on kpakpato-api by [subscribing](http://centonni.com) to my blog.
