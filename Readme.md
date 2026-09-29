# Baltimore Homicide Data Fetcher (Scala)

A Scala command-line implementation that retrieves annual Baltimore City homicide tables and calculates yearly victim totals plus counts for victims age 18 or younger.

## Highlights

- Uses Java's built-in HTTP client with fallback source URLs.
- Handles unavailable source pages gracefully.
- Prints a readable report or exports `output.csv` / `output.json`.
- Includes a Docker build based on JDK 17 and Scala 2.13.

## Run

```bash
scalac Main.Scala
scala Main
scala Main --output=json
```

Build with Docker using `docker build -t scala-homicide-fetcher .`, then run `docker run --rm scala-homicide-fetcher`.

The project reads public tables published by Cham's Page; results depend on that source’s availability and markup.
