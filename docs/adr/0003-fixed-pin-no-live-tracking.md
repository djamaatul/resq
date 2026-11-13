# Emergency Request location is a fixed pin; no live tracking

An Emergency Request is pinned to the GPS location captured when it is raised (the Requester may manually re-pin). Neither the Requester's nor Responders' positions are tracked live. We rejected live tracking to limit how much location data ResQ collects and exposes, and to keep the MVP simple; Members' own last-known location is stored only while they are Available, solely to compute who is within the Notification Radius.
