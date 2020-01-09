# PSR-15 closure middleware

This package implements a simple PSR-15 adapter middleware for closures. This way simple closures
can be used to implement middleware functionality. The closure receives the request and the next 
handler and **must** return an instance of `ResponseInterface`:

    $middleware = new ClosureMiddleware(function ($request, $next)  {
                                        
        /** insert your code here **/

        return $response;
    }); 

Not only closures, but any `callable` can be passed to the closure middleware.
