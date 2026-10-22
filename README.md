# Watchlist

CS310 Mobile Application Development - Group 15

Watchlist is a proposed Flutter app for browsing movies from one external API,
filtering by genre, and keeping a personal watchlist with watched status stored
on the device.

## Group

| Member | Student ID | Step 1 responsibilities |
| --- | --- | --- |
| Baran Aksoy | 33575 | All tasks jointly with Adar: proposal, scope, API feasibility, data requirements, challenges, repository setup, and final review. |
| Adar Dogru (spelling to confirm) | 34269 | All tasks jointly with Baran: proposal, scope, API feasibility, data requirements, challenges, repository setup, and final review. |
| TBA | TBA | TBA |

Step 1 coordinator: Baran Aksoy (33575). Third-member details require confirmation with the TA.

## Planned core features

- Browse movies and filter by genre using one external API.
- View title, poster, description, and provider rating.
- Add and remove saved movies, avoiding duplicates.
- Mark saved movies watched or unwatched and retain these changes after restart.

Optional: swipe gestures, if time remains after completing the core features.

## Data and technical plan

- Flutter application with HTTP requests and JSON parsing.
- API: TMDB. An authenticated feasibility check on 22 October 2026 passed: genre list, genre-filtered movies, movie details, and poster retrieval.
- Local storage for saved movie IDs, titles, poster references, and watched status.
- No sign-in, cloud database, or cross-device sync in the current scope.
- Browsing new movies and loading remote posters require internet access.
- TMDB ratings will be labeled as TMDB ratings. Required provider attribution
  will be included if this provider is used.

## Current status

Step 1 planning only. Application implementation has not started.

The API feasibility check used Baran's TMDB account on its Free Developer plan.
It checks API connectivity and data retrieval; the Flutter app is not implemented yet.

Before submission: confirm remaining group details and membership, review this scope
as a group, and verify accepted collaborator access.

## API references

- [TMDB movie discovery](https://developer.themoviedb.org/reference/discover-movie)
- [TMDB application authentication](https://developer.themoviedb.org/docs/authentication-application)
- [TMDB API FAQ and attribution](https://developer.themoviedb.org/docs/faq)

Credentials must not be committed to this repository.
