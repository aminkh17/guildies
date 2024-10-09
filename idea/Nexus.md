# Nexus
A central point where engineers connect their knowledge and propose ideas.A place where ideas are crafted and transformed into sessions

**Purpose:** Engineers express interest in hosting sessions, providing details about themselves and their proposed topics.
- An engineer who would like to host a session will register his/her expression of interest including his/her about me part
- the request will then review by guild editors. they could be able to communicate on the topic to understand more and have an option to nourish the idea and eventually approve or reject the guild topic 
- once it's been approved, the engineer will have opportunity to propose a closest date for his/her session

---

```mermaid
 
architecture-beta
    group api(logos:aws-lambda)[API]

    service db(logos:aws-aurora)[Database] in api
    service disk1(logos:aws-glacier)[Storage] in api
    service disk2(logos:aws-s3)[Storage] in api
    service server(logos:aws-ec2)[Server] in api

    db:L -- R:server
    disk1:T -- B:server
    disk2:T -- B:db
 

 


```

```mermaid

graph TD
    subgraph Client Side
        A1[User Interface - Web/PWA]
        A2[Mobile App - PWA]
        A3[MS Teams Channel]
    end

    subgraph Backend
        B1[API Gateway] --> |Auth Requests| C1[Authentication Service]
        B1 --> |Session Proposals| C2[Session Management Service]
        B1 --> |File Uploads| C3[Media Service]
        B1 --> |Data Fetch| C4[User Profile Service]
        B1 --> |Session Notifications| C5[Notification Service]
        
        subgraph Async Workers
            C6[Background Worker] --> C2
            C6 --> |Large File Processing| C3
            C6 --> |Notification Triggers| C5
        end
    end

    subgraph Storage
        C7[Relational Database - User & Session Data]
        C8[Redis Cache - Session Metadata]
        C9[Cloud Storage - OneDrive, Google Drive, SharePoint-]
        C3 --> C9
    end
    
    subgraph External Integrations
        D1[OneDrive]
        D2[Google Drive]
        D3[SharePoint]
        C9 --> D1
        C9 --> D2
        C9 --> D3
    end
    
    subgraph CDN Layer
        D4[Content Delivery Network - Static Media Delivery]
        C9 --> D4
    end

    %% Client to Backend interactions
    A1 --> B1
    A2 --> B1
    A3 --> B1
    
    %% Backend Storage interactions
    C2 --> C7
    C4 --> C7
    C2 --> C8
    C3 --> C9
    C5 --> C9
```