# INFO8985 Task 2
lcbo database with signoz demo ... use this as a template to complete task 2, monitoring and logging from the database to the signoz instance.

```bash
git submodule update --init --recursive
```

This will bring submodules for signoz and lcbo in to the project. Look at the README.md in the signoz folder for a patch command. Integrate this in to the up.yml file in the root of this project. When you are happy that you have the patch command correct in up.yml

```bash
ansible-playbook up.yml
```

This does docker compose up on an "empty" signoz in a codespace. Use this as a starting point for instrumenting your app. It also creates a postgresql/pgadmin container with an old version of the LCBO database in it.

```bash
ansible-playbook down.yml
```

This does docker compose down on the `docker-compose.yml` (the same docker-compose file from up.yml)

The task is to make the database do monitoring and logging to the signoz instance.

** Marks

|Item|Out Of|
|--|--:|
|integrate the patch command from the signoz/README.md in to up.yml|2|
|create an otel collector, based on the pattern in signoz/docker to collect from sqlquery and postgresql|2|
|create a metric for some value from the lcbo database and show it in a panel on a dashboard you create|2|
|create a jupyter notebook (.ipynb) that displays some data from the database in a nice neat table or graph based on lcbo/products.ipynb|2|
|update this README to give the steps you used to make it work in a codespace|2|
|||
|total|10|

## Submission

Submit a .zip downloaded from your github. In the comments include a link to your github. Hope that this is fun!