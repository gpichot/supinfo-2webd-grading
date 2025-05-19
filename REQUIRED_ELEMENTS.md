# Required Elements for MET Museum Interface Tests

This document lists all the CSS classes, selectors, and text content that must be present in your implementation for the end-to-end tests to pass.

## Global Elements

### Navigation
- A navigation element with role="navigation" containing links
- A link with text "Recherche avancée"

### Quick Search
- An input with placeholder="Recherche rapide..."
- A button with text "Rechercher" near the search input

## Home Page

### URL Structure
- The home page should be accessible at the root URL "/"

### Highlighted Articles
- A section with class ".highlights-section" containing artwork cards
- Multiple elements with class ".artwork-card" inside the highlights section
- A heading with text "Oeuvres en vedette"

## Advanced Search Page

### URL Structure
- The advanced search page should be accessible at "/advanced-search"

### Form Elements
- A form with attribute name="advanced-search"
- A select element with label "Département"
- An input with label "Date de début"
- An input with label "Date de fin"
- An input with label "Mots-clés"
- A button with text "Rechercher" inside the form

### Search Results
- Elements with class ".artwork-card" for search results
- A heading or text "Résultats de Recherche" when results are displayed
- Text "Aucun résultat trouvé. Essayez d'ajuster vos critères de recherche." when no results match

## Item Detail Page

### URL Structure
- Item detail pages should be accessible at "/object/{id}" where {id} is the object ID

### Item Details
- A heading (h1) for the item title
- An image with class ".artwork-detail-image"
- Text containing "département" for department information
- A section with class ".artwork-detail" containing the item details
- For specific test items:
  - Item ID "229770" should display:
    - Text "Hunting and fishing scenes"
    - Text "Robert Jones"
    - Text "1769"
    - Text "European Sculpture and Decorative Arts"
    - Text "Linen and cotton"

## Quick Search Results
- Elements with class ".quick-search-item" for search results
- For specific test searches:
  - Search for "Monet" should display:
    - Text "The Monet Family"
  - Search for non-existent items should display:
    - Text "Aucun résultat trouvé"

## Advanced Search Results
- For specific test searches:
  - Search for "portrait" should display results containing "Portrait"

## Notes for Implementation
1. All pages should have the quick search functionality available
2. Navigation should be consistent across all pages
3. Form controls should have proper labels for accessibility
4. The website should be in French
5. All API calls should use the MET Museum API
