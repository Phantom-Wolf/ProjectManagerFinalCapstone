- so far, I am thinking of having the following business objects: users, projects, tasks, notes

* users: (registered users)

  - id (PK)
  - username
  - email
  - Password

* projects: (created projects)

  - id (PK)
  - name
  - originator (user_id) (FK)

* contributor: (relationship between project originator, their project and allowing a contributor to help)

  - project_id (FK)
  - contributor_id (user_id) (FK)
  - PRIMARY KEY (project_id, contributor_id)

* tasks: (created tasks connected to project tree relationship)

  - id (PK)
  - transfer_id (random generator in front end)
  - project_id (FK)
  - title
  - depth_level
  - parent (either 0 or transfer_id)
  - completion_status

* notes: (notes added to each individual task)
  - id (PK)
  - task_id (FK)
  - user_id (FK)
  - content
  - date_created

### 5. Wireframes

(Example) Landing Page
:-------------------------:
![Landing Page](/github-images/wireframes/landing-page-wireframe.png)
Register Page
![Register Page](/github-images/wireframes/register-page-wireframe.png)

Primary/foreign key: https://itnext.io/how-to-have-unique-identifier-in-your-postgresql-database-using-primary-key-and-foreign-key-9d2ddd4efce2
