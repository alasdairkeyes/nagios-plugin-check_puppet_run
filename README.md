# nagios-plugin-check_puppet_run
Nagios plugin to monitor puppet run results and last run time

## Dependencies

* Getopt::Long Perl module
* Nagios::Plugin Perl Module
* YAML Perl Module

## Installation

* Copy the check_puppet_run to your nagios plugin folder and set executable
* Add a line to your nrpe.cfg file

    command[check_puppet_run]=/usr/lib/nagios/plugins/check_puppet_run

* By default, the location of the state file is not readable by unprivileged users, add the following to your sudo config

    nagios    ALL=(ALL) NOPASSWD:/usr/lib/nagios/plugins/check_puppet_run


## Examples

* Run with the --help argument to see all options

    check_puppet_run --help

* Run a custom path to the Puppet statefile

    check_puppet_run --statefile=/path/to/puppet/statefile.yaml

* Run with longer timeout before reporting an error

    check_puppet_run --runtimeout=60

## Future Work

None planned

## Site 

https://github.com/alasdairkeyes/nagios-plugin-check_btc_miner

## Author

* Alasdair Keyes - https://akeyes.co.uk/

## License

Released under GPL V3 - See included license file.
