Cargo and Departmental Economy
==============================

This proposal details a rework of the cargo department and the use of money as a vector of roleplay/gameplay in all departments.

## Preface

Right now, cargo as a department, as well as the economy, lies in a very bad spot. Money is a pointless resource, as it can be produced in abundance, and there is a lack of meaningful things to spend it on. Materials, as well as a few others, are common purchases, but if salvage does a good enough job you end up sitting on a pile of money (the only really interesting thing you can do with which is gamble).

Certain departments' gameplay tends to be completely reactive; Medical, Engineering, and Security all rely upon something to go wrong in order to have interesting rounds, or even something to do at all. This is a bad state of affairs, as it's hard to get people invested in a specific round when their gameplay only consists of fighting off bad things from happening, rather than potentially building towards something.

The jobs that actually have something to do are often antisocial, which goes against one of our stated goals of making jobs more involved in social interaction, and not designing them around isolation.

Lastly, the ATS is a problem. It is a major target for antagonistic behavior that is far separated from the consequences of doing something on station. Why make a secret room or base in maints when you can stash things in the backroom of ATS that nobody ever checks? If your goal is to destroy the station, the ATS is also an obvious target; you can cut off the station from any further resources at basically no risk. Also, it being considered part of the station in code causes many bugs. There are many hacky solutions that are employed to try and make these things not the case, but I think a total rethink of it is in order.

## Changes

I think we can kill 4 birds with one stone here, as these problems are in many ways interlinked.

### Departmental Money-Making and Expenditures
The solution looks something like
Each department:
- Has its own way of making money
- Has Costs they need to cover to keep the department running
- Having the above things interface with cargo where possible

The way departments should make money should include behavior we wish to encourage.
These things should often include but are not limited to:
- A mechanic, feature, or behavior in the department that is underutilized or unexplored
- A behavior that is social or roleplay oriented
- Things which make the player more invested in the station and the current round

Money making features should not:
- Encourage a role to become more isolated
- Consume enough of a role's attention that they are unable to focus on other things

For each department, here are some examples of potential sources of income that meet the requirements. These are by no means final or their exclusive ways, but they follow the above guidelines

Engi:
- Selling power
  - encourages producing more power than is simply necessary for the station.
- Atmos gets orders for large quantities of certain gases.

Science:
(Both of these already exist somewhat)
- Selling researched artifacts
- Tech disk rework - persistent research point cost

Security: (These also need more discussion, to prevent sec from arresting everyone)
- Prisoner Labor
  - Prisoners should have several tasks they can do within the brig to make small amounts of money for Security, they can use this money to shorten or bypass their sentence.
- Fining Other Departments
  - For minor crimes, departments should be fined instead of someone being arrested
- Potentially remake of lawyer or adding a magistrate role to arbitrate security arrests, in the worst case where they arrest everyone. This would be a non-antag, mindshielded role

Medical:
- Producing medicine/chemicals
  - Having chem produce large quantities of either niche or high quality chemicals
- Blood test/donations or medical checkups
  - Medical receives task to take blood from or do medical checkups on random people on the station, which makes them money

All departments:
- Selling misc items
- Printing bills to other departments
  - You print the bill in one console, and insert it into the target one that has to pay, then they have to accept

Departments should also have expenses which facilitate the need for departments to have money

Department expenses should:
- Not require enough overhead to where one must constantly focus on their job
- Provide meaningful incentive to have and obtain money

### Changes to Cargo
With all the departments interacting with money in some fashion, this drastically reshapes the role of the cargo department. 

Basis of how cargo will work is the following

- The rest of the station loses their direct market access.

- The rest of the station will buy orders through cargo directly at a static price.

- Cargo has access to market goods and services, at a fluctuating price.

- Other departments will sell their products (where applicable) to the market through cargo (cargo will take a small cut of this)


- Cargo's job then becomes to fulfill orders that are given to them from other departments, either through making market purchases that they then resell to the department, or through supplying the order using their own stock.

This turns cargo more into a logistics operation, rather than doing random fetch quests. This also makes their job more purposeful, as they have to coordinate and interact with the station intimately, rather than leave a yellow note on someone's desk.

### Changes to the ATS and FTLing
The ATS is stupid and causes problems. There are two solutions to this which I can see working:

- Starsector Inspired FTLing
  - FTL is underutilized, clunky, and also stupid for reasons that I will not get into. However, there was a suggestion to improve this which can be integrated into the solution for the ATS. This solution is to make one specific area, which you must go to, in each system where you are capable of using FTL rather than allowing it anywhere on the map. We can integrate the ATS into this by making it, or perhaps multiple of them (with perhaps some market variation between them), one of the FTL destinations within other systems. This makes the ATS far less prone to much of the BS, as we can highly restrict its usefulness for antags, as well as make it not part of the main station grid.

- Just remove it
  - Revert to be similar to the old cargo system, where you get orders directly on the station.