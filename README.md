 # Laravel10_products-app
 Laravel10 Project ( CRUD - Authentication )

  ## in the beginning, Make Laravel-10 project ::
  ````laravel
  composer create-project laravel/laravel:^10.0 apiapp
  ````

### 1- CRUD (Create , read , Update , delete )
````laravel
 php artisun make:migration ' '  --create =''
 ````

### 2- then make controller
````laravel
 php artisun make:controller ' ' --resource --model=' ' 
 ````

 resource : index , edit, show, delete , create

### 3- inherit 
````laravel
@yield(' ')
@extends(' folder name. file name ')
@section (' ')
@endSection
````
-----------------------------------------------------------------
### some syntax have to write :
````laravel
  ::latest()->paginate();
   compact( ' ' )
   validate
   getClientOriginalExtension()
   move( , )
   ::create()

   {{route(' ') }}
   @if
   @endif
   @foreach
   @endforeach
   .Session::get
   @csrf
   .links()
   .dd
   @method('PUT')
   @method('DELETE')
   ->any()
   ->all()
   {{ !!   !!}}
````

-----------------------------------------------------------------
## Authentication ( Login / Register / Middleware )

### 1-you need to setup the code :
````laravel
    Composer require laravel/ui
    php artisun ui bootstrap --auth
    npm install && npm run dev
    npm run build
    php artisun migrate
````

### You ethier make middleware in Controller or Router

2- Contruct Function
````laravel
    public function __Construct(){
      $this->middleware('auth')->expect([ ' ' ])
      $this->middleware('auth')->only([ ' ' ])
    }
````

3- you can make it in router (web.php):
````
   Route::rosource( ' ' ,  ::class) -> middleware('auth');
````
### some syntax have to write :
````laravel
    @auth
    @endauth
    Auth::routes();
````

-----------------------------------------------------------------
## to understand the structure of the projects: 
 1- we make two models ( user , products ) user have three inputs ( name , password , email ) products have three input ( name ,image, details).
 
 2- we make two controllers : productscontroller , authusercontroller.
 
 3- we also have to upload the images.
 
 4- we make CRUD (Store, index , Edit , Update) we use Resources.



