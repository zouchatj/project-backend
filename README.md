# project-backend
asd

## Servers
- Base URL: [http://localhost:8080](http://localhost:8080)

## Paths

### `/api/directors/{id}`
- GET: Get director by ID
- PUT: Update director by ID
- DELETE: Delete director by ID

### `/api/actors/{id}`
- GET: Get actor by ID
- PUT: Update actor by ID
- DELETE: Delete actor by ID

### `/api/movies/`
- POST: Create a movie

### `/api/directors/`
- POST: Create a director

### `/api/actors/`
- POST: Create an actor

### `/api/ratings`
- GET: Get all ratings

### `/api/movies`
- GET: Get all movies

### `/api/movies/{id}`
- GET: Get movie by ID
- DELETE: Delete movie by ID

### `/api/genres`
- GET: Get all genres

### `/api/directors`
- GET: Get all directors

### `/api/actors`
- GET: Get all actors

## Components

### Schemas

#### Director
- `id` (integer, format: int32)
- `firstName` (string)
- `lastName` (string)
- `dateOfBirth` (string, format: date-time)

#### Actor
- `id` (integer, format: int32)
- `firstName` (string)
- `lastName` (string)
- `dateOfBirth` (string, format: date-time)

#### Genre
- `id` (integer, format: int32)
- `genre` (string)

#### Movie
- `id` (integer, format: int32)
- `movieTitle` (string)
- `movieLength` (integer, format: int32)
- `releaseDate` (string, format: date-time)
- `trailerUrl` (string)
- `director` (reference: Director schema)
- `genre` (reference: Genre schema)
- `rating` (reference: Rating schema)
- `actors` (array of Actor schemas)
- `overview` (string)

#### Rating
- `id` (integer, format: int32)
- `rating` (string)
- `description` (string)
