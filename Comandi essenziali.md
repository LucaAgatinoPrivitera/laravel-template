# Comandi essenziali: #

`composer install`

`php artisan key:generate` (mi da errore)

`npm i`

`php artisan serve` (lo devo fare dopo run dev a quanto pare mi da errore altrimenti)

`npm run dev`



### Controller e Model ###
```
`php artisan make:controller Folder/NameController` (creo il controller dove dentro ci metto le funzioni per le route)

php artisan make:model MyModel (con questo creo un modello, che sarà il DB)

```



### Migration e Faker (non il giocatore )###
```
php artisan make:migration create_users_table (creo una migration in database/migrations)

php artisan migrate (eseguo le migrazioni che ho creato)

php artisan migrate:rollback (torno allo status precedente, annulla tutto il bloccone di codice eseguito prima)

php artisan migrate:reset (resetto tutto quanto, hard delete praticamente)

php artisan make:seeder UsersTableSeeder (creo un seeder)
Alla fine della funzione serve il ->save()

php artisan db:seed --class=UsersTableSeeder (eseguo il seed)

public function run (Faker $faker) da mettere nel seeder ci permette di compilare in automatico e casualmente
RICHIEDE: use Faker\Generator as Faker;


Il controller mi permette di dare i dati attraverso per esempio $dato, a una o più pagine attraverso il web.php.

Migration crei la struttura, e seeder invece popoli la struttura.