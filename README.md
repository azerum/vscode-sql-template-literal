# vscode-sql-template-literal

Highlights code inside string as SQL, if that string starts with ```/*sql*/``` or ```sql``` (case-insensitive)

```js
sql`select * from users;` //highlights
/*sql*/`select * from users;` //highlights

//does not highlight; there should be no other characters inside the comment,
//including spaces
/* sql */`select * from users;` 

SQL`select * from users`; //highlights
/*SQL*/`select * from users`; //highlights
sQl`select * from users`; //highlights, and ugly
```
