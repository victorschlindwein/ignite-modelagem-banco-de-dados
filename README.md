This diagram was made at https://dbdiagram.io/

Code:

Table users as U {
id uuid pk
first_name string
last_name string
email string
created_at date
updated_at date
}

Table users_games {
usersId uuid [pk]
gamesId uuid [pk]
}

Table games as G {
id uuid pk
title string
created_at date
updated_at date
}

Ref: U.id < users_games.usersId
Ref: G.id < users_games.gamesId
