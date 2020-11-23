# Freelancing Management Site Requirement

## 1. Framework and knowledge

- Framework: MERN
- Knowledge: react, express, material UI, MongoDB

## 2. Structure

- Team member management
- Project management
- Resource management(Templates, Themes, Sample projects)
- Financial management
- ...

## 3. Modules

### 3.1 User Management

- User: id, name, username, birthday, account
- Role: admin, team member

** Relationship **

- User has many roles, projects, resources, clients, skills, plans

### 3.2 Project Management

- Project: id, title, user_id, client_id, type_id, skill_id, escription, github_rul, status, from, to, total amount, percentDone, released amount, review mark
- Client: username, national, 
- Type: id, name - (Ex. template or themes or sample project)
- Skill: id, name - (Ex. react, laravel, ...)

** Relationship **

- Project belongs to client, user, type and belongs to many skill
- Clinet belongs to many users

### 3.3 Resource Manangement

- Resource: id, name, github_url, visibility(in github), type_id, user_id, size(MB), skill_id, popularity

** Relationship **

- Resource belongs to type, user and belongs to many skills

** Popularity **
This is calculated by user recommendations

### 3.4 Financial Management

- Plan: id, user_id, parent_id, type(monthly, weekly or something else), from, to, plan_amount, actual

** Relationship **

Plan belongs to user, parent.

Here "plan belongs to its parent" means that weekly plan belongs to monthly plan for example.