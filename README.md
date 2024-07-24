## Diagrama de Classes

```mermaid
classDiagram
  class User {
    -String name
    -Account account
    -Features[] features
    -Card Card
    -News[] news
  }

  class Account {
    -String number
    -String agency
    -Number balance
    -Number limit
  }

  class Feature {
    -String icon
    -String description
  }

  class Card {
    -String number
    -Number limit
  }

  class News {
    -String icon
    -Number description
  }

  User "1" *-- "1" Account
  User "1" *-- "1..N" Feature
  User "1" *-- "0..1" Card
  User "1" *-- "0..N" News
