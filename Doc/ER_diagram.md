# This diagram represents the ER relationship diagram among the entities below

#

# In order to understand the cardinality, please refer to the mermaid documentation

# https://mermaid-js.github.io/mermaid/#/entityRelationshipDiagram

#

#

#

#

```mermaid
  erDiagram
          USER ||--|| STUDENT : is
          USER ||--|| MENTOR : is
          USER ||--|| ADMIN : is
          USER ||--|| SIGNIN : has
          STUDENT ||--o{ EVENTS : posts
          STUDENT ||--|| CALENDAR : has
          MENTOR ||--|| CALENDAR : has
          MENTOR ||--|{ WEEKDAYS : tutors
          ADMIN ||--o{ EVENTS : posts
          CALENDAR ||--|{ WEEKDAYS: has
        USER {
            int user_id PK
            string fullName
            string Jnumber
            string email
            string role
            string userName
        }
        STUDENT {
            int student_id PK
            string user_id FK
        }
        MENTOR {
            int mentor_id PK
            string user_id FK
            string course
        }
        ADMIN {
             int admin_id PK
             string user_id FK
        }
        SIGNIN {
            int signIn_id PK
            string user_id FK
            string userName
            string password
        }
        EVENTS {
            int events_id PK
            string mentor_id FK
            string student_id FK
            dateFormat startDate
            dateFormat endDate
        }
        CALENDAR {
            int calendar_id PK
            int weekday_id FK
        }
        WEEKDAYS {
            int weekday_id PK
            int mentor_id FK
            dateFormat startDate
            dateFormat endDate
        }
```
