# Bookmarks app #

=================

<center>

![InventiveOnes Logo][IO-Logo]

| Product | Version | Last update |             Author |
|---------|:-------:|:-----------:|-------------------:|
| `ownCloud Bookmarks` | **0.1.0** |  19/02/2017 | [Lavysh Alexander] |

</center>

## Developer setup info ##

--------------------------

1. Just clone this repo into one of your apps directory.
2. Done!)


## Status ##

------------

From original repository:

> Rewrite by [Stefan Klemm] aka ganomi (https://github.com/ganomi)
> 
> * This is a refactored / rewritten version of the bookmarks app using the app framework
> * Dependency Injection for user and db is used througout the controllers
> * The Routing features a consistent rest api
> * The Routing provides some legacy routes, so that for exampe the Android Bookmarks App still works.
> * Merged all the changes from https://github.com/owncloud/bookmarks/pull/68 and added visual fixes. App uses the App Framework Styling on the Client side now.
> 
> There is a publicly available api that provides access to bookmarks per user. (This is usefull in connection with the Wordpress Plugin https://github.com/mario-nolte/oc2wp-bookmarks)


## Public Rest Api (JSON Formatting) ##

---------

Example Url:

```
../apps/bookmarks/public/rest/v1/bookmark?user=username&password=password&tags[]=firsttag&tags[]=anothertag&select[]=description&conjunction=AND&sortby=description
```

### Parameters ###

* user is a mandatory parameter. This will return all bookmarks from the specific user marked as public. (not yet possible!)
* by providing the users password all bookmarks will be returned
* tags[] can take multiple arguments and they are used to filter the requested bookmarks by tags
* conjunction (default = or) sets the tag filter to OR or to AND
* select[] takes multiple arguments. By default only url and title per bookmark are returned. Further you can select any attribute of the bookmarks table and also the attribute "tags"
* sortby takes and attribute that results will be sorted by descending.

## Maintainers ##

-----------------

* [*Lavysh Alexander*]


## Links ##
<!------------ Links -------------->
[Lavysh Alexander]: http://lavysh.ru


<!------------ Images -------------->
[IO-Logo]: https://dl.dropboxusercontent.com/u/4025012/Static/Projects/All/IO.png "InventiveOnes Ltd."
