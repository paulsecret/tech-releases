# tech-releases
Information about releases from the tech department

## Purpose

This repository should contain a lot of information relevant to "what happened"
on a given date that might be relevant to an investigation.

Significant changes in behaviour might be explained by releases on specific
dates, so we would like to centralise this data to allow investigators to find
relevant factors more efficiently.

Much of the information here will still require technical interpretation and
filtering to make sure that relevant data can be found and make sure that
unrelated changes can be ignored.

Please ask for help.

## Structure
Information should be sorted by date. When a new release occurs, it should be
recorded in a file in the directory with the matching date.

For example, a release on 31 March 2025 should be stored in
`2025/03-march/31-monday/releases.txt`.

## Types
There are several types of "release" that we want to log here.

1. ArgoCD deployments
2. Feature releases
3. "Significant" configuration changes applied
4. "Significant" database insert/update queries invoked

### ArgoCD deployments

We would like to document all deployments to `production` via ArgoCD in a file
for each day.

As of November 2024, this still needs to be configured.

### Feature releases

Some features are activated using methods other than ArgoCD deployments.

For example, functionality in `outfittery-mobile-app` can be activated using
Firebase configuration.

### Significant configuration changes

Some configuration is stored as a database value and read in real-time,
allowing significant changes to the behaviour of the system based on a single
value being updated.

For example, changing the value of the prepayment amount required can
significantly affect CR1 and default rates.

As of November 2024, what counts as "significant" has not been specified.

### Significant database queries

Some large database insert/update queries can cause significant changes in the
behaviour of the system. For example, changing the due date of large numbers of
opportunities could cause large batches of orders to be created.

As of November 2024, what counts as "significant" has not been specified.

## Contacts

If you have questions, please ask:

* Matthew Heard (matthew.heard@outfittery.de)
* Martin Trajkow (martin.trajkow@outfittery.de)
* Jakub Jabłoński (jakub.jablonski@outfittery.de)
