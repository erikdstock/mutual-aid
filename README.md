# Mutual-Aid-in-a-Box

A tool for coordinating a loosely-centralized mutual aid network.

MVP features (final naming TBD):

- [ ] `User` can sign up to help (contact info required)
- [ ] User can hav `admin` role
- [ ] Admin dashboard restricted to admin users user can administer all objects
- [ ] User can make a request (a `Request`) with a location + notes - they are now a requestor
- [ ] Helping user can see nearby requests (v1: search by postal code)
- [ ] User can mark themselves as the responder (`Fulfillment` joins `request` + `user`)
- [ ] Admin can contact requestor and responder to mark a fulfillment complete
- [ ] Users can contact admins with issues

Post-MVP:

- Create requests without creating an account (perhaps a minimal user that only has a phone number?)
- Admins can designate regions - a collection of zip codes
- Ability to look up needs by location, including current location
- Visibility into level of need by area
- A supposed response can be marked unfulfilled
- User stats are visible somewhere, maybe only to them and admins, re fulfillments vs abandoned fulfillments

## Development setup

You'll need

- ruby 2.6.1 (with bundler)
- node 12.14.1 (with yarn)
- a running postgresql server

1. Clone + enter this repo
2. Install dependencies: `bundle install && yarn`
3. Set up database: `rails db:setup && rails db:migrate`
4. Run tests: `bundle exec rails spec`
5. Run server: `bundle exec rails s`
