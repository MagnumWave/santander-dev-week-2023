# santander-dev-week-2023
Java RESTful API criada para a Santander Dev Week 2023

# diagrama de entidade e relacionamento

```mermaid
classDiagram
    class User {
        name: String
        account: Account
        card: Card
        features: Feature[]
        news: News[]
    }
    
    class Account {
        number: String
        agency: String
        balance: Float
        limit: Float
    }
    
    class Card {
        number: String
        limit: Float
    }
    
    class Feature {
        icon: String
        description: String
    }
    
    class News {
        icon: String
        description: String
    }
    
    User "1" *-- "1" Account  
    User "1" *-- "1" Card 
    User "1" *-- "1..N" Feature
    User "1" *-- "1..N" News 
```