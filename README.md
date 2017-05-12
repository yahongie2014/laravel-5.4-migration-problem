After installlation laravel 5.4 and make migrate that
# Error :
>SQLSTATE[42000]: Syntax error or access violation: 1071 Specified key was too long; max key length is 1000 bytes (SQL: alter table users add unique users_email_unique(email))
# you just need to add that line :
>Schema::defaultStringLength(191);
#
then import schema illuminate for laravel on the top
#
>use Illuminate\Support\Facades\Schema;
# save it and type that command : 
>php artisan migrate:rollback or dump your database
#
then make migrate
#
>php artisan make migrate

# Great u r now on :)
