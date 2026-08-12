# Day 1 — Linux core (compressed)

**Date:** Wednesday, 12 Aug 2026  
**Effort:** 6–7 hours (dense day)  

## Learning goals

Operate a Linux host safely: filesystem layout, users/permissions, processes/services, resources, and logs.

## Morning — Filesystem, users, permissions (~3 h)

### Study

- Hierarchy: `/etc`, `/var`, `/home`, `/opt`, `/tmp`, `/proc`, `/usr`  
- Users, groups, ownership, `sudo`  
- Permissions: `644` / `755`; why `777` is unsafe  
- Hard link vs symlink  

### Lab A

1. Create non-root user with controlled sudo; document how.  
2. Create `/opt/intern-app` with correct ownership/permissions.  
3. Create hard link + symlink; prove difference (`ls -li`, `stat`).  
4. Find recently modified files and five largest files under an assigned path.

## Afternoon — Processes, services, resources, logs (~3–4 h)

### Study

- Process vs service; `SIGTERM` vs `SIGKILL`  
- `systemctl` start/stop/restart/enable/status  
- `ps`, `top`, `free`, `df`, `du`, `ss`, `lsof`, `journalctl`  

### Lab B

1. Install/manage Nginx with `systemctl`.  
2. Identify PID, user, listening socket, config, logs.  
3. Record a healthy baseline (ports, disk, memory).  
4. Diagnose one broken Nginx config (mentor injects or copy-break in lab).


## Note for tomorrow

Cron, mounts, and `fstab` are **Week 3** — do not block on them today. Push all notes/scripts to Git before EOD.
