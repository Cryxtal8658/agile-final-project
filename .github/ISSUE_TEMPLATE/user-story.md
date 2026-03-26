---
name: User Story
about: A user story for the product backlog
title: ''
labels: ''
assignees: ''
---

## User Story
As a back-end developer,
I need to create a product in the catalog,
So that customers can view and purchase available products.

## Acceptance Criteria
```gherkin
Given a valid product with name, description, and price
When I send a POST request to the /products endpoint
Then the product is saved to the catalog and a 201 response is returned
```

### Story 2 — Retrieve a Product
As a back-end developer,
I need to retrieve a product from the catalog,
So that product details can be displayed to customers.
```gherkin
Given a product with a valid ID exists in the catalog
When I send a GET request to the /products/{id} endpoint
Then the product details are returned with a 200 response
```

### Story 3 — Update a Product
As a back-end developer,
I need to update a product in the catalog,
So that product information stays accurate and current.
```gherkin
Given a product with a valid ID exists in the catalog
When I send a PUT request with updated data to /products/{id}
Then the product is updated and a 200 response is returned
```

### Story 4 — Delete a Product
As a back-end developer,
I need to delete a product from the catalog,
So that discontinued products are removed from the system.
```gherkin
Given a product with a valid ID exists in the catalog
When I send a DELETE request to the /products/{id} endpoint
Then the product is removed and a 204 response is returned
```

### Story 5 — Like a Product
As a customer,
I need to like a product in the catalog,
So that I can save my favorite products for future reference.
```gherkin
Given a product with a valid ID exists in the catalog
When I send a POST request to /products/{id}/like
Then the product like count increases by 1 and a 200 response is returned
```

## Definition of Done
- [ ] Acceptance criteria met
- [ ] Code reviewed and approved
- [ ] Unit tests written and passing
- [ ] Deployed to cloud environment
```
