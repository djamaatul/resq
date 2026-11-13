# ResQ

ResQ is a community emergency-assistance platform: a Member in trouble raises an Emergency Request at their location, and nearby Members are notified so they can come and help. It is peer help, not a replacement for official emergency services.

## Language

### People

**Member**:
A registered person using ResQ. Any Member can both ask for help and give help.
_Avoid_: User (ambiguous with Admin), Volunteer, Customer
_UI (id)_: Pengguna

**Requester**:
The Member who raised a given Emergency Request. A role within one request, not an account type.
_Avoid_: Victim, Sender, Reporter
_UI (id)_: Peminta Bantuan

**Responder**:
A Member who helps with a given Emergency Request. A role within one request, not an account type.
_Avoid_: Helper, Volunteer, Rescuer
_UI (id)_: Penolong

**Admin**:
A platform operator who moderates Emergency Requests, manages Members, and monitors platform activity. Not a Member.
_Avoid_: Moderator, Operator
_UI (id)_: Admin

### Emergencies

**Emergency Request**:
A call for help raised by a Requester, pinned to the GPS location captured when it was raised.
_Avoid_: Signal, SOS (as a noun), Alert, Incident, Report
_UI (id)_: Permintaan Darurat

**SOS**:
The act of raising an Emergency Request. A verb/button, never the name of the thing created.
_UI (id)_: SOS

**Emergency Category**:
The required, fixed classification of an Emergency Request: Accident, Fire, Crime, Medical, Natural Disaster, or Other.
_Avoid_: Type, Kind
_UI (id)_: Jenis Darurat (Kecelakaan, Kebakaran, Kriminal, Medis, Bencana Alam, Lainnya)

**Request Status**:
Where an Emergency Request is in its life: Open → Being Helped while active, then one end state: Resolved, Cancelled, Expired, or Closed by Admin.

**Open**:
An active Emergency Request with no active Assistance yet; it returns here if every Responder withdraws.
_UI (id)_: Menunggu Bantuan

**Being Helped**:
An active Emergency Request with at least one active Assistance.
_Avoid_: In progress, Handled
_UI (id)_: Sedang Dibantu

**Resolved**:
The end state of an Emergency Request that the Requester declares handled.
_UI (id)_: Selesai

**Cancelled**:
The end state of an Emergency Request the Requester withdrew because help is no longer needed.
_UI (id)_: Dibatalkan

**Notification Radius**:
The single platform-wide distance (set by an Admin) within which Members are notified of a new Emergency Request.
_Avoid_: Range, Coverage area
_UI (id)_: Radius Notifikasi

**Request Chat**:
The single conversation attached to an Emergency Request, shared by its Requester and all its Responders.
_Avoid_: Message, DM, Thread
_UI (id)_: Obrolan

**Expired**:
The end state of an Emergency Request left unresolved past its allowed lifetime.
_Avoid_: Timed out, Stale
_UI (id)_: Kedaluwarsa

**Closed by Admin**:
The end state of an Emergency Request ended through Moderation, always carrying a Closure Reason.
_Avoid_: Removed, Deleted, Rejected
_UI (id)_: Ditutup Admin

**Closure Reason**:
Why an Admin closed an Emergency Request: False Alarm, Abuse, Duplicate, or Other.
_UI (id)_: Alasan Penutupan (Alarm Palsu, Penyalahgunaan, Duplikat, Lainnya)

### Helping

**Assistance**:
One Responder's commitment to one Emergency Request, with its own progress separate from the request's state. An Emergency Request can have many Assistances.
_Avoid_: Response, Help, Task
_UI (id)_: Bantuan

**Available**:
A Member who has opted in to receive Emergency Requests; only Available Members within the Notification Radius of their last-known location are notified.
_Avoid_: Online, Active, On duty
_UI (id)_: Siap Membantu

**Assistance Status**:
The progress of one Assistance: Accepted → On the Way → Arrived → Completed, or Withdrawn.
_UI (id)_: Diterima → Dalam Perjalanan → Tiba → Selesai / Mundur

**Accept**:
A Member taking on an Emergency Request, which creates their Assistance and makes them a Responder.
_UI (id)_: Terima

**Decline**:
A nearby Member dismissing an Emergency Request from their own view. It has no effect on the request or anyone else.
_Avoid_: Reject
_UI (id)_: Tolak

**Withdraw**:
A Responder backing out of an Assistance they previously accepted.
_Avoid_: Reject, Cancel
_UI (id)_: Mundur

### Administration

**Moderation**:
An Admin's intervention on an Emergency Request, such as marking it a false alarm, closing a stale one, or removing abuse.
_Avoid_: Emergency Report, Report management

**Suspended**:
A Member an Admin has barred from logging in, raising, or accepting Emergency Requests until reactivated.
_Avoid_: Banned, Blocked, Deleted
_UI (id)_: Dinonaktifkan
