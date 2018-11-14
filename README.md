# The Instakittens project

The Instakittens project is a collection of Instagram-like applications using a
variety of technologies:

- Languages
- Frameworks
- Protocols
- Architectures

This is mostly an educative and explorative project with a strong focus on
tests, not applicative code. Think of [TodoMVC](http://todomvc.com/), but for
testing frameworks. TodoMVC is a great project, but I think that, in the scope
of this project, the data model and the business rules of a To-Do list manager
are too simple compared to most real-world applications, especially on the
following points:

- No complex entity relationships
- No user profiles
- Use case scenarios are very linear and self-contained
- Static, non-temporal data

On the other hand, social applications such as Instagram:

- Are multi-users by nature, interacting with each others
- Define several user profiles
- Implement authentication and authorization policies
- Handle temporal data (e.g. comments)

Last, they only depend on a handful of entities (users, albums, photos,
comments), making them ideal candidates for this experiment.

## Entities

### Users

The application allows several levels of access:

- Anonymous, unauthenticated visitors
- Registered users
- Administrators

### Albums

Users can create any number of photo albums. Albums allow several access levels:

- **Public**: Content is visible by everybody
- **Restricted**: Content is visible by registered users only
- **Private**: Content is visible by owner only

### Photos

Albums can contain any number of kitten pictures.

### Comments

Registered users can post comments under public or restricted album photos.
