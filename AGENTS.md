# Temporary workspaces

Create a private, task-specific directory below `/tmp/` before writing disposable
host files. Keep logs, fixtures, downloads and build intermediates inside that
directory. Do not create loose files directly in `/tmp` or use the platform's
default temporary root. `/private/tmp` is the macOS alias of `/tmp`.

Remove owned disposable workspaces when their task ends. Check active processes
and open files before cleanup. Preserve unresolved uploads, one-use documents,
audit metadata, durable outboxes and active IPC until their workflow reconciles
them. Never sweep unrelated applications' temporary files. Atomic replacement
files stay beside their destination to preserve same-filesystem rename. Durable
caches, release archives, third-party source and Android device paths are separate
from disposable host scratch.
