# fantasy-sports

Hello! If you're in a private ESPN league with regular seasons ending week 13, this will return a table with historical stats for each team (Wins, Losses, Points For, Points Allowed)

To make this work, you'll need to do a few things before (1) + (2) and after (3) running the script 

(1) grab your league_id and add it where specified in get_season_json
(2) grab your swid and espn_s2 cookies and add it where specified when running r = requests... (this happens twice)
(3) map Team ID to actual humans

To do each,

(1) should be solvable by logging into your ESPN.com page and scanning the URL for a 'leagueid=...'

(2) should take one minute, you just need to inspect the webpage when you're on ESPN.com > then open storage > look at the cookies for espn.com > find the swid and espn_s2 cookies. The stmorse link below has explicit instructions to do so.

(3) should be solvable by either scanning the URL on each team's page on your league homepage or more quickly checking out https://fantasy.espn.com/apis/v3/games/ffl/seasons/2021/segments/0/leagues/'league_id' with your 'league_id' coming from (1). It may be doable programmatically via beautiful soup but I didn't have the time.

______

Credit to https://www.fantasyfootballdatapros.com/blog/ff-analysis/7 (most of the code is copied from their tutorial, some of which be extraneous for the output, in any case my edits are commented using ##) and https://stmorse.github.io/journal/espn-fantasy-v3.html (whose site helped troubleshoot the public vs private league issue).

