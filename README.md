# A Simple [Battlesnake](http://play.battlesnake.com) Written in Python

This is an implementation of the [Battlesnake API](https://docs.battlesnake.com/references/api). 

It is designed to be:
- Stateless - a decision is made based on the board state provided on request.
- Reusable - all game modes are accounted for in one code base.
- Performant - enough to run on a low-power device.  It could be much better!

It has code to:

- Avoid the edges of the map.
- Avoid collisions with other snakes on the board.
- Avoid entering spaces too small to fit, unless space would be vacated by exiting snake bodies.
- Avoid hazard spaces unless it's where our food is.
- Seek food when other snakes are larger, and avoid it when we don't need it.
- Consider the pathfinding exercise when locating available food.
- Blindly find food when very low in health.
- Take a certain winning move when an opponent snake has one available move.
- Take a drafting larger snake to a wall, just to see what happens.
- Consider options when other snakes are in collision range.
- If we have trapped a snake between ourselves and a wall, close the lane if possible.
- Avoid paths that could be closed due to other snake movement.
- Accept a board state and return debugging output for a single move.

### Next steps

- Improve hazard code to reduce time spent in hazards.
- Unit and regression tests.
- Improve logic to prioritize survival, then advantages, then wins.

### Possible refactoring

- A better idling strategy than choosing a random move.
- Improve pathfinder code to use a multi-node tree, to collect more info as we seek a 'best' path.
- Perform pathfinding on other snakes to consider where collisions or traps are.
- Optimize to run better on the Raspberry Pi.

### Technologies Used

* [Python3](https://www.python.org/)
* [CherryPy](https://cherrypy.org/)

### Resources

Battlesnake documentation is available at [docs.battlesnake.com](https://docs.battlesnake.com), including detailed Guides, API References, and Tips.

You can also join the Battlesnake Developer Community on [Discord](https://discord.gg/FZusE7FH4q). We have a growing community of Battlesnake developers of all skill levels wanting to help everyone succeed and have fun with Battlesnake!
