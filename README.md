# kiln-run

The viewer page for [KILN](https://github.com/sams808/KILN) runs, published
at **https://sams808.github.io/kiln-run/**.

KILN turns a furnace program into a link whose fragment — everything after
the `#` — carries the resolved run: the profile, the step boundaries and
the feature times. Browsers never send a fragment to a server, so this page
receives no data from anyone. It reads the fragment, works out where the
run is against the phone's clock, and draws it.

Scanning a second code adds a second run, so several furnaces can be
followed at once; opening the address with no fragment lists them. Runs are
held in the browser's local storage on that device alone and are forgotten
a day after they finish.

The page is a single file with no dependencies and no network requests of
any kind, so it keeps working with no signal once it has loaded — which is
the point, for a program that runs overnight.
