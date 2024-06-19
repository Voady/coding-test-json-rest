
# Koduppgift för Utvecklare: Skapa ett enkelt REST API för hantering av böcker

## Beskrivning

Ditt uppdrag är att skapa ett enkelt REST API för att hantera en boklista. API:et ska tillåta att böcker läggs till, hämtas, uppdateras och tas bort. Varje bok ska ha följande attribut:

- `id` (unikt heltals-ID)
- `title` (boktitel)
- `author` (författare)
- `published_year` (utgivningsår)

## Krav

1. **GET /books**:
    - Returnerar en lista över alla böcker.
    - Exempel på svar:
    ```json
    [
        {
            "id": 1,
            "title": "To Kill a Mockingbird",
            "author": "Harper Lee",
            "published_year": 1960
        },
        {
            "id": 2,
            "title": "1984",
            "author": "George Orwell",
            "published_year": 1949
        }
    ]
    ```

2. **GET /books/{id}**:
    - Returnerar en enskild bok baserat på dess ID.
    - Exempel på svar:
    ```json
    {
        "id": 1,
        "title": "To Kill a Mockingbird",
        "author": "Harper Lee",
        "published_year": 1960
    }
    ```

3. **POST /books**:
    - Lägger till en ny bok i listan.
    - Exempel på begäran:
    ```json
    {
        "title": "The Great Gatsby",
        "author": "F. Scott Fitzgerald",
        "published_year": 1925
    }
    ```
    - Exempel på svar:
    ```json
    {
        "id": 3,
        "title": "The Great Gatsby",
        "author": "F. Scott Fitzgerald",
        "published_year": 1925
    }
    ```

4. **PUT /books/{id}**:
    - Uppdaterar informationen om en bok baserat på dess ID.
    - Exempel på begäran:
    ```json
    {
        "title": "The Great Gatsby",
        "author": "F. Scott Fitzgerald",
        "published_year": 1925
    }
    ```
    - Exempel på svar:
    ```json
    {
        "id": 3,
        "title": "The Great Gatsby",
        "author": "F. Scott Fitzgerald",
        "published_year": 1925
    }
    ```

5. **DELETE /books/{id}**:
    - Tar bort en bok från listan baserat på dess ID.
    - Exempel på svar:
    ```json
    {
        "message": "Book deleted successfully"
    }
    ```

## Tips och verktyg

- Använd ett backend-ramverk som **Flask** (Python), **Express** (Node.js), **Gin** (Go) eller **Quarkus** (Java) för att skapa ditt API.
- Använd en enkel in-memory datastruktur (som en lista eller en dictionary) för att lagra böckerna.
- Se till att hantera fel, som att försöka hämta eller uppdatera en bok som inte finns.

## Bedömningskriterier

- Funktionalitet: API:et ska uppfylla alla krav.
- Kodkvalitet: Ren och läsbar kod med lämpliga kommentarer.
- Hantering av fel: API:et ska hantera fel på ett användarvänligt sätt.
- Dokumentation: Enkel dokumentation som beskriver hur man kör och testar API:et.

## OpenAPI Specifikation

För en detaljerad OpenAPI-specifikation, se [openapi_spec.yaml](./openapi_spec.yaml).

Lycka till!
