# testing_erd_mermaid_diagraming_on_github
Trying to see if the ERD (Entity Relationship Diagrams) portion of Mermaid works on GitHub.

```mermaid
erDiagram
    USERS ||--|{ POSTS : write
    USERS ||--|{ REPLIES : write
    USERS ||..|{ FAVORITES : chose
    USERS {
        string id PK
        string username
        string email
        datetime date_created
    }
    POSTS {
        string id PK
        string user_id FK
        string content
        datetime date_created
    }
    REPLIES |{--|| POSTS : respond
    REPLIES {
        string id PK
        string user_id FK
        string post_id FK
        string content
        datetime date_created
    }
    FAVORITES {
        string id PK
        string user_id FK
        string post_id FK
    }
```
Keys can be PK, FK or UK, for Primary Key, Foreign Key or Unique Key. 
