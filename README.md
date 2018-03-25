# rankPrivateVPNServers

List and rate the PrivateVPN servers

```
usage: rankpvpn [-h] [--list-countries] [--save <filepath>]
                [--sort {rate,country}] [--threads n] [--verbose] [--info]
                [--ip] [-c <country>] [-f n] [-i <regex>] [-x <regex>] [-n n]
                [-r]

Retrieve and filter the list of PrivateVPN servers

optional arguments:
  -h, --help            show this help message and exit
  --list-countries      Display a table of the distribution of servers by
                        country.
  --save <filepath>     Save the server-list to the given path.
  --sort {rate,country}
                        Sort the serverlist. "rate": avarage ping; "country":
                        server's location.
  --threads n           The number of threads to use when rating servers.
  --verbose             Print extra information to STDERR. Only works with
                        some options.
  --info                Print server information instead of a server list.
                        Filter options apply.
  --ip                  Display your public IP.

filters:
  The following filters are inclusive, i.e. the returned list will only
  contain servers for which all of the given conditions are met.

  -c <country>, --country <country>
                        Match one of the given countries (case-sensitive). Use
                        "--list-countries" to see which are available.
  -f n, --fastest n     Return the n fastest servers that meet the other
                        criteria. Do not use this option without other
                        filtering options.
  -i <regex>, --include <regex>
                        Include servers that match <regex>.
  -x <regex>, --exclude <regex>
                        Exclude servers that match <regex>.
  -n n, --number n      Return at most n servers.
  -r, --random          Choose a random server.

```

Based on [Reflector](https://xyne.archlinux.ca/projects/reflector/) from Archlinux, thanks Xyne!
