---
title: "Design Patterns Refresher"
excerpt: "This is a refresher on Design Patterns"
coverImage: "/assets/blog/design-patterns/design-patterns.jpg"
date: "2020-03-16T05:35:07.322Z"
author:
  name: GS
  picture: "/assets/blog/authors/jj.jpeg"
ogImage:
  url: "/assets/blog/design-patterns/design-patterns.jpg"
---

There are three types of design patterns: Creational, Behavioral and Structural.

## Creational
### Singleton

The Singleton pattern is used to ensure that a class has only one instance, and it provides a global point of access to that instance.
```
public class ConfigurationManager
{
  private static ConfigurationManager _instance;
  private ConfigurationManager() { } // Private constructor prevents external instantiation
  public static ConfigurationManager Instance
  {
    get
    {
      if (_instance == null)
      {
        _instance = new ConfigurationManager();
      }
      return _instance;
    }
  }
  // Configuration data and methods
}
```