Issues Resolved:
https://github.com/mjl62/event_manager/issues/1
https://github.com/mjl62/event_manager/issues/3
https://github.com/mjl62/event_manager/issues/5
https://github.com/mjl62/event_manager/issues/7
https://github.com/mjl62/event_manager/issues/9
https://github.com/mjl62/event_manager/issues/13

All issues have a linked pull request in their history and on the right side of the page under "Development". Any commits or pull requests that fixed an issue will include "Resolves #_" with the issue number.

Coverage was already at 93% when I forked the repo, but I still added and changed where needed.

Docker Hub Image: https://hub.docker.com/repository/docker/mattlidonni/event_manager

Overall this reinforced a lot of practices I've been recently accustomed to in my Capstone course. Since I handle front end tasks in that group, this was a nice way to experience more of the backend and database programming. I faced some challenges with getting used to managing PostGres and the database needing to be reconstructed after running tests. In one or two situations I spent some time troubleshooting without realizing I still needed to reconstruct the database, and had me confused for a bit.

Another issue I had was my GitHub actions failing, which was due to the Docker Scan step catching a very recent vulnerability in Gunicorn. I wasn't sure if this was intentional, but I handled it like the other problems and created a new issue. I researched a solution online, finding that Gunicorn had patched this vulnerability in their most recent version, so I opened a new branch and updated Gunicorn to 22.0.0. I ran all my tests again and manually tested all the endpoints and functionality over again incase something in the newer version broke the app, but it all worked the same and I pushed the change.
