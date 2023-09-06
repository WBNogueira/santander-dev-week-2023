# Santander Dev Week 2023
Java RESTful API para a Santander Dev Week.

## Diagrama de Classes

```mermaid
classDiagram
    class User {
        - id: long
        - name: string
        - account: Account
        - features: Feature[]
        - card: Card
        - news: News[]
    }

    class Account {
        - id: long
        - number: string
        - agency: string
        - balance: float
        - limit: float
    }

    class Feature {
        - id: long
        - icon: string
        - description: string
    }

    class Card {
        - id: long
        - number: string
        - limit: float
    }

    class News {
        - id: long
        - icon: string
        - description: string
    }

    User "1" *-- "1" Account
    User "1" *-- "N" Feature
    User "1" *-- "1" Card
    User "1" *-- "N" News

