# Watchlist

CS310 Mobile Application Development - Group 15

Watchlist is a proposed Flutter mobile app, targeting Android first, for students
and casual movie viewers. It combines movie discovery, title search and a personal
watchlist with watched status and personal star ratings stored on the device.

## Group and Step 1 responsibilities

| Member | Student ID | Assigned tasks |
| --- | --- | --- |
| Baran Aksoy | 33575 | All Step 1 tasks jointly with Adar: proposal, scope, API feasibility, data requirements, challenges, repository setup and final review; Step 1 coordinator. |
| Adar Doğru | 34269 | All Step 1 tasks jointly with Baran: proposal, scope, API feasibility, data requirements, challenges, repository setup and final review. |
| Ozan Barış Turgut | Pending confirmation | Review the revised scope and user-input features; write or revise the final data/storage and technical-challenges sections; review the final proposal and README. |

Step 1 coordinator: **Baran Aksoy (33575)**. A different member will coordinate
the next step. These are assigned responsibilities; all members must review the
final submission and be able to explain their own work.

## Planned core features

- Browse TMDB movies and filter the discovery list by genre.
- Search by movie title through a text field and Search button.
- View title, poster, description and the provider's TMDB score (0-10).
- Add or remove watchlist entries, preventing duplicate movie IDs.
- Mark saved movies watched or unwatched.
- Add, edit or clear a personal rating of 1-5 stars for a saved movie.
- Preserve saved movies, watched status and personal stars across app restarts.

## Optional features

A release-year lower bound and minimum TMDB-score filter for discovery browsing,
only after completing the core. Title search is a separate mode.

Shared-user rating cohorts, discovery-history analysis, review summaries,
accounts, cloud synchronization and a shared backend are outside this scope.

## Data and technical plan

- Flutter with HTTP requests and JSON parsing; TMDB is the single movie provider.
- SQLite via **sqflite**, with **path**, for local storage on the Android target.
- One saved-movies table: TMDB movie ID (primary key), title, poster reference,
  watched flag and nullable personal rating (integer 1-5).
- Personal ratings stay local and are separate from TMDB scores.
- Saved titles, watched flags and personal stars are usable offline. New browsing,
  search, details and uncached remote posters require internet access.
- Include required TMDB attribution and refresh or clear provider metadata within
  the provider's caching limit. Never commit API credentials. A mobile build
  cannot guarantee credential secrecy.

## Feasibility and status

Step 1 planning only; the Flutter application has not been implemented.
An authenticated check using Baran's TMDB Free Developer account passed on
22 October 2026 for genre listing, genre-filtered discovery, details and poster
retrieval. Title search is documented by TMDB. The new Flutter search and SQLite
flows still need implementation and testing.

Baran owns this public repository. Adar has accepted collaborator access as
**Adar-21**. An invitation was issued to Ozan's confirmed school email on
25 October 2026; acceptance remains pending. Ozan's student ID also needs confirmation.

## Implementation sequence

1. Build Discover, Search and Details screens with loading, empty and error states.
2. Add the SQLite watchlist, duplicate prevention and watched-status controls.
3. Add the personal star selector and persistence.
4. Verify: search -> open a movie -> save -> change status and stars -> restart
   -> confirm the same saved values. Also check removal, no results and network failure.
5. Consider optional year and TMDB-score filters only after the core works.

## References

- [TMDB discovery](https://developer.themoviedb.org/reference/discover-movie)
- [TMDB title search](https://developer.themoviedb.org/reference/search-movie)
- [TMDB authentication](https://developer.themoviedb.org/docs/authentication-application)
- [TMDB FAQ and attribution](https://developer.themoviedb.org/docs/faq)
- [Flutter: persist data with SQLite](https://docs.flutter.dev/cookbook/persistence/sqlite)
