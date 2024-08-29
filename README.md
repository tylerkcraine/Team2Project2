# Team2Project2

Project2 Backend

Entities

Class Player
- id: UUID
- username: String
- password: String
- role: String
- team: Team.id :UUID

Class Team
- id: UUID
- name: String
- sponsor: Array of Sponsor.id UUID

Class Sponsor
- id: UUID
- category: String
- name: String
- budget: Double

Class Proposals
- id: UUID
- Type: String (PlayerInvite or SponsorProposal)
- Status: String (PENDING/ACCEPTED/REJECTED)
- sender: Team.id if PlayerInvite else Sponsor.id

User Stories

Create user
- url = POST : "/auth/create"
- body = { username: password: name: role: }

login user
- url = POST : "/auth/login"
- body = { username: password: }

change role
- url = patch : "/role"
- path parameter = new role

view sponsors
- url = get : "/sponsors"

Accept/Reject team invite

User/ Manager Stories
- Accept/Reject Sponsor proposals
- Send team invite to Player
- Remove team player
- See Total Investment

Sponsor Stories
- create login
- Send proposal
- Change budget
- See remaining balance

Admin user
- create player/teams/sponsors
