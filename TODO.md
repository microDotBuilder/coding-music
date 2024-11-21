## CREATE DIFFERENT BRANCHES FOR EACH FEATURE

-   [ ] create branch for base template\
         - [ ] include prisma in this
-   [ ] create branch for docker postgress database template
-   [ ] create branch for clerk authentication template
-   [ ] create branch for convex db template
-   [ ] create branch for firebase template

## question about authentication:

-   [ ] how does the session storage works in nextjs
-   [ ] does clerk create a session storage to keep user logged in
-   [ ] if i want to store the user cookie in the session storage \
         can i take it from clerk and store it in the session storage\
         and store that information in the database.\

## for the coding music app:

-   [ ] convex db
-   [ ] firebase
-   [ ] clerk
-   [ ] react-query / tanstack query
-   [ ] react-hook-form

## auth hookup:

-   [ ] learn how cody web dev did the hookup with the clerk\
         convex setup using the session token and jwt token\
         and we want to store the session token in the cookie\
         and use the cookie to store that information and :
        save the cookie information the the databse:

-   [ ] design the database schema to connect the session tokens to the clerk users

<!-- docker run --name nextstatertemplate\
 -e POSTGRES_PASSWORD=supersecretpassword\
 -e POSTGRES_USER=nextstatertemplate\
 -e POSTGRES_DB=nextstatertemplate\
 -p 5432:5432\
 -d postgres -->
