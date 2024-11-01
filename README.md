Ruter
1. Booking Service
Endpoint: /api/bookings/<path>
Metoder: GET, POST, PUT
Beskrivelse: Omdirigerer forespørgsler til booking-servicen på http://booking-service:5001.
2. Rengøringsservice
Endpoint: /api/cleaning/<path>
Metoder: GET, POST, PUT
Beskrivelse: Omdirigerer forespørgsler til rengøringsservicen på http://cleaning-service:5003.
3. Faktureringsservice
Endpoint: /api/billing/<path>
Metoder: GET, POST, PUT
Beskrivelse: Omdirigerer forespørgsler til faktureringsservicen på http://billing-service:5002.
Sådan fungerer det
Forespørgsel: Når der sendes en HTTP-forespørgsel til API Gateway'en, modtager Flask-applikationen forespørgslen.
Routing: API Gateway'en identificerer det korrekte mikroservice baseret på URL-path.
Videreførsel: Flask anvender requests til at videresende forespørgslen til mikroservicen og returnerer svaret tilbage til klienten.
Afhængigheder
Python: Version 3.10
Flask: Web-framework for API Gateway
requests: Håndtering af HTTP-forespørgsler til mikroservices