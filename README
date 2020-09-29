#The makeCacheMateic function
#Define inverse
makeCacheMatrix <- function(x = c(1:4, nrow=2, ncol=2)){
               m<-NULL
               set <- function(y) {
                       x <<- y
                       m <<- NULL
        }
        get <- function() x
        setinverse <- function(inverse) m <<- inverse
        getinverse <- function() m
        list(set = set, get = get,
             setinverse = setinverse,
             getinverse = getinverse)     
 }

#return the inverse of a matrix
#solve(x) function
 cacheinverse <- function(x, ...) {
            m <- solve(x)
            if(!is.null(m)) {
                message("getting cached data")
                return(m)
            }
            data <- x$get()
        m <- solve(data, ...)
         x$setinverse(m)
        m
}
