# 3.2.31 / 2021-11-08

## Enhancements:

* Don't pass empty `DESTDIR` to `nmake` since it works differently from
  standard `make`. Pull request #5057 by hsbt
* Fix `gem install` vs `gem fetch` inconsistency. Pull request #5037 by
  deivid-rodriguez
* Lazily load and vendor `optparse`. Pull request #4881 by
  deivid-rodriguez
* Use a vendored copy of `tsort` internally. Pull request #5027 by
  deivid-rodriguez
* Install bundler 2.2.31 as a default gem.

## Bug fixes:

* Fix `ruby setup.rb` when `--prefix` is passed. Pull request #5051 by
  deivid-rodriguez
* Don't apply `--destdir` twice when running `setup.rb`. Pull request
  #2768 by alyssais

# 3.2.30 / 2021-10-26

## Enhancements:

* Add support to build and sign certificates with multiple key algorithms.
  Pull request #4991 by doodzik
* Avoid loading the `digest` gem unnecessarily. Pull request #4979 by
  deivid-rodriguez
* Prefer `require_relative` for all internal requires. Pull request #4978
  by deivid-rodriguez
* Add missing `require` of `time` within
  `Gem::Request.verify_certificate_message`. Pull request #4975 by nobu
* Install bundler 2.2.30 as a default gem.

## Performance:

* Speed up `gem install`, specially under Windows. Pull request #4960 by
  deivid-rodriguez

# 3.2.29 / 2021-10-08

## Enhancements:

* Only disallow FIXME/TODO for first word of gemspec description. Pull
  request #4937 by duckinator
* Install bundler 2.2.29 as a default gem.

## Bug fixes:

* Fix `wordy` method in `SourceFetchProblem` changing the password of
  source. Pull request #4910 by Huangxiaodui

## Performance:

* Improve `require` performance, particularly on systems with a lot of
  gems installed. Pull request #4951 by pocke

# 3.2.28 / 2021-09-23

## Enhancements:

* Support MINGW-UCRT. Pull request #4925 by hsbt
* Only check if descriptions *start with* FIXME/TODO. Pull request #4841
  by duckinator
* Avoid loading `uri` unnecessarily when activating gems. Pull request
  #4897 by deivid-rodriguez
* Install bundler 2.2.28 as a default gem.

## Bug fixes:

* Fix redacted credentials being sent to gemserver. Pull request #4919 by
  jdliss

# 3.2.27 / 2021-09-03

## Enhancements:

* Redact credentails when printing URI. Pull request #4868 by intuxicated
* Prefer `require_relative` to `require` for internal requires. Pull
  request #4858 by deivid-rodriguez
* Prioritise gems with higher version for fetching metadata, and stop
  fetching once we find a valid candidate. Pull request #4843 by intuxicated
* Install bundler 2.2.27 as a default gem.

# 3.2.26 / 2021-08-17

## Enhancements:

* Enhance the error handling for loading the
  `rubygems/defaults/operating_system` file. Pull request #4824 by
  intuxicated
* Ignore `RUBYGEMS_GEMDEPS` for the bundler gem. Pull request #4532 by
  deivid-rodriguez
* Install bundler 2.2.26 as a default gem.

## Bug fixes:

* Also load user installed rubygems plugins. Pull request #4829 by
  deivid-rodriguez

# 3.2.25 / 2021-07-30

## Enhancements:

* Don't load the `base64` library since it's not used. Pull request #4785
  by deivid-rodriguez
* Don't load the `resolv` library since it's not used. Pull request #4784
  by deivid-rodriguez
* Lazily load `shellwords` library. Pull request #4783 by deivid-rodriguez
* Check requirements class before loading marshalled requirements. Pull
  request #4651 by nobu
* Install bundler 2.2.25 as a default gem.

## Bug fixes:

* Add missing `require 'fileutils'` in `Gem::ConfigFile`. Pull request
  #4768 by ybiquitous

# 3.2.24 / 2021-07-15

## Enhancements:

* Install bundler 2.2.24 as a default gem.

## Bug fixes:

* Fix contradictory message about deletion of default gem. Pull request
  #4739 by jaredbeck

## Documentation:

* Add a description about `GEM_HOST_OTP_CODE` to help text. Pull request
  #4742 by ybiquitous

# 3.2.23 / 2021-07-09

## Enhancements:

* Rewind IO source to allow working with contents in memory. Pull request
  #4729 by drcapulet
* Install bundler 2.2.23 as a default gem.

# 3.2.22 / 2021-07-06

## Enhancements:

* Allow setting `--otp` via `GEM_HOST_OTP_CODE`. Pull request #4697 by
  CGA1123
* Fixes for the edge case when openssl library is missing. Pull request
  #4695 by rhenium
* Install bundler 2.2.22 as a default gem.

# 3.2.21 / 2021-06-23

## Enhancements:

* Fix typo in OpenSSL detection. Pull request #4679 by osyoyu
* Add the most recent licenses from spdx.org. Pull request #4662 by nobu
* Simplify setup.rb code to allow installing rubygems from source on
  truffleruby 21.0 and 21.1. Pull request #4624 by deivid-rodriguez
* Install bundler 2.2.21 as a default gem.

## Bug fixes:

* Create credentials folder when setting API keys if not there yet. Pull
  request #4665 by deivid-rodriguez

# 3.2.20 / 2021-06-11

## Security fixes:

* Verify plaform before installing to avoid potential remote code
  execution. Pull request #4667 by sonalkr132

## Enhancements:

* Add better specification policy error description. Pull request #4658 by
  ceritium
* Install bundler 2.2.20 as a default gem.

# 3.2.19 / 2021-05-31

## Enhancements:

* Fix `gem help build` output format. Pull request #4613 by tnir
* Install bundler 2.2.19 as a default gem.

# 3.2.18 / 2021-05-25

## Enhancements:

* Don't leave temporary directory around when building extensions to
  improve build reproducibility. Pull request #4610 by baloo
* Install bundler 2.2.18 as a default gem.

# 3.2.17 / 2021-05-05

## Enhancements:

* Only print month & year in deprecation messages. Pull request #3085 by
  Schwad
* Make deprecate method support ruby3's keyword arguments. Pull request
  #4558 by mame
* Update the default bindir on macOS. Pull request #4524 by nobu
* Prefer File.open instead of Kernel#open. Pull request #4529 by mame
* Install bundler 2.2.17 as a default gem.

## Documentation:

* Fix usage messages to reflect the current POSIX-compatible behaviour.
  Pull request #4551 by graywolf-at-work

# 3.2.16 / 2021-04-08

## Enhancements:

* Install bundler 2.2.16 as a default gem.

## Bug fixes:

* Correctly handle symlinks. Pull request #2836 by voxik

# 3.2.15 / 2021-03-19

## Enhancements:

* Prevent downgrades to untested rubygems versions. Pull request #4460 by
  deivid-rodriguez
* Install bundler 2.2.15 as a default gem.

## Bug fixes:

* Fix missing require breaking `gem cert`. Pull request #4464 by lukehinds

# 3.2.14 / 2021-03-08

## Enhancements:

* Less wrapping of network errors. Pull request #4064 by deivid-rodriguez
* Install bundler 2.2.14 as a default gem.

## Bug fixes:

* Revert addition of support for `musl` variants to restore graceful
  fallback on Alpine. Pull request #4434 by deivid-rodriguez

# 3.2.13 / 2021-03-03

## Enhancements:

* Install bundler 2.2.13 as a default gem.

## Bug fixes:

* Support non-gnu libc linux platforms. Pull request #4082 by lloeki

# 3.2.12 / 2021-03-01

## Enhancements:

* Install bundler 2.2.12 as a default gem.

## Bug fixes:

* Restore the ability to manually install extension gems. Pull request
  #4384 by cfis

# 3.2.11 / 2021-02-17

## Enhancements:

* Optionally fallback to IPv4 when IPv6 is unreachable. Pull request #2662
  by sonalkr132
* Install bundler 2.2.11 as a default gem.

# 3.2.10 / 2021-02-15

## Enhancements:

* Install bundler 2.2.10 as a default gem.

## Documentation:

* Add a `gem push` example to `gem help`. Pull request #4373 by
  deivid-rodriguez
* Improve documentation for `required_ruby_version`. Pull request #4343 by
  AlexWayfer

# 3.2.9 / 2021-02-08

## Enhancements:

* Install bundler 2.2.9 as a default gem.

## Bug fixes:

* Fix error message when underscore selection can't find bundler. Pull
  request #4363 by deivid-rodriguez
* Fix `Gem::Specification.stubs_for` returning wrong named specs. Pull
  request #4356 by tompng
* Don't error out when activating a binstub unless necessary. Pull request
  #4351 by deivid-rodriguez
* Fix `gem outdated` incorrectly handling platform specific gems. Pull
  request #4248 by deivid-rodriguez

# 3.2.8 / 2021-02-02

## Enhancements:

* Install bundler 2.2.8 as a default gem.

## Bug fixes:

* Fix `gem install` crashing on gemspec with nil required_ruby_version.
  Pull request #4334 by pbernays

# 3.2.7 / 2021-01-26

## Enhancements:

* Install bundler 2.2.7 as a default gem.

## Bug fixes:

* Generate plugin wrappers with relative requires. Pull request #4317 by
  deivid-rodriguez

# 3.2.6 / 2021-01-18

## Enhancements:

* Fix `Gem::Platform#inspect` showing duplicate information. Pull request
  #4276 by deivid-rodriguez
* Install bundler 2.2.6 as a default gem.

## Bug fixes:

* Swallow any system call error in `ensure_gem_subdirs` to support jruby
  embedded paths. Pull request #4291 by kares
* Restore accepting custom make command with extra options as the `make`
  env variable. Pull request #4271 by terceiro

# 3.2.5 / 2021-01-11

## Enhancements:

* Install bundler 2.2.5 as a default gem.

## Bug fixes:

* Don't load more specs after the whole set of specs has been setup. Pull
  request #4262 by deivid-rodriguez
* Fix broken `bundler` executable after `gem update --system`. Pull
  request #4221 by deivid-rodriguez

# 3.2.4 / 2020-12-31

## Enhancements:

* Use a CHANGELOG in markdown for rubygems. Pull request #4168 by
  deivid-rodriguez
* Never spawn subshells when building extensions. Pull request #4190 by
  deivid-rodriguez
* Install bundler 2.2.4 as a default gem.

## Bug fixes:

* Fix fallback to the old index and installation from it not working. Pull
  request #4213 by deivid-rodriguez
* Fix installing from source on truffleruby. Pull request #4201 by
  deivid-rodriguez

# 3.2.3 / 2020-12-22

## Enhancements:

* Fix misspellings in default API key name. Pull request #4177 by hsbt
* Install bundler 2.2.3 as a default gem.

## Bug fixes:

* Respect `required_ruby_version` and `required_rubygems_version`
  constraints when looking for `gem install` candidates. Pull request #4110
  by deivid-rodriguez

# 3.2.2 / 2020-12-17

## Enhancements:

* Install bundler 2.2.2 as a default gem.

## Bug fixes:

* Fix issue where CLI commands making more than one request to
  rubygems.org needing an OTP code would crash or ask for the code twice.
  Pull request #4162 by sonalkr132
* Fix building rake extensions that require openssl. Pull request #4165 by
  deivid-rodriguez
* Fix `gem update --system` displaying too many changelog entries. Pull
  request #4145 by deivid-rodriguez

# 3.2.1 / 2020-12-14

## Enhancements:

* Added help message for gem i webrick in gem server command. Pull request
  #4117 by hsbt
* Install bundler 2.2.1 as a default gem.

## Bug fixes:

* Added the missing loading of fileutils same as load_specs. Pull request
  #4124 by hsbt
* Fix Resolver::APISet to always include prereleases when necessary. Pull
  request #4113 by deivid-rodriguez

# 3.2.0 / 2020-12-07

## Enhancements:

* Do not override Kernel#warn when there is no need. Pull request #4075 by
  eregon
* Update endpoint of gem signin command. Pull request #3840 by sonalkr132
* Omit deprecated commands from command help output. Pull request #4023 by
  landongrindheim
* Suggest alternatives in `gem query` deprecation. Pull request #4021 by
  landongrindheim
* Lazily load `time`, `cgi`, and `zlib`. Pull request #4010 by
  deivid-rodriguez
* Don't hit the network when installing dependencyless local gemspec. Pull
  request #3968 by deivid-rodriguez
* Add `--force` option to `gem sources` command. Pull request #3956 by
  andy-smith-msm
* Lazily load `openssl`. Pull request #3850 by deivid-rodriguez
* Pass more information when comparing platforms. Pull request #3817 by
  eregon
* Install bundler 2.2.0 as a default gem.

## Bug fixes:

* Use better owner & group for files in rubygems package. Pull request
  #4065 by deivid-rodriguez
* Improve gem build -C flag. Pull request #3983 by bronzdoc
* Handle unexpected behavior with URI#merge and subpaths missing trailing
  slashes. Pull request #3123 by drcapulet
* Add missing `fileutils` require in rubygems installer. Pull request
  #4036 by deivid-rodriguez
* Fix `--platform` option to `gem specification` being ignored. Pull
  request #4043 by deivid-rodriguez
* Expose `--no-minimal-deps` flag to install the latest version of
  dependencies. Pull request #4030 by deivid-rodriguez
* Fix "stack level too deep" error when overriding `Warning.warn`. Pull
  request #3987 by eregon
* Append '.gemspec' extension only when it is not present. Pull request
  #3988 by voxik
* Install to correct plugins dir when using `--build-root`. Pull request
  #3972 by deivid-rodriguez
* Fix `--build-root` flag under Windows. Pull request #3975 by
  deivid-rodriguez
* Fix `typo_squatting?` false positive for `rubygems.org` itself. Pull
  request #3951 by andy-smith-msm
* Make `--default` and `--install-dir` options to `gem install` play nice
  together. Pull request #3906 by deivid-rodriguez

## Deprecations:

* Deprecate server command. Pull request #3868 by bronzdoc

## Performance:

* Don't change ruby process CWD when building extensions. Pull request
  #3498 by deivid-rodriguez

# 3.2.0.rc.2 / 2020-10-08

## Enhancements:

* Make --dry-run flag consistent across rubygems commands. Pull request
  #3867 by bronzdoc
* Disallow downgrades to too old versions. Pull request #3566 by
  deivid-rodriguez
* Added `--platform` option to `build` command. Pull request #3079 by nobu
* Have "gem update --system" pass through the `--silent` flag. Pull
  request #3789 by duckinator
* Add writable check for cache dir. Pull request #3876 by xndcn
* Warn on duplicate dependency in a specification. Pull request #3864 by
  bronzdoc
* Fix indentation in `gem env`. Pull request #3861 by colby-swandale
* Let more exceptions flow. Pull request #3819 by deivid-rodriguez
* Ignore internal frames in RubyGems' Kernel#warn. Pull request #3810 by
  eregon

## Bug fixes:

* Add missing fileutils require. Pull request #3911 by deivid-rodriguez
* Fix false positive warning on Windows when PATH has
  `File::ALT_SEPARATOR`. Pull request #3829 by deivid-rodriguez
* Fix Kernel#warn override to handle backtrace location with nil path.
  Pull request #3852 by jeremyevans
* Don't format executables on `gem update --system`. Pull request #3811 by
  deivid-rodriguez
* `gem install --user` fails with `Gem::FilePermissionError` on the system
  plugins directory. Pull request #3804 by nobu

## Performance:

* Avoid duplicated generation of APISpecification objects. Pull request
  #3940 by mame
* Eval defaults with frozen_string_literal: true. Pull request #3847 by
  casperisfine
* Deduplicate the requirement operators in memory. Pull request #3846 by
  casperisfine
* Optimize Gem.already_loaded?. Pull request #3793 by casperisfine

# 3.2.0.rc.1 / 2020-07-04

## Enhancements:

* Test TruffleRuby in CI. Pull request #2797 by Benoit Daloze.
* Rework plugins system and speed up rubygems. Pull request #3108 by David
  Rodríguez.
* Specify explicit separator not to be affected by $;. Pull request #3424
  by Nobuyoshi Nakada.
* Enable `Layout/ExtraSpacing` cop. Pull request #3449 by David Rodríguez.
* Rollback gem deprecate. Pull request #3530 by Luis Sagastume.
* Normalize heredoc delimiters. Pull request #3533 by David Rodríguez.
* Log messages to stdout in `rake package`. Pull request #3632 by David
  Rodríguez.
* Remove explicit `psych` activation. Pull request #3636 by David
  Rodríguez.
* Delay `fileutils` loading to fix some warnings. Pull request #3637 by
  David Rodríguez.
* Make sure rubygems/package can be directly required reliably. Pull
  request #3670 by Luis Sagastume.
* Make sure `tmp` folder exists before calling `Dir.tmpdir`. Pull request
  #3711 by David Rodríguez.
* Add Gem.disable_system_update_message to disable gem update --system if
  needed. Pull request #3720 by Josef Šimánek.
* Tweaks to play nice with ruby-core setup. Pull request #3733 by David
  Rodríguez.
* Remove explicit require for auto-loaded constant. Pull request #3751 by
  Karol Bucek.
* Test files should not be included in spec.files. Pull request #3758 by
  Marc-André Lafortune.
* Remove TODO comment about warning on setting instead of pushing. Pull
  request #2823 by Luis Sagastume.
* Add deprecate command method. Pull request #2935 by Luis Sagastume.
* Simplify deprecate command method. Pull request #2974 by Luis Sagastume.
* Fix Gem::LOADED_SPECS_MUTEX handling for recursive locking. Pull request
  #2985 by MSP-Greg.
* Add `funding_uri ` metadata field to gemspec. Pull request #3060 by
  Colby Swandale.
* Updates to some old gem-signing docs. Pull request #3063 by Tieg
  Zaharia.
* Update the gem method for Gem::Installer. Pull request #3137 by Daniel
  Berger.
* Simplify initial gem help output. Pull request #3148 by Olivier Lacan.
* Resolve latest version via `gem contents`. Pull request #3149 by Dan
  Rice.
* Install suggestions. Pull request #3151 by Sophia Castellarin.
* Only rescue the errors we actually want to rescue. Pull request #3156 by
  David Rodríguez.

## Bug fixes:

* Accept not only /usr/bin/env but also /bin/env in some tests. Pull
  request #3422 by Yusuke Endoh.
* Skip a test that attempts to remove the current directory on Solaris.
  Pull request #3423 by Yusuke Endoh.
* Fix race condition on bundler's parallel installer. Pull request #3440
  by David Rodríguez.
* Fix platform comparison check in #contains_requirable_file?. Pull
  request #3495 by Benoit Daloze.
* Improve missing spec error. Pull request #3559 by Luis Sagastume.
* Fix hidden bundler template installation from rubygems updater. Pull
  request #3674 by David Rodríguez.
* Fix gem update --user-install. Pull request #2901 by Luis Sagastume.
* Correct conflict list when uninstallation is prevented. Pull request
  #2973 by David Rodríguez.
* Fix error when trying to find bundler with a deleted "working directo….
  Pull request #3090 by Luis Sagastume.
* Fix -I require priority. Pull request #3124 by David Rodríguez.
* Fix `ruby setup.rb` for new plugins layout. Pull request #3144 by David
  Rodríguez.

## Deprecations:

* Set deprecation warning on query command. Pull request #2967 by Luis
  Sagastume.

## Breaking changes:

* Remove ruby 1.8 leftovers. Pull request #3442 by David Rodríguez.
* Minitest cleanup. Pull request #3445 by David Rodríguez.
* Remove `builder` gem requirement for `gem regenerate_index`. Pull
  request #3552 by David Rodríguez.
* Remove modelines for consistency. Pull request #3714 by David Rodríguez.
* Stop using deprecated OpenSSL::Digest constants. Pull request #3763 by
  Bart de Water.
* Remove Gem module deprecated methods. Pull request #3101 by Luis
  Sagastume.
* Remove ubygems.rb. Pull request #3102 by Luis Sagastume.
* Remove Gem::Commands::QueryCommand. Pull request #3104 by Luis
  Sagastume.
* Remove dependency installer deprecated methods. Pull request #3106 by
  Luis Sagastume.
* Remove Gem::UserInteraction#debug method. Pull request #3107 by Luis
  Sagastume.
* Remove options from Gem::GemRunner.new. Pull request #3110 by Luis
  Sagastume.
* Remove deprecated Gem::RemoteFetcher#fetch_size. Pull request #3111 by
  Luis Sagastume.
* Remove source_exception from Gem::Exception. Pull request #3112 by Luis
  Sagastume.
* Requiring rubygems/source_specific_file is deprecated, remove it. Pull
  request #3114 by Luis Sagastume.

# 3.1.4 / 2020-06-03

## Enhancements:

* Deprecate rubyforge_project attribute only during build
  time. Pull request #3609 by Josef Šimánek.
* Update links. Pull request #3610 by Josef Šimánek.
* Run CI at 3.1 branch head as well. Pull request #3677 by Josef Šimánek.
* Remove failing ubuntu-rvm CI flow. Pull request #3611 by
  Josef Šimánek.

# 3.1.3 / 2020-05-05

## Enhancements:

* Resolver: require NameTuple before use. Pull request #3171 by Olle
  Jonsson.
* Use absolute paths with autoload. Pull request #3100 by David Rodríguez.
* Avoid changing $SOURCE_DATE_EPOCH. Pull request #3088 by Ellen Marie
  Dash.
* Use Bundler 2.1.4. Pull request #3072 by Hiroshi SHIBATA.
* Add tests to check if Gem.ruby_version works with ruby git master.
  Pull request #3049 by Yusuke Endoh.

## Bug fixes:

* Fix platform comparison check in #contains_requirable_file?. Pull
  request #3495 by Benoit Daloze.
* Improve gzip errors logging. Pull request #3485 by David Rodríguez.
* Fix incorrect `gem uninstall --all` message. Pull request #3483 by David
  Rodríguez.
* Fix incorrect bundler version being required. Pull request #3458 by
  David Rodríguez.
* Fix gem install from a gemdeps file with complex dependencies.
  Pull request #3054 by Luis Sagastume.

# 3.1.2 / 2019-12-20

## Enhancements:

* Restore non prompting `gem update --system` behavior. Pull request #3040
  by David Rodríguez.
* Show only release notes for new code installed. Pull request #3041 by
  David Rodríguez.
* Inform about installed `bundle` executable after `gem update --system`.
  Pull request #3042 by David Rodríguez.
* Use Bundler 2.1.2. Pull request #3043 by SHIBATA Hiroshi.

## Bug fixes:

* Require `uri` in source.rb. Pull request #3034 by mihaibuzgau.
* Fix `gem update --system --force`. Pull request #3035 by David
  Rodríguez.
* Move `require uri` to source_list. Pull request #3038 by mihaibuzgau.

# 3.1.1 / 2019-12-16

## Bug fixes:

* Vendor Bundler 2.1.0 again. The version of Bundler with
  RubyGems 3.1.0 was Bundler 2.1.0.pre.3. Pull request #3029 by
  SHIBATA Hiroshi.

# 3.1.0 / 2019-12-16

## Enhancements:

* Vendor bundler 2.1. Pull request #3028 by David Rodríguez.
* Check for rubygems.org typo squatting sources. Pull request #2999 by
  Luis Sagastume.
* Refactor remote fetcher. Pull request #3017 by David Rodríguez.
* Lazily load `open3`. Pull request #3001 by David Rodríguez.
* Remove `delegate` dependency. Pull request #3002 by David Rodríguez.
* Lazily load `uri`. Pull request #3005 by David Rodríguez.
* Lazily load `rubygems/gem_runner` during tests. Pull request #3009 by
  David Rodríguez.
* Use bundler to manage development dependencies. Pull request #3012 by
  David Rodríguez.

## Bug fixes:

* Remove unnecessary executable flags. Pull request #2982 by David
  Rodríguez.
* Remove configuration that contained a typo. Pull request #2989 by David
  Rodríguez.

## Deprecations:

* Deprecate `gem generate_index --modern` and `gem generate_index
  --no-modern`. Pull request #2992 by David Rodríguez.

## Breaking changes:

* Remove 1.8.7 leftovers. Pull request #2972 by David Rodríguez.

# 3.1.0.pre3 / 2019-11-11

## Enhancements:

* Fix gem pristine not accounting for user installed gems. Pull request
  #2914 by Luis Sagastume.
* Refactor keyword argument test for Ruby 2.7. Pull request #2947 by
  SHIBATA Hiroshi.
* Fix errors at frozen Gem::Version. Pull request #2949 by Nobuyoshi
  Nakada.
* Remove taint usage on Ruby 2.7+. Pull request #2951 by Jeremy Evans.
* Check Manifest.txt is up to date. Pull request #2953 by David Rodríguez.
* Clarify symlink conditionals in tests. Pull request #2962 by David
  Rodríguez.
* Update command line parsing to work under ps. Pull request #2966 by
  David Rodríguez.
* Properly test `Gem::Specifications.stub_for`. Pull request #2970 by
  David Rodríguez.
* Fix Gem::LOADED_SPECS_MUTEX handling for recursive locking. Pull request
  #2985 by MSP-Greg.

# 3.1.0.pre2 / 2019-10-15

## Enhancements:

* Optimize Gem::Package::TarReader#each. Pull request #2941 by Jean byroot
  Boussier.
* Time comparison around date boundary. Pull request #2944 by Nobuyoshi
  Nakada.

# 3.1.0.pre1 / 2019-10-08

## Enhancements:

* Try to use bundler-2.1.0.pre.2. Pull request #2923 by SHIBATA Hiroshi.
* [Require] Ensure -I beats a default gem. Pull request #1868 by Samuel
  Giddins.
* [Specification] Prefer user-installed gems to default gems. Pull request
  #2112 by Samuel Giddins.
* Multifactor authentication for yank command. Pull request #2514 by Qiu
  Chaofan.
* Autoswitch to exact bundler version if present. Pull request #2583 by
  David Rodríguez.
* Fix Gem::Requirement equality comparison when ~> operator is used. Pull
  request #2554 by Grey Baker.
* Don't use a proxy if https_proxy env var is empty. Pull request #2567 by
  Luis Sagastume.
* Fix typo in specs warning. Pull request #2585 by Rui.
* Bin/gem: remove initial empty line. Pull request #2602 by Kenyon Ralph.
* Avoid rdoc hook when it's failed to load rdoc library. Pull request
  #2604 by SHIBATA Hiroshi.
* Refactor get_proxy_from_env logic. Pull request #2611 by Luis Sagastume.
* Allow to easily bisect flaky failures. Pull request #2626 by David
  Rodríguez.
* Fix `--ignore-dependencies` flag not installing platform specific gems.
  Pull request #2631 by David Rodríguez.
* Make `gem install --explain` list platforms. Pull request #2634 by David
  Rodríguez.
* Make `gem update --explain` list platforms. Pull request #2635 by David
  Rodríguez.
* Refactoring install and update explanations. Pull request #2643 by David
  Rodríguez.
* Restore transitiveness of version comparison. Pull request #2651 by
  David Rodríguez.
* Undo requirement sorting. Pull request #2652 by David Rodríguez.
* Update dummy version of Bundler for #2581. Pull request #2584 by SHIBATA
  Hiroshi.
* Ignore to handle the different platform. Pull request #2672 by SHIBATA
  Hiroshi.
* Make Gem::Specification.default_stubs to public methods. Pull request
  #2675 by SHIBATA Hiroshi.
* Sort files and test_files in specifications. Pull request #2524 by
  Christopher Baines.
* Fix comment of Gem::Specification#required_ruby_version=. Pull request
  #2732 by Alex Junger.
* Config_file.rb - update path separator in ENV['GEMRC'] logic. Pull
  request #2735 by MSP-Greg.
* Fix `ruby setup.rb` warnings. Pull request #2737 by David Rodríguez.
* Don't use regex delimiters when searching for a dependency. Pull request
  #2738 by Luis Sagastume.
* Refactor query command. Pull request #2739 by Luis Sagastume.
* Don't remove default spec files from mapping after require. Pull request
  #2741 by David Rodríguez.
* Cleanup base test case. Pull request #2742 by David Rodríguez.
* Simplify Specification#gems_dir. Pull request #2745 by David Rodríguez.
* Fix test warning. Pull request #2746 by David Rodríguez.
* Extract an `add_to_load_path` method. Pull request #2749 by David
  Rodríguez.
* Fix setup command if format_executable is true by default. Pull request
  #2766 by Jeremy Evans.
* Update the certificate files to make the test pass on Debian 10. Pull
  request #2777 by Yusuke Endoh.
* Write to the correct config file(.gemrc). Pull request #2779 by Luis
  Sagastume.
* Fix for large values in UID/GID fields in tar archives. Pull request
  #2780 by Alexey Shein.
* Lazy require stringio. Pull request #2781 by Luis Sagastume.
* Make Gem::Specification#ruby_code handle OpenSSL::PKey::RSA objects.
  Pull request #2782 by Luis Sagastume.
* Fix setup command test for bundler with program_suffix. Pull request
  #2783 by Sorah Fukumori.
* Make sure `rake package` works. Pull request #2787 by David Rodríguez.
* Synchronize access to the Gem::Specification::LOAD_CACHE Hash. Pull
  request #2789 by Benoit Daloze.
* Task to install rubygems to local system. Pull request #2795 by David
  Rodríguez.
* Add an attr_reader to Gem::Installer for the package instance variable.
  Pull request #2796 by Daniel Berger.
* Switch CI script to bash. Pull request #2799 by David Rodríguez.
* Move gemcutter utilities code to Gem::Command. Pull request #2803 by
  Luis Sagastume.
* Add raw spec method to gem package. Pull request #2806 by Luis
  Sagastume.
* Improve `rake package` test error message. Pull request #2815 by David
  Rodríguez.
* Resolve `@@project_dir` from test file paths. Pull request #2843 by
  Nobuyoshi Nakada.
* Remove dead code in Gem::Validator. Pull request #2537 by Ellen Marie
  Dash.
* The date might have advanced since TODAY has been set. Pull request
  #2938 by Nobuyoshi Nakada.
* Remove old ci configurations. Pull request #2917 by SHIBATA Hiroshi.
* Add Gem::Dependency identity. Pull request #2936 by Luis Sagastume.
* Filter dependency type and name strictly. Pull request #2930 by SHIBATA
  Hiroshi.
* Always pass an encoding option to Zlib::GzipReader.wrap. Pull request
  #2933 by Nobuyoshi Nakada.
* Introduce default prerelease requirement. Pull request #2925 by David
  Rodríguez.
* Detect libc version, closes #2918. Pull request #2922 by fauno.
* Use IAM role to extract security-credentials for EC2 instance. Pull
  request #2894 by Alexander Pakulov.
* Improve `gem uninstall --all`. Pull request #2893 by David Rodríguez.
* Use `RbConfig::CONFIG['rubylibprefix']`. Pull request #2889 by Nobuyoshi
  Nakada.
* Build the first gemspec we found if no arguments are passed to gem
  build. Pull request #2887 by Luis Sagastume.
* $LOAD_PATH elements should be real paths. Pull request #2885 by
  Nobuyoshi Nakada.
* Use the standard RUBY_ENGINE_VERSION instead of JRUBY_VERSION. Pull
  request #2864 by Benoit Daloze.
* Cleanup after testing `rake package`. Pull request #2862 by David
  Rodríguez.
* Cherry-pick shushing deprecation warnings from ruby-core. Pull request
  #2861 by David Rodríguez.
* Ext/builder.rb cleanup. Pull request #2849 by Luis Sagastume.
* Fix @ran_rake assignment in builder.rb. Pull request #2850 by Luis
  Sagastume.
* Remove test suite warnings. Pull request #2845 by Luis Sagastume.
* Replace domain parameter with a parameter to suppress suggestions. Pull
  request #2846 by Luis Sagastume.
* Move default specifications dir definition out of BasicSpecification.
  Pull request #2841 by Vít Ondruch.
* There is no usage of @orig_env_* variables in test suite. Pull request
  #2838 by SHIBATA Hiroshi.
* Use File#open instead of Kernel#open in stub_specification.rb. Pull
  request #2834 by Luis Sagastume.
* Simplify #to_ruby code. Pull request #2825 by Nobuyoshi Nakada.
* Add a gem attr to the Gem::Package class. Pull request #2828 by Daniel
  Berger.
* Remove useless TODO comment. Pull request #2818 by Luis Sagastume.

## Bug fixes:

* Fix typos in History.txt. Pull request #2565 by Igor Zubkov.
* Remove unused empty sources array. Pull request #2598 by Aaron
  Patterson.
* Fix windows specific executables generated by `gem install`. Pull
  request #2628 by David Rodríguez.
* Gem::Specification#to_ruby needs OpenSSL. Pull request #2937 by
  Nobuyoshi Nakada.
* Set SOURCE_DATE_EPOCH env var if not provided. Pull request #2882 by
  Ellen Marie Dash.
* Installer.rb - fix #windows_stub_script. Pull request #2876 by MSP-Greg.
* Fixed deprecation message. Pull request #2867 by Nobuyoshi Nakada.
* Fix requiring default gems to consider prereleases. Pull request #2728
  by David Rodríguez.
* Forbid `find_spec_for_exe` without an `exec_name`. Pull request #2706 by
  David Rodríguez.
* Do not prompt for passphrase when key can be loaded without it. Pull
  request #2710 by Luis Sagastume.
* Add missing wrapper. Pull request #2690 by David Rodríguez.
* Remove long ago deprecated methods. Pull request #2704 by David
  Rodríguez.
* Renamed duplicate test. Pull request #2678 by Nobuyoshi Nakada.
* File.exists? is deprecated. Pull request #2855 by SHIBATA Hiroshi.
* Fixed to warn with shadowing outer local variable. Pull request #2856 by
  SHIBATA Hiroshi.
* Fix explain with ignore-dependencies. Pull request #2647 by David
  Rodríguez.
* Fix default gem executable installation when folder is not `bin/`. Pull
  request #2649 by David Rodríguez.
* Fix cryptic error on local and ignore-dependencies combination. Pull
  request #2650 by David Rodríguez.

## Deprecations:

* Make deprecate Gem::RubyGemsVersion and Gem::ConfigMap. Pull request
  #2857 by SHIBATA Hiroshi.
* Deprecate Gem::RemoteFetcher#fetch_size. Pull request #2833 by Luis
  Sagastume.
* Explicitly deprecate `rubyforge_project`. Pull request #2798 by David
  Rodríguez.
* Deprecate unused Gem::Installer#unpack method. Pull request #2715 by Vít
  Ondruch.
* Deprecate a few unused methods. Pull request #2674 by David Rodríguez.
* Add deprecation warnings for cli options. Pull request #2607 by Luis
  Sagastume.

## Breaking changes:

* Suppress keywords warning. Pull request #2934 by Nobuyoshi Nakada.
* Suppress Ruby 2.7's real kwargs warning. Pull request #2912 by Koichi
  ITO.
* Fix Kernel#warn override. Pull request #2911 by Jeremy Evans.
* Remove conflict.rb code that was supposed to be removed in Rubygems 3.
  Pull request #2802 by Luis Sagastume.
* Compatibility cleanups. Pull request #2754 by David Rodríguez.
* Remove `others_possible` activation request param. Pull request #2747 by
  David Rodríguez.
* Remove dependency installer deprecated code. Pull request #2740 by Luis
  Sagastume.
* Removed guard condition with USE_BUNDLER_FOR_GEMDEPS. Pull request #2716
  by SHIBATA Hiroshi.
* Skip deprecation warning during specs. Pull request #2718 by David
  Rodríguez.
* Remove QuickLoader reference. Pull request #2719 by David Rodríguez.
* Removed circular require. Pull request #2679 by Nobuyoshi Nakada.
* Removed needless environmental variable for Travis CI. Pull request
  #2685 by SHIBATA Hiroshi.
* Removing yaml require. Pull request #2538 by Luciano Sousa.

# 3.0.8 / 2020-02-19

## Bug fixes:

* Gem::Specification#to_ruby needs OpenSSL. Pull request #2937 by
  Nobuyoshi Nakada.

# 3.0.7 / 2020-02-18

## Bug fixes:

* Fix underscore version selection for bundler #2908 by David Rodríguez.
* Add missing wrapper. Pull request #2690 by David Rodríguez.
* Make Gem::Specification#ruby_code handle OpenSSL::PKey::RSA objects.
  Pull request #2782 by Luis Sagastume.
* Installer.rb - fix #windows_stub_script. Pull request #2876 by MSP-Greg.
* Use IAM role to extract security-credentials for EC2 instance. Pull
  request #2894 by Alexander Pakulov.

# 3.0.6 / 2019-08-17

## Bug fixes:

* Revert #2813. It broke the compatibility with 3.0.x versions.

# 3.0.5 / 2019-08-16

## Enhancements:

* Use env var to configure api key on push. Pull request #2559 by Luis
  Sagastume.
* Unswallow uninstall error. Pull request #2707 by David Rodríguez.
* Expose windows path normalization utility. Pull request #2767 by David
  Rodríguez.
* Clean which command. Pull request #2801 by Luis Sagastume.
* Upgrading S3 source signature to AWS SigV4. Pull request #2807 by
  Alexander Pakulov.
* Remove misleading comment, no reason to move Gem.host to Gem::Util.
  Pull request #2811 by Luis Sagastume.
* Drop support for 'gem env packageversion'. Pull request #2813 by Luis
  Sagastume.
* Take into account just git tracked files in update_manifest rake task.
  Pull request #2816 by Luis Sagastume.
* Remove TODO comment, there's no Gem::Dirs constant. Pull request #2819
  by Luis Sagastume.
* Remove unused 'raise' from test_case. Pull request #2820 by Luis
  Sagastume.
* Move TODO comment to an information comment. Pull request #2821 by Luis
  Sagastume.
* Use File#open instead of Kernel#open in stub_specification.rb. Pull
  request #2834 by Luis Sagastume.
* Make error code a gemcutter_utilities a constant. Pull request #2844 by
  Luis Sagastume.
* Remove FIXME comment related to PathSupport. Pull request #2854 by Luis
  Sagastume.
* Use gsub with Hash. Pull request #2860 by Kazuhiro NISHIYAMA.
* Use the standard RUBY_ENGINE_VERSION instead of JRUBY_VERSION. Pull
  request #2864 by Benoit Daloze.
* Do not mutate uri.query during s3 signature creation. Pull request #2874
  by Alexander Pakulov.
* Fixup #2844. Pull request #2878 by SHIBATA Hiroshi.

## Bug fixes:

* Fix intermittent test error on Appveyor & Travis. Pull request #2568 by
  MSP-Greg.
* Extend timeout on assert_self_install_permissions. Pull request #2605 by
  SHIBATA Hiroshi.
* Better folder assertions. Pull request #2644 by David Rodríguez.
* Fix default gem executable installation when folder is not `bin/`. Pull
  request #2649 by David Rodríguez.
* Fix gem uninstall behavior. Pull request #2663 by Luis Sagastume.
* Fix for large values in UID/GID fields in tar archives. Pull request
  #2780 by Alexey Shein.
* Fixed task order for release. Pull request #2792 by SHIBATA Hiroshi.
* Ignore GEMRC variable for test suite. Pull request #2837 by SHIBATA
  Hiroshi.

# 3.0.4 / 2019-06-14

## Enhancements:

* Add support for TruffleRuby #2612 by Benoit Daloze
* Serve a more descriptive error when --no-ri or --no-rdoc are used #2572
  by Grey Baker
* Improve test compatibility with CMake 2.8. Pull request #2590 by Vít
  Ondruch.
* Restore gem build behavior and introduce the "-C" flag to gem build.
  Pull request #2596 by Luis Sagastume.
* Enabled block call with util_set_arch. Pull request #2603 by SHIBATA
  Hiroshi.
* Avoid rdoc hook when it's failed to load rdoc library. Pull request
  #2604 by SHIBATA Hiroshi.
* Drop tests for legacy RDoc. Pull request #2608 by Nobuyoshi Nakada.
* Update TODO comment. Pull request #2658 by Luis Sagastume.
* Skip malicious extension test with mswin platform. Pull request #2670 by
  SHIBATA Hiroshi.
* Check deprecated methods on release. Pull request #2673 by David
  Rodríguez.
* Add steps to run bundler tests. Pull request #2680 by Aditya Prakash.
* Skip temporary "No such host is known" error. Pull request #2684 by
  Takashi Kokubun.
* Replaced aws-sdk-s3 instead of s3cmd. Pull request #2688 by SHIBATA
  Hiroshi.
* Allow uninstall from symlinked GEM_HOME. Pull request #2720 by David
  Rodríguez.
* Use current checkout in CI to uninstall RVM related gems. Pull request
  #2729 by David Rodríguez.
* Update Contributor Covenant v1.4.1. Pull request #2751 by SHIBATA
  Hiroshi.
* Added supported versions of Ruby. Pull request #2756 by SHIBATA Hiroshi.
* Fix shadowing outer local variable warning. Pull request #2763 by Luis
  Sagastume.
* Update the certificate files to make the test pass on Debian 10. Pull
  request #2777 by Yusuke Endoh.
* Backport ruby core changes. Pull request #2778 by SHIBATA Hiroshi.

## Bug fixes:

* Test_gem.rb - intermittent failure fix. Pull request #2613 by MSP-Greg.
* Fix sporadic CI failures. Pull request #2617 by David Rodríguez.
* Fix flaky bundler version finder tests. Pull request #2624 by David
  Rodríguez.
* Fix gem indexer tests leaking utility gems. Pull request #2625 by David
  Rodríguez.
* Clean up default spec dir too. Pull request #2639 by David Rodríguez.
* Fix 2.6.1 build against vendored bundler. Pull request #2645 by David
  Rodríguez.
* Fix comment typo. Pull request #2664 by Luis Sagastume.
* Fix comment of Gem::Specification#required_ruby_version=. Pull request
  #2732 by Alex Junger.
* Fix TODOs. Pull request #2748 by David Rodríguez.

# 3.0.3 / 2019-03-05

Security fixes:

  * CVE-2019-8320: Delete directory using symlink when decompressing tar
  * CVE-2019-8321: Escape sequence injection vulnerability in `verbose`
  * CVE-2019-8322: Escape sequence injection vulnerability in `gem owner`
  * CVE-2019-8323: Escape sequence injection vulnerability in API response handling
  * CVE-2019-8324: Installing a malicious gem may lead to arbitrary code execution
  * CVE-2019-8325: Escape sequence injection vulnerability in errors

# 3.0.2 / 2019-01-01

## Enhancements:

* Use Bundler-1.17.3. Pull request #2556 by SHIBATA Hiroshi.
* Fix document flag description. Pull request #2555 by Luis Sagastume.

## Bug fixes:

* Fix tests when ruby --program-suffix is used without rubygems
  --format-executable. Pull request #2549 by Jeremy Evans.
* Fix Gem::Requirement equality comparison when ~> operator is used. Pull
  request #2554 by Grey Baker.
* Unset SOURCE_DATE_EPOCH in the test cases. Pull request #2558 by Sorah
  Fukumori.
* Restore SOURCE_DATE_EPOCH. Pull request #2560 by SHIBATA Hiroshi.

# 3.0.1 / 2018-12-23

## Bug fixes:

* Ensure globbed files paths are expanded. Pull request #2536 by Tony Ta.
* Dup the Dir.home string before passing it on. Pull request #2545 by
  Charles Oliver Nutter.
* Added permissions to installed files for non-owners. Pull request #2546
  by SHIBATA Hiroshi.
* Restore release task without hoe. Pull request #2547 by SHIBATA Hiroshi.

# 3.0.0 / 2018-12-19

## Enhancements:

* S3 source. Pull request #1690 by Aditya Prakash.
* Download gems with threads. Pull request #1898 by André Arko.
* Update to SPDX license list 3.0. Pull request #2152 by Mike Linksvayer.
* [GSoC] Multi-factor feature for RubyGems. Pull request #2369 by Qiu
  Chaofan.
* Use bundler 1.17.2. Pull request #2521 by SHIBATA Hiroshi.
* Don't treat inaccessible working directories as build failures. Pull
  request #1135 by Pete.
* Remove useless directory parameter from builders .build methods.
  [rebased]. Pull request #1433 by Kurtis Rainbolt-Greene.
* Skipping more than one gem in pristine. Pull request #1592 by Henne
  Vogelsang.
* Add info command to print information about an installed gem. Pull
  request #2023 by Colby Swandale.
* Add --[no-]check-development option to cleanup command. Pull request
  #2061 by Lin Jen-Shin (godfat).
* Show which gem referenced a missing gem. Pull request #2067 by Artem
  Khramov.
* Prevent to delete to "bundler-" prefix gem like bundler-audit. Pull
  request #2086 by SHIBATA Hiroshi.
* Fix rake install_test_deps once the rake clean_env does not exist. Pull
  request #2090 by Lucas Arantes.
* Workaround common options mutation in Gem::Command test. Pull request
  #2098 by Thibault Jouan.
* Extract a SpecificationPolicy validation class. Pull request #2101 by
  Olle Jonsson.
* Handle environment that does not have `flock` system call. Pull request
  #2107 by SHIBATA Hiroshi.
* Handle the explain option in gem update. Pull request #2110 by Colby
  Swandale.
* Add Gem.operating_system_defaults to allow packagers to override
  defaults. Pull request #2116 by Vít Ondruch.
* Update for compatibility with new minitest. Pull request #2118 by
  MSP-Greg.
* Make Windows bin stubs portable. Pull request #2119 by MSP-Greg.
* Avoid to warnings about gemspec loadings in rubygems tests. Pull request
  #2125 by SHIBATA Hiroshi.
* Set whether bundler is used for gemdeps with an environmental variable.
  Pull request #2126 by SHIBATA Hiroshi.
* Titleize "GETTING HELP" in readme. Pull request #2136 by Colby Swandale.
* Improve the error message given when using --version with multiple gems
  in the install command. Pull request #2137 by Colby Swandale.
* Use `File.open` instead of `open`. Pull request #2142 by SHIBATA
  Hiroshi.
* Gem::Util.traverse_parents should not crash on permissions error. Pull
  request #2147 by Robert Ulejczyk.
* [Installer] Avoid a #mkdir race condition. Pull request #2148 by Samuel
  Giddins.
* Allow writing gemspecs from gem unpack to location specified by target
  option. Pull request #2150 by Colby Swandale.
* Raise errors in `gem uninstall` when a file in a gem could not be
  removed . Pull request #2154 by Colby Swandale.
* Remove PID from gem index directory. Pull request #2155 by SHIBATA
  Hiroshi.
* Nil guard on `Gem::Specification`. Pull request #2164 by SHIBATA
  Hiroshi.
* Skip broken test with macOS platform. Pull request #2167 by SHIBATA
  Hiroshi.
* Support option for `--destdir` with upgrade installer. Pull request
  #2169 by SHIBATA Hiroshi.
* To use constant instead of hard-coded version. Pull request #2171 by
  SHIBATA Hiroshi.
* Add Rake task to install dev dependencies. Pull request #2173 by Ellen
  Marie Dash.
* Add new sections to the README and explanation of what RubyGems is.
  Pull request #2174 by Colby Swandale.
* Prefer to use `Numeric#zero?` instead of `== 0`. Pull request #2176 by
  SHIBATA Hiroshi.
* Ignore performance test of version regexp pattern. Pull request #2179 by
  SHIBATA Hiroshi.
* Ignore .DS_Store files in the update_manifest task. Pull request #2199
  by Colby Swandale.
* Allow building gems without having to be in the gem folder . Pull
  request #2204 by Colby Swandale.
* Added coverage ability used by simplecov. Pull request #2207 by SHIBATA
  Hiroshi.
* Improve invalid proxy error message. Pull request #2217 by Luis
  Sagastume.
* Simplify home directory detection and platform condition. Pull request
  #2218 by SHIBATA Hiroshi.
* Permission options. Pull request #2219 by Nobuyoshi Nakada.
* Improve gemspec and package task. Pull request #2220 by SHIBATA Hiroshi.
* Prefer to use util_spec in `Gem::TestCase`. Pull request #2227 by
  SHIBATA Hiroshi.
*  [Requirement] Treat requirements with == versions as equal. Pull
  request #2230 by Samuel Giddins.
* Add a note for the non-semantically versioned case. Pull request #2242
  by David Rodríguez.
* Keep feature names loaded in the block. Pull request #2261 by Nobuyoshi
  Nakada.
* Tweak warning recommendation. Pull request #2266 by David Rodríguez.
* Show git path in gem env. Pull request #2268 by Luis Sagastume.
* Add `--env-shebang` flag to setup command. Pull request #2271 by James
  Myers.
* Support SOURCE_DATE_EPOCH to make gem spec reproducible. Pull request
  #2278 by Levente Polyak.
* Chdir back to original directory when building an extension fails. Pull
  request #2282 by Samuel Giddins.
* [Rakefile] Add a default task that runs the tests. Pull request #2283 by
  Samuel Giddins.
* Support SOURCE_DATE_EPOCH to make gem tar reproducible. Pull request
  #2289 by Levente Polyak.
* Reset hooks in test cases. Pull request #2297 by Samuel Giddins.
* Minor typo: nokogiri. Pull request #2298 by Darshan Baid.
* Ignore vendored molinillo from code coverage. Pull request #2302 by
  SHIBATA Hiroshi.
* Support IO.copy_stream. Pull request #2303 by okkez.
* Prepare beta release. Pull request #2304 by SHIBATA Hiroshi.
* Add error message when trying to open a default gem. Pull request #2307
  by Luis Sagastume.
* Add alias command 'i' for 'install' command. Pull request #2308 by
  ota42y.
* Cleanup rdoc task in Rakefile. Pull request #2318 by SHIBATA Hiroshi.
* Add testcase to test_gem_text.rb. Pull request #2329 by Oliver.
* Gem build strict option. Pull request #2332 by David Rodríguez.
* Make spec reset more informative. Pull request #2333 by Luis Sagastume.
* [Rakefile] Set bundler build metadata when doing a release. Pull request
  #2335 by Samuel Giddins.
* Speed up globbing relative to given directories. Pull request #2336 by
  Samuel Giddins.
* Remove semver gem build warning. Pull request #2351 by David Rodríguez.
* Expand symlinks in gem path. Pull request #2352 by Benoit Daloze.
* Normalize comment indentations. Pull request #2353 by David Rodríguez.
* Add bindir flag to pristine. Pull request #2361 by Luis Sagastume.
* Add --user-install behaviour to cleanup command. Pull request #2362 by
  Luis Sagastume.
* Allow build options to be passed to Rake. Pull request #2382 by Alyssa
  Ross.
* Add --re-sign flag to cert command. Pull request #2391 by Luis
  Sagastume.
* Fix "interpreted as grouped expression" warning. Pull request #2399 by
  Colby Swandale.
* [Gem::Ext::Builder] Comments to aid future refactoring. Pull request
  #2405 by Ellen Marie Dash.
* Move CONTRIBUTING.rdoc and POLICIES.rdoc documents to markdown. Pull
  request #2412 by Colby Swandale.
* Improve certificate expiration defaults. Pull request #2420 by Luis
  Sagastume.
* Freeze all possible constants. Pull request #2422 by Colby Swandale.
* Fix bundler rubygems binstub not properly looking for bundler. Pull
  request #2426 by David Rodríguez.
* Make sure rubygems never leaks to another installation. Pull request
  #2427 by David Rodríguez.
* Update README.md. Pull request #2428 by Marc-André Lafortune.
* Restrict special chars from prefixing new gem names. Pull request #2432
  by Luis Sagastume.
* This removes support for dynamic API backend lookup via DNS SRV records.
  Pull request #2433 by Arlandis Word.
* Fix link to CONTRIBUTING.md doc. Pull request #2434 by Arlandis Word.
* Support Keyword args with Psych. Pull request #2439 by SHIBATA Hiroshi.
* Bug/kernel#warn uplevel. Pull request #2442 by Nobuyoshi Nakada.
* Improve certificate error message. Pull request #2454 by Luis Sagastume.
* Update gem open command help text. Pull request #2458 by Aditya Prakash.
* Uninstall with versions. Pull request #2466 by David Rodríguez.
* Add output option to build command. Pull request #2501 by Colby
  Swandale.
* Move rubocop into a separate stage in travis ci. Pull request #2510 by
  Colby Swandale.
* Ignore warnings with test_gem_specification.rb. Pull request #2523 by
  SHIBATA Hiroshi.
* Support the environment without OpenSSL. Pull request #2528 by SHIBATA
  Hiroshi.

## Bug fixes:

* Fix undefined method error when printing alert. Pull request #1884 by
  Robert Ross.
* Frozen string fix - lib/rubygems/bundler_version_finder.rb. Pull request
  #2115 by MSP-Greg.
* Fixed typos. Pull request #2143 by SHIBATA Hiroshi.
* Fix regression of destdir on Windows platform. Pull request #2178 by
  SHIBATA Hiroshi.
* Fixed no assignment variables about default gems installation. Pull
  request #2181 by SHIBATA Hiroshi.
* Fix spelling errors in the README. Pull request #2187 by Colby Swandale.
* Missing comma creates ambiguous meaning. Pull request #2190 by Clifford
  Heath.
* Fix getting started instructions. Pull request #2198 by Luis Sagastume.
* Fix rubygems dev env. Pull request #2201 by Luis Sagastume.
* Fix #1470: generate documentation when --install-dir is present. Pull
  request #2229 by Elias Hernandis.
* Fix activation when multiple platforms installed. Pull request #2339 by
  MSP-Greg.
* Fix required_ruby_version with prereleases and improve error message.
  Pull request #2344 by David Rodríguez.
* Update tests for 'newer' Windows builds. Pull request #2348 by MSP-Greg.
* Fix broken rubocop task by upgrading to 0.58.1. Pull request #2356 by
  David Rodríguez.
* Gem::Version should handle nil like it used to before. Pull request
  #2363 by Luis Sagastume.
* Avoid need of C++ compiler to pass the test suite. Pull request #2367 by
  Vít Ondruch.
* Fix auto resign expired certificate. Pull request #2380 by Luis
  Sagastume.
* Skip permissions-dependent test when root. Pull request #2386 by Alyssa
  Ross.
* Fix test that depended on /usr/bin being in PATH. Pull request #2387 by
  Alyssa Ross.
* Fixed test fail with mswin environment. Pull request #2390 by SHIBATA
  Hiroshi.
* Fix broken builds using the correct rubocop version. Pull request #2396
  by Luis Sagastume.
* Fix extension builder failure when verbose. Pull request #2457 by Sorah
  Fukumori.
* Fix test warnings. Pull request #2472 by MSP-Greg.
* The test suite of bundler is not present ruby description. Pull request
  #2484 by SHIBATA Hiroshi.
* Fix crash on certain gemspecs. Pull request #2506 by David Rodríguez.
* Fixed test fails with the newer version of OpenSSL. Pull request #2507
  by SHIBATA Hiroshi.
* Fix broken symlink that points to ../*. Pull request #2516 by Akira
  Matsuda.
* Fix remote fetcher tests. Pull request #2520 by Luis Sagastume.
* Fix tests when --program-suffix and similar ruby configure options are
  used. Pull request #2529 by Jeremy Evans.

## Breaking changes:

* IO.binread is not provided at Ruby 1.8. Pull request #2093 by SHIBATA
  Hiroshi.
* Ignored to publish rdoc documentation of rubygems for
  docs.seattlerb.org. Pull request #2105 by SHIBATA Hiroshi.
* Support pre-release RubyGems. Pull request #2128 by SHIBATA Hiroshi.
* Relax minitest version for 5. Pull request #2131 by SHIBATA Hiroshi.
* Remove zentest from dev dependency. Pull request #2132 by SHIBATA
  Hiroshi.
* Remove hoe for test suite. Pull request #2160 by SHIBATA Hiroshi.
* Cleanup deprecated tasks. Pull request #2162 by SHIBATA Hiroshi.
* Drop to support Ruby < 2.2. Pull request #2182 by SHIBATA Hiroshi.
* Cleanup deprecated style. Pull request #2193 by SHIBATA Hiroshi.
* Remove CVEs from the rubygems repo. Pull request #2195 by Colby
  Swandale.
* Removed needless condition for old version of ruby. Pull request #2206
  by SHIBATA Hiroshi.
* Removed deprecated methods over the limit day. Pull request #2216 by
  SHIBATA Hiroshi.
* Remove syck support. Pull request #2222 by SHIBATA Hiroshi.
* Removed needless condition for Encoding. Pull request #2223 by SHIBATA
  Hiroshi.
* Removed needless condition for String#force_encoding. Pull request #2225
  by SHIBATA Hiroshi.
* Removed needless OpenSSL patch for Ruby 1.8. Pull request #2243 by
  SHIBATA Hiroshi.
* Removed compatibility code for Ruby 1.9.2. Pull request #2244 by SHIBATA
  Hiroshi.
* Removed needless version condition for the old ruby. Pull request #2252
  by SHIBATA Hiroshi.
* Remove needless define/respond_to condition. Pull request #2255 by
  SHIBATA Hiroshi.
* Use File.realpath directly in Gem::Package. Pull request #2284 by
  SHIBATA Hiroshi.
* Removed needless condition for old versions of Ruby. Pull request #2286
  by SHIBATA Hiroshi.
* Remove the --rdoc and --ri options from install/update. Pull request
  #2354 by Colby Swandale.
* Move authors assigner to required attributes section of
  Gem::Specification. Pull request #2406 by Grey Baker.
* Remove rubyforge_page functionality. Pull request #2436 by Nick
  Schwaderer.
* Drop ruby 1.8 support and use IO.popen. Pull request #2441 by Nobuyoshi
  Nakada.
* Drop ruby 2.2 support. Pull request #2487 by David Rodríguez.
* Remove some old compatibility code. Pull request #2488 by David
  Rodríguez.
* Remove .document from src. Pull request #2489 by Colby Swandale.
* Remove old version support. Pull request #2493 by Nobuyoshi Nakada.
* [BudlerVersionFinder] set .filter! and .compatible? to match only on
  major versions. Pull request #2515 by Colby Swandale.

# 2.7.10 / 2019-06-14

## Enhancements:

* Fix bundler rubygems binstub not properly looking for bundler. Pull request #2426
  by David Rodríguez.
* [BudlerVersionFinder] set .filter! and .compatible? to match only on major versions.
  Pull request #2515 by Colby Swandale.
+ Update for compatibility with new minitest. Pull request #2118 by MSP-Greg.

# 2.7.9 / 2019-03-05

Security fixes:

  * CVE-2019-8320: Delete directory using symlink when decompressing tar
  * CVE-2019-8321: Escape sequence injection vulnerability in `verbose`
  * CVE-2019-8322: Escape sequence injection vulnerability in `gem owner`
  * CVE-2019-8323: Escape sequence injection vulnerability in API response handling
  * CVE-2019-8324: Installing a malicious gem may lead to arbitrary code execution
  * CVE-2019-8325: Escape sequence injection vulnerability in errors

# 2.7.8 / 2018-11-02

## Enhancements:

* [Requirement] Treat requirements with == versions as equal. Pull
  request #2230 by Samuel Giddins.
* Fix exec_name documentation. Pull request #2239 by Luis Sagastume.
* [TarHeader] Extract the empty header into a constant. Pull request #2247
  by Samuel Giddins.
* Simplify the code that lets us call the original, non-monkeypatched
  Kernel#require. Pull request #2267 by Leon Miller-Out.
* Add install alias documentation. Pull request #2320 by ota42y.
* [Rakefile] Set bundler build metadata when doing a release. Pull request
  #2335 by Samuel Giddins.
* Backport commits from ruby core . Pull request #2347 by SHIBATA Hiroshi.
* Sign in to the correct host before push. Pull request #2366 by Luis
  Sagastume.
* Bump bundler-1.16.4. Pull request #2381 by SHIBATA Hiroshi.
* Improve bindir flag description. Pull request #2383 by Luis Sagastume.
* Update bundler-1.16.6. Pull request #2423 by SHIBATA Hiroshi.

## Bug fixes:

* Fix #1470: generate documentation when --install-dir is present. Pull
  request #2229 by Elias Hernandis.
* Fix no proxy checking. Pull request #2249 by Luis Sagastume.
* Validate SPDX license exceptions. Pull request #2257 by Mikit.
* Retry api specification spec with original platform. Pull request #2275
  by Luis Sagastume.
* Fix approximate recommendation with prereleases. Pull request #2345 by
  David Rodríguez.
* Gem::Version should handle nil like it used to before. Pull request
  #2363 by Luis Sagastume.

# 2.7.7 / 2018-05-08

## Enhancements:

* [RequestSet] Only suggest a gem version with an installable platform.
  Pull request #2175 by Samuel Giddins.
* Fixed no assignment variables about default gems installation. Pull
  request #2181 by SHIBATA Hiroshi.
* Backport improvements for test-case from Ruby core. Pull request #2189
  by SHIBATA Hiroshi.
* Fix ruby warnings in test suite. Pull request #2205 by Colby Swandale.
* To use Gem::Specification#bindir of bundler instead of hard coded path.
  Pull request #2208 by SHIBATA Hiroshi.
* Update gem push --help description. Pull request #2215 by Luis
  Sagastume.
* Backport ruby core commits. Pull request #2264 by SHIBATA Hiroshi.

## Bug fixes:

* Frozen string fix - lib/rubygems/bundler_version_finder.rb. Pull request
  #2115 by MSP-Greg.
* Fixed tempfile leak for RubyGems 2.7.6. Pull request #2194 by SHIBATA
  Hiroshi.
* Add missing requires. Pull request #2196 by David Rodríguez.
* Fix Gem::Version.correct?. Pull request #2203 by Masato Nakamura.
* Fix verify_entry regex for metadata. Pull request #2212 by Luis
  Sagastume.
* Fix path checks for case insensitive filesystem. Pull request #2211 by
  Lars Kanis.

## Deprecations:

* Deprecate unused code before removing them at #1524. Pull request #2197
  by SHIBATA Hiroshi.
* Deprecate for rubygems 3. Pull request #2214 by SHIBATA Hiroshi.
* Mark deprecation to `ubygems.rb` for RubyGems 4. Pull request #2269 by
  SHIBATA Hiroshi.

## Breaking changes:

* Update bundler-1.16.2. Pull request #2291 by SHIBATA Hiroshi.

# 2.7.6 / 2018-02-16

Security fixes:

* Prevent path traversal when writing to a symlinked basedir outside of the root.
  Discovered by nmalkin, fixed by Jonathan Claudius and Samuel Giddins.
* Fix possible Unsafe Object Deserialization Vulnerability in gem owner.
  Fixed by Jonathan Claudius.
* Strictly interpret octal fields in tar headers.
  Discovered by plover, fixed by Samuel Giddins.
* Raise a security error when there are duplicate files in a package.
  Discovered by plover, fixed by Samuel Giddins.
* Enforce URL validation on spec homepage attribute.
  Discovered by Yasin Soliman, fixed by Jonathan Claudius.
* Mitigate XSS vulnerability in homepage attribute when displayed via `gem server`.
  Discovered by Yasin Soliman, fixed by Jonathan Claudius.
* Prevent Path Traversal issue during gem installation.
  Discovered by nmalkin.

# 2.7.5

## Bug fixes:

* To use bundler-1.16.1 #2121 by SHIBATA Hiroshi.
* Fixed leaked FDs. Pull request #2127 by Nobuyoshi Nakada.
* Support option for `--destdir` with upgrade installer. #2169 by Thibault Jouan.
* Remove PID from gem index directory. #2155 by SHIBATA Hiroshi.
* Avoid a #mkdir race condition #2148 by Samuel Giddins.
* Gem::Util.traverse_parents should not crash on permissions error #2147 by Robert Ulejczyk.
* Use `File.open` instead of `open`. #2142 by SHIBATA Hiroshi.
* Set whether bundler is used for gemdeps with an environmental variable #2126 by SHIBATA Hiroshi.
* Fix undefined method error when printing alert #1884 by Robert Ross.

# 2.7.4

## Bug fixes:

* Fixed leaked FDs. Pull request #2127 by Nobuyoshi Nakada.
* Avoid to warnings about gemspec loadings in rubygems tests. Pull request
  #2125 by SHIBATA Hiroshi.
* Fix updater with rubygems-2.7.3 Pull request #2124 by SHIBATA Hiroshi.
* Handle environment that does not have `flock` system call. Pull request
  #2107 by SHIBATA Hiroshi.

# 2.7.3

## Enhancements:

* Removed needless version lock. Pull request #2074 by SHIBATA Hiroshi.
* Add --[no-]check-development option to cleanup command. Pull request
  #2061 by Lin Jen-Shin (godfat).
* Merge glob pattern using braces. Pull request #2072 by Kazuhiro
  NISHIYAMA.
* Removed warnings of unused variables. Pull request #2084 by SHIBATA
  Hiroshi.
* Call SPDX.org using HTTPS. Pull request #2102 by Olle Jonsson.
* Remove multi load warning from plugins documentation. Pull request #2103
  by Thibault Jouan.

## Bug fixes:

* Fix test failure on Alpine Linux. Pull request #2079 by Ellen Marie
  Dash.
* Avoid encoding issues by using binread in setup. Pull request #2089 by
  Mauro Morales.
* Fix rake install_test_deps once the rake clean_env does not exist. Pull
  request #2090 by Lucas Oliveira.
* Prevent to delete to "bundler-" prefix gem like bundler-audit. Pull
  request #2086 by SHIBATA Hiroshi.
* Generate .bat files on Windows platform. Pull request #2094 by SHIBATA
  Hiroshi.
* Workaround common options mutation in Gem::Command test. Pull request
  #2098 by Thibault Jouan.
* Check gems dir existence before removing bundler. Pull request #2104 by
  Thibault Jouan.
* Use setup command --regenerate-binstubs option flag. Pull request #2099
  by Thibault Jouan.

# 2.7.2

## Bug fixes:

* Added template files to vendoerd bundler. Pull request #2065 by SHIBATA
  Hiroshi.
* Added workaround for non-git environment. Pull request #2066 by SHIBATA
  Hiroshi.

# 2.7.1 (2017-11-03)

## Bug fixes:

* Fix `gem update --system` with RubyGems 2.7+. Pull request #2054 by
  Samuel Giddins.

# 2.7.0 (2017-11-02)

## Enhancements:

* Update vendored bundler-1.16.0. Pull request #2051 by Samuel Giddins.
* Use Bundler for Gem.use_gemdeps. Pull request #1674 by Samuel Giddins.
* Add command `signin` to `gem` CLI. Pull request #1944 by Shiva Bhusal.
* Add Logout feature to CLI. Pull request #1938 by Shiva Bhusal.
* Added message to uninstall command for gem that is not installed. Pull
  request #1979 by anant anil kolvankar.
* Add --trust-policy option to unpack command. Pull request #1718 by
  Nobuyoshi Nakada.
* Show default gems for all platforms. Pull request #1685 by Konstantin
  Shabanov.
* Add Travis and Appveyor build status to README. Pull request #1918 by
  Jun Aruga.
* Remove warning `no email specified` when no email. Pull request #1675 by
  Leigh McCulloch.
* Improve -rubygems performance. Pull request #1801 by Samuel Giddins.
* Improve the performance of Kernel#require. Pull request #1678 by Samuel
  Giddins.
* Improve user-facing messages by consistent casing of Ruby/RubyGems. Pull
  request #1771 by John Labovitz.
* Improve error message when Gem::RuntimeRequirementNotMetError is raised.
  Pull request #1789 by Luis Sagastume.
* Code Improvement: Inheritance corrected. Pull request #1942 by Shiva
  Bhusal.
* [Source] Autoload fileutils. Pull request #1906 by Samuel Giddins.
* Use Hash#fetch instead of if/else in Gem::ConfigFile. Pull request #1824
  by Daniel Berger.
* Require digest when it is used. Pull request #2006 by Samuel Giddins.
* Do not index the doc folder in the `update_manifest` task. Pull request
  #2031 by Colby Swandale.
* Don't use two postfix conditionals on one line. Pull request #2038 by
  Ellen Marie Dash.
* [SafeYAML] Avoid warning when Gem::Deprecate.skip is set. Pull request
  #2034 by Samuel Giddins.
* Update gem yank description. Pull request #2009 by David Radcliffe.
* Fix formatting of installation instructions in README. Pull request
  #2018 by Jordan Danford.
* Do not use #quick_spec internally. Pull request #1733 by Jon Moss.
* Switch from docs to guides reference. Pull request #1886 by Jonathan
  Claudius.
* Happier message when latest version is already installed. Pull request
  #1956 by Jared Beck.
* Update specification reference docs. Pull request #1960 by Grey Baker.
* Allow Gem.finish_resolve to respect already-activated specs. Pull
  request #1910 by Samuel Giddins.
* Update cryptography for Gem::Security. Pull request #1691 by Sylvain
  Daubert.
* Don't output mkmf.log message if compilation didn't fail. Pull request
  #1808 by Jeremy Evans.
* Matches_for_glob - remove root path. Pull request #2010 by ahorek.
* Gem::Resolver#search_for update for reliable searching/sorting. Pull
  request #1993 by MSP-Greg.
* Allow local installs with transitive prerelease requirements. Pull
  request #1990 by Samuel Giddins.
* Small style fixes to Installer Set. Pull request #1985 by Arthur
  Marzinkovskiy.
* Setup cmd: Avoid terminating option string w/ dot. Pull request #1825 by
  Olle Jonsson.
* Warn when no files are set. Pull request #1773 by Aidan Coyle.
* Ensure `to_spec` falls back on prerelease specs. Pull request #1755 by
  André Arko.
* [Specification] Eval setting default attributes in #initialize. Pull
  request #1739 by Samuel Giddins.
* Sort ordering of sources is preserved. Pull request #1633 by Nathan
  Ladd.
* Retry with :prerelease when no suggestions are found. Pull request #1696
  by Aditya Prakash.
* [Rakefile] Run `git submodule update --init` in `rake newb`. Pull
  request #1694 by Samuel Giddins.
* [TestCase] Address comments around ui changes. Pull request #1677 by
  Samuel Giddins.
* Eagerly resolve in activate_bin_path. Pull request #1666 by Samuel
  Giddins.
* [Version] Make hash based upon canonical segments. Pull request #1659 by
  Samuel Giddins.
* Add Ruby Together CTA, rearrange README a bit. Pull request #1775 by
  Michael Bernstein.
* Update Contributing.rdoc with new label usage. Pull request #1716 by
  Lynn Cyrin.
* Add --host sample to help. Pull request #1709 by Code Ahss.
* Add a helpful suggestion when `gem install` fails due to required_rub….
  Pull request #1697 by Samuel Giddins.
* Add cert expiration length flag. Pull request #1725 by Luis Sagastume.
* Add submodule instructions to manual install. Pull request #1727 by
  Joseph Frazier.
* Allow usage of multiple `--version` operators. Pull request #1546 by
  James Wen.
* Warn when requiring deprecated files. Pull request #1939 by Ellen Marie
  Dash.

## Deprecations:

* Deprecate Gem::InstallerTestCase#util_gem_bindir and
  Gem::InstallerTestCase#util_gem_dir. Pull request #1729 by Jon Moss.
* Deprecate passing options to Gem::GemRunner. Pull request #1730 by Jon
  Moss.
* Add deprecation for Gem#datadir. Pull request #1732 by Jon Moss.
* Add deprecation warning for Gem::DependencyInstaller#gems_to_install.
  Pull request #1731 by Jon Moss.

## Breaking changes:

* Use `-rrubygems` instead of `-rubygems.rb`. Because ubygems.rb is
  unavailable on Ruby 2.5. Pull request #2028 #2027 #2029
  by SHIBATA Hiroshi.
* Update Code of Conduct to Contributor Covenant v1.4.0. Pull request
  #1796 by Matej.

## Bug fixes:

* Fix issue for MinGW / MSYS2 builds and testing. Pull request #1876 by
  MSP-Greg.
* Fixed broken links and overzealous URL encoding in gem server. Pull
  request #1809 by Nicole Orchard.
* Fix a typo. Pull request #1722 by Koichi ITO.
* Fix error message Gem::Security::Policy. Pull request #1724 by Nobuyoshi
  Nakada.
* Fixing links markdown formatting in README. Pull request #1791 by Piotr
  Kuczynski.
* Fix failing Bundler 1.8.7 CI builds. Pull request #1820 by Samuel
  Giddins.
* Fixed test broken on ruby-head . Pull request #1842 by SHIBATA Hiroshi.
* Fix typos with misspell. Pull request #1846 by SHIBATA Hiroshi.
* Fix gem open to open highest version number rather than lowest. Pull
  request #1877 by Tim Pope.
* Fix test_self_find_files_with_gemfile to sort expected files. Pull
  request #1878 by Kazuaki Matsuo.
* Fix typos in CONTRIBUTING.rdoc. Pull request #1909 by Mark Sayson.
* Fix some small documentation issues in installer. Pull request #1972 by
  Colby Swandale.
* Fix links in Policies document. Pull request #1964 by Alyssa Ross.
* Fix NoMethodError on bundler/inline environment. Pull request #2042 by
  SHIBATA Hiroshi.
* Correct comments for Gem::InstallerTestCase#setup. Pull request #1741 by
  MSP-Greg.
* Use File.expand_path for certification and key location. Pull request
  #1987 by SHIBATA Hiroshi.
* Rescue EROFS. Pull request #1417 by Nobuyoshi Nakada.
* Fix spelling of 'vulnerability'. Pull request #2022 by Philip Arndt.
* Fix metadata link key names. Pull request #1896 by Aditya Prakash.
* Fix a typo in uninstall_command.rb. Pull request #1934 by Yasuhiro
  Horimoto.
* Gem::Requirement.create treat arguments as variable-length. Pull request
  #1830 by Toru YAGI.
* Display an explanation when rake encounters an ontological problem. Pull
  request #1982 by Wilson Bilkovich.
* [Server] Handle gems with names ending in `-\d`. Pull request #1926 by
  Samuel Giddins.
* [InstallerSet] Avoid reloading _all_ local gems multiple times during
  dependency resolution. Pull request #1925 by Samuel Giddins.
* Modify the return value of Gem::Version.correct?. Pull request #1916 by
  Tsukuru Tanimichi.
* Validate metadata link keys. Pull request #1834 by Aditya Prakash.
* Add changelog to metadata validation. Pull request #1885 by Aditya
  Prakash.
* Replace socket error text message. Pull request #1823 by Daniel Berger.
* Raise error if the email is invalid when building cert. Pull request
  #1779 by Luis Sagastume.
* [StubSpecification] Don’t iterate through all loaded specs in #to_spec.
  Pull request #1738 by Samuel Giddins.

# 2.6.14 / 2017-10-09

Security fixes:

* Whitelist classes and symbols that are in loaded YAML.
  See CVE-2017-0903 for full details.
  Fix by Aaron Patterson.

# 2.6.13 / 2017-08-27

Security fixes:

* Fix a DNS request hijacking vulnerability. (CVE-2017-0902)
  Discovered by Jonathan Claudius, fix by Samuel Giddins.
* Fix an ANSI escape sequence vulnerability. (CVE-2017-0899)
  Discovered by Yusuke Endoh, fix by Evan Phoenix.
* Fix a DOS vulnerability in the `query` command. (CVE-2017-0900)
  Discovered by Yusuke Endoh, fix by Samuel Giddins.
* Fix a vulnerability in the gem installer that allowed a malicious gem
  to overwrite arbitrary files. (CVE-2017-0901)
  Discovered by Yusuke Endoh, fix by Samuel Giddins.

# 2.6.12 / 2017-04-30

## Bug fixes:

* Fix test_self_find_files_with_gemfile to sort expected files. Pull
  request #1880 by Kazuaki Matsuo.
* Fix issue for MinGW / MSYS2 builds and testing. Pull request #1879 by
  MSP-Greg.
* Fix gem open to open highest version number rather than lowest. Pull
  request #1877 by Tim Pope.
* Add a test for requiring a default spec as installed by the ruby
  installer. Pull request #1899 by Samuel Giddins.
* Fix broken --exact parameter to gem command. Pull request #1873 by Jason
  Frey.
* [Installer] Generate backwards-compatible binstubs. Pull request #1904
  by Samuel Giddins.
* Fix pre-existing source recognition on add action. Pull request #1883 by
  Jonathan Claudius.
* Prevent negative IDs in output of #inspect. Pull request #1908 by Vít
  Ondruch.
* Allow Gem.finish_resolve to respect already-activated specs. Pull
  request #1910 by Samuel Giddins.

# 2.6.11 / 2017-03-16

## Bug fixes:

* Fixed broken tests on ruby-head. Pull request #1841 by
  SHIBATA Hiroshi.
* Update vendored Molinillo to 0.5.7. Pull request #1859 by Samuel
  Giddins.
* Avoid activating Ruby 2.5 default gems when possible. Pull request #1843
  by Samuel Giddins.
* Use improved resolver sorting algorithm. Pull request #1856 by
  Samuel Giddins.

# 2.6.10 / 2017-01-23

## Bug fixes:

* Fix `require` calling the wrong `gem` method when it is overridden.
  Pull request #1822 by Samuel Giddins.

# 2.6.9 / 2017-01-20

## Bug fixes:

* Allow initializing versions with empty strings. Pull request #1767 by
  Luis Sagastume.
* Fix TypeError on 2.4. Pull request #1788 by Nobuyoshi Nakada.
* Don't output mkmf.log message if compilation didn't fail. Pull request
  #1808 by Jeremy Evans.
* Fixed broken links and overzealous URL encoding in gem server. Pull
  request #1809 by Nicole Orchard.
* Update vendored Molinillo to 0.5.5. Pull request #1812 by Samuel
  Giddins.
* RakeBuilder: avoid frozen string issue. Pull request #1819 by Olle
  Jonsson.

# 2.6.8 / 2016-10-29

## Bug fixes:

* Improve SSL verification failure message. Pull request #1751
  by Eric Hodel.
* Ensure `to_spec` falls back on prerelease specs. Pull request
  #1755 by André Arko.
* Update vendored Molinillo to 0.5.3. Pull request #1763 by
  Samuel Giddins.

# 2.6.7 / 2016-09-26

## Bug fixes:

* Install native extensions in the correct location when using the
  `--user-install` flag. Pull request #1683 by Noah Kantrowitz.
* When calling `Gem.sources`, load sources from `configuration`
  if present, else use the default sources. Pull request #1699
  by Luis Sagastume.
* Fail gracefully when attempting to redirect without a Location.
  Pull request #1711 by Samuel Giddins.
* Update vendored Molinillo to 0.5.1. Pull request #1714 by
  Samuel Giddins.

# 2.6.6 / 2016-06-22

## Bug fixes:

* Sort installed versions to make sure we install the latest version when
  running `gem update --system`. As a one-time fix, run
  `gem update --system=2.6.6`. Pull request #1601 by David Radcliffe.

# 2.6.5 / 2016-06-21

## Enhancements:

* Support for unified Integer in Ruby 2.4. Pull request #1618
  by SHIBATA Hiroshi.
* Update vendored Molinillo to 0.5.0 for performance improvements.
  Pull request #1638 by Samuel Giddins.

## Bug fixes:

* Raise an explicit error if Signer#sign is called with no certs. Pull
  request #1605 by Daniel Berger.
* Update `update_bundled_ca_certificates` utility script for directory
  nesting. Pull request #1583 by James Wen.
* Fix broken symlink support in tar writer (+ fix broken test). Pull
  request #1578 by Cezary Baginski.
* Remove extension directory before (re-)installing. Pull request #1576
  by Jeremy Hinegardner.
* Regenerate test CA certificates with appropriate extensions. Pull
  request #1611 by rhenium.
* Rubygems does not terminate on failed file lock when not superuser. Pull
  request #1582 by Ellen Marie Dash.
* Fix tar headers with a 101 character name. Pull request #1612 by Paweł
  Tomulik.
* Add Gem.platform_defaults to allow implementations to override defaults.
  Pull request #1644 by Charles Oliver Nutter.
* Run Bundler tests on TravisCI. Pull request #1650 by Samuel Giddins.

# 2.6.4 / 2016-04-26

## Enhancements:

* Use Gem::Util::NULL_DEVICE instead of hard coded strings. Pull request #1588
  by Chris Charabaruk.
* Use File.symlink on MS Windows if supported. Pull request #1418
  by Nobuyoshi Nakada.

## Bug fixes:

* Redact uri password from error output when gem fetch fails. Pull request
  #1565 by Brian Fletcher.
* Suppress warnings. Pull request #1594 by Nobuyoshi Nakada.
* Escape user-supplied content served on web pages by `gem server` to avoid
  potential XSS vulnerabilities. Samuel Giddins.

# 2.6.3 / 2016-04-05

## Enhancements:

* Lazily calculate Gem::LoadError exception messages. Pull request #1550
  by Aaron Patterson.
* New fastly cert. Pull request #1548 by David Radcliffe.
* Organize and cleanup SSL certs. Pull request #1555 by James Wen.
* [RubyGems] Make deprecation message for paths= more helpful. Pull
  request #1562 by Samuel Giddins.
* Show default gems when using "gem list". Pull request #1570 by Luis
  Sagastume.

## Bug fixes:

* Stub ordering should be consistent regardless of how cache is populated.
  Pull request #1552 by Aaron Patterson.
* Handle cases when the @@stubs variable contains non-stubs. Pull request
  #1558 by Per Lundberg.
* Fix test on Windows for inconsistent temp path. Pull request #1554 by
  Hiroshi Shirosaki.
* Fix `Gem.find_spec_for_exe` picks oldest gem. Pull request #1566 by
  Shinichi Maeshima.
* [Owner] Fallback to email and userid when owner email is missing. Pull
  request #1569 by Samuel Giddins.
* [Installer] Handle nil existing executable. Pull request #1561 by Samuel
  Giddins.
* Allow two digit version numbers in the tests. Pull request #1575 by unak.

# 2.6.2 / 2016-03-12

## Bug fixes:

* Fix wrong version of gem activation for bin stub. Pull request #1527 by
  Aaron Patterson.
* Speed up gem activation failures. Pull request #1539 by Aaron Patterson.
* Fix platform sorting in the resolver. Pull request #1542 by Samuel E.
  Giddins.
* Ensure we unlock the monitor even if try_activate throws. Pull request
  #1538 by Charles Oliver Nutter.


# 2.6.1 / 2016-02-28

## Bug fixes:

* Ensure `default_path` and `home` are set for paths. Pull request #1513
  by Aaron Patterson.
* Restore but deprecate support for Array values on `Gem.paths=`. Pull
  request #1514 by Aaron Patterson.
* Fix invalid gem file preventing gem install from working. Pull request
  #1499 by Luis Sagastume.

# 2.6.0 / 2016-02-26

## Enhancements:

* RubyGems now defaults the `gem push` to the gem's "allowed_push_host"
  metadata setting.  Pull request #1486 by Josh Lane.
* Update bundled Molinillo to 0.4.3. Pull request #1493 by Samuel E. Giddins.
* Add version option to gem open command. Pull request #1483 by Hrvoje
  Šimić.
* Feature/add silent flag. Pull request #1455 by Luis Sagastume.
* Allow specifying gem requirements via env variables. Pull request #1472
  by Samuel E. Giddins.

## Bug fixes:

* RubyGems now stores `gem push` credentials under the host you signed-in for.
  Pull request #1485 by Josh Lane.
* Move `coding` location to first line. Pull request #1471 by SHIBATA
  Hiroshi.
* [PathSupport] Handle a regexp path separator. Pull request #1469 by
  Samuel E. Giddins.
* Clean up the PathSupport object. Pull request #1094 by Aaron Patterson.
* Join with File::PATH_SEPARATOR in Gem.use_paths. Pull request #1476 by
  Samuel E. Giddins.
* Handle when the gem home and gem path aren't set in the config file. Pull
  request #1478 by Samuel E. Giddins.
* Terminate TimeoutHandler. Pull request #1479 by Nobuyoshi Nakada.
* Remove redundant cache. Pull request #1482 by Eileen M. Uchitelle.
* Freeze `Gem::Version@segments` instance variable. Pull request #1487 by
  Ben Dean.
* Gem cleanup is trying to uninstall gems outside GEM_HOME and reporting
  an error after it tries. Pull request #1353 by Luis Sagastume.
* Avoid duplicated sources. Pull request #1489 by Luis Sagastume.
* Better description for quiet flag. Pull request #1491 by Luis Sagastume.
* Raise error if find_by_name returns with nil. Pull request #1494 by
  Zoltán Hegedüs.
* Find_files only from loaded_gems when using gemdeps. Pull request #1277
  by Michal Papis.

# 2.5.2 / 2016-01-31

## Bug fixes:

* Fix memoization of Gem::Version#prerelease? Pull request #1125 by Matijs van
  Zuijlen.
* Handle trailing colons in GEM_PATH, by Damien Robert.
* Improve the Gemfile `gemspec` method, fixing #1204 and #1033. Pull request
  #1276 by Michael Papis.
* Warn only once when a gemspec license is invalid. Pull request #1414 by Samuel
  E. Giddins.
* Check for exact constants before using them, fixing Ruby bug #11940. Pull
  request #1438 by Nobuyoshi Nakada.
* Fix building C extensions on Ruby 1.9.x on Windows. Pull request #1453 by Marie
  Markwell.
* Handle symlinks containing ".." correctly. Pull request #1457 by Samuel E.
  Giddins.

## Enhancements:

* Add `--no-rc` flag, which skips loading `.gemrc`. Pull request #1329 by Luis
  Sagastume.
* Allow basic auth to be excluded from `allowed_push_host`. By Josh Lane.
* Add `gem list --exact`, which finds gems by string match instead of regex. Pull
  request #1344 by Luis Sagastume.
* Suggest alternatives when gem license is unknown. Pull request #1443 by Samuel
  E. Giddins.
* Print a useful error if a binstub expects a newer version of a gem than is
  installed. Pull request #1407 by Samuel E. Giddins.
* Allow the (supported) s3:// scheme to be used with `--source`. Pull request
  #1416 by Dave Adams.
* Add `--[no-]post-install-message` to `install` and `update`. Pull request #1162
  by Josef Šimánek.
* Add `--host` option to `yank`, providing symmetry with `pull`. Pull request
  #1361 by Mike Virata-Stone.
* Update bundled Molinillo to 0.4.1. Pull request #1452 by Samuel E. Giddins.
* Allow calling `build` without '.gemspec'. Pull request #1454 by Stephen
  Blackstone.
* Add support for `source` option on gems in Gemfile. Pull request #1355 by
  Michael Papis.
* Function correctly when string literals are frozen on Ruby 2.3. Pull request
  #1408 by Samuel E. Giddins.

# 2.5.1 / 2015-12-10

## Bug fixes:

* Ensure platform sorting only uses strings. Affected binary installs on Windows.
  Issue #1369 reported by Ryan Atball (among others).
  Pull request #1375 by Samuel E. Giddins.
* Revert PR #1332. Unable to reproduce, and nil should be impossible.
* Gem::Specification#to_fullpath now returns .rb extensions when such a file
  exists.  Pull request #1114 by y-yagi.
* RubyGems now handles Net::HTTPFatalError instead of crashing.  Pull
  request #1314 by Samuel E. Giddins.
* Updated bundled Molinillo to 0.4.0.  Pull request #1322, #1396 by Samuel E.
  Giddins.
* Improved performance of spec loading by reducing likelihood of loading the
  complete specification.  Pull request #1373 by Aaron Patterson.
* Improved caching of requirable files  Pull request #1377 by Aaron Patterson.
* Fixed activation of gems with development dependencies.  Pull request #1388
  by Samuel E. Giddins.
* RubyGems now uses the same Molinillo vendoring strategy as Bundler.  Pull
  request #1397 by Samuel E. Giddins.
* Fixed documentation of Gem::Requirement.parse.  Pull request #1398 by
  Juanito Fatas.
* RubyGems no longer warns when a prerelease gem has prerelease dependencies.
  Pull request #1399 by Samuel E. Giddins.
* Fixed Gem::Version documentation example.  Pull request #1401 by Guilherme
  Goettems Schneider.
* Updated documentation links to https://.  Pull request #1404 by Suriyaa
  Kudo.
* Fixed double word typo.  Pull request #1411 by Jake Worth.

# 2.5.0 / 2015-11-03

## Enhancements:

* Added the Gem::Licenses class which provides a set of standard license
  identifiers as set by spdx.org. This is now used by the
  Gem::Specification#license attribute to try to standardize (though not
  enforce) licenses set by gem authors.

  Pull request #1249 by Kyle Mitchell.

* Use Molinillo as the resolver library.  This is the same resolver as used by
  Bundler.  Pull request #1189 by Samuel E. Giddins.
* Add `--skip=gem_name` to Pristine command.  Pull request #1018 by windwiny.
* The parsed gem dependencies file is now available via Gem.gemdeps following
  Gem.use_gemdeps.  Pull request #1224 by Hsing-Hui Hsu, issue #1213 by
  Michal Papis.
* Moved description attribute to recommended for Gem::Specification.
  Pull request #1046 by Michal Papis
* Moved `Gem::Indexer#abbreviate` and `#sanitize` to `Gem::Specification`.
  Pull request #1145 by Arthur Nogueira Neves
* Cache Gem::Version segments for `#bump` and `#release`.
  Pull request #1131 by Matijs van Zuijlen
* Fix edge case in `levenshtein_distance` for comparing longer strings.
  Pull request #1173 by Richard Schneeman
* Remove duplication from List#to_a, improving from O(n^2) to O(n) time.
  Pull request #1200 by Marc Siegel.
* Gem::Specification.add_specs is deprecated and will be removed from version
  3.0 with no replacement.  To add specs, install the gem, then reset the
  cache.
* Gem::Specification.add_spec is deprecated and will be removed from version
  3.0 with no replacement.  To add specs, install the gem, then reset the
  cache.
* Gem::Specification.remove_spec is deprecated and will be removed from version
  3.0 with no replacement.  To remove specs, uninstall the gem, then reset the
  cache by calling Gem::Specification.reset.
* Call Array#compact before calling Array#uniq for minor speed improvement in
  the Gem::Specification#files method.
  Pull request #1253 by Marat Amerov.
* Use stringio instead of custom String classes.
  Pull request #1250 by Petr Skocik.
* Use URI#host instead of URI#hostname to retain backwards compatibility with
  Ruby 1.9.2 and earlier in util library.
  Pull request #1288 by Joe Rafaniello.
* Documentation update for gem sources.
  Pull request #1324 by Ilya Vassilevsky.
* Documentation update for required_ruby_version.
  Pull request #1321 by Matt Patterson.
* Documentation update for gem update.
  Pull request #1306 by Tim Blair.
* Emit a warning on SRV resolve failure.
  Pull request #1023 by Ivan Kuchin.
* Allow duplicate dependencies between runtime and development.
  Pull request #1032 by Murray Steele.
* The gem env command now shows the user installation directory.
  Pull request #1343 by Luis Sagastume.
* The Gem::Platform#=== method now treats a nil cpu arch the same as 'universal'.
  Pull request #1356 by Daniel Berger.
* Improved memory performance in Gem::Specification.traverse.  Pull request
  #1188 by Aaron Patterson.
* RubyGems packages now support symlinks.  Pull request #1209 by Samuel E.
  Giddins.
* RubyGems no longer outputs mkmf.log if it does not exist.  Pull request
  #1222 by Andrew Hooker.
* Added Bitrig platform.  Pull request #1233 by John C. Vernaleo.
* Improved error message for first-time RubyGems developers.  Pull request
  #1241 by André Arko
* Improved performance of Gem::Specification#load with cached specs.  Pull
  request #1297 by Samuel E. Giddins.
* Gem::RemoteFetcher allows users to set HTTP headers.  Pull request #1363 by
  Agis Anastasopoulos.

## Bug fixes:

* Fixed Rake homepage url in example for Gem::Specification#homepage.
  Pull request #1171 by Arthur Nogueira Neves
* Don't crash if partially uninstalled gem can't be found.
  Pull request #1283 by Cezary Baginski.
* Test warning cleanup.
  Pull request #1298 by Samuel E. Giddins.
* Documentation fix for GemDependencyAPI.
  Pull request #1308 by Michael Papis.
* Fetcher now ignores ENOLCK errors in single threaded environments. This
  handles an issue with gem installation on NFS as best we can. Addresses
  issue #1176 by Ryan Moore.
  Pull request #1327 by Daniel Berger.
* Fix some path quoting issues in the test suite.
  Pull request #1328 by Gavin Miller.
* Fix NoMethodError in running ruby processes when gems are uninstalled.
  Pull request #1332 by Peter Drake.
* Fixed a potential NoMethodError for gem cleanup.
  Pull request #1333 by Peter Drake.
* Fixed gem help bug.
  Issue #1352 reported by bogem, pull request #1357 by Luis Sagastume.
* Remove temporary directories after tests finish.  Pull request #1181 by
  Nobuyoshi Nokada.
* Update links in RubyGems documentation.  Pull request #1185 by Darío Hereñú.
* Prerelease gem executables can now be run.  Pull request #1186 by Samuel E.
  Giddins.
* Updated RubyGems travis-ci ruby versions.  Pull request #1187 by Samuel E.
  Giddins.
* Fixed release date of RubyGems 2.4.6.  Pull request #1190 by Frieder
  Bluemle.
* Fixed bugs in gem activation.  Pull request #1202 by Miklós Fazekas.
* Fixed documentation for `gem list`.  Pull request #1228 by Godfrey Chan.
* Fixed #1200 history entry.  Pull request #1234 by Marc Siegel.
* Fixed synchronization issue when resetting the Gem::Specification gem list.
  Pull request #1239 by Samuel E. Giddins.
* Fixed running tests in parallel.  Pull request #1257 by SHIBATA Hiroshi.
* Fixed running tests with `--program-prefix` or `--program-suffix` for ruby.
  Pull request #1258 by Shane Gibbs.
* Fixed Gem::Specification#to_yaml.  Pull request #1262 by Hiroaki Izu.
* Fixed taintedness of Gem::Specification#raw_require_paths.  Pull request
  #1268 by Sam Ruby.
* Fixed sorting of platforms when installing gems.  Pull request #1271 by
  nonsequitur.
* Use `--no-document` over deprecated documentation options when installing
  dependencies on travis.  Pull request #1272 by takiy33.
* Improved support for IPv6 addresses in URIs.  Pull request #1275 by Joe
  Rafaniello.
* Spec validation no longer crashes if a file does not exist.  Pull request
  #1278 by Samuel E. Giddins.
* Gems can now be installed within `rescue`.  Pull request #1282 by Samuel E.
  Giddins.
* Increased Diffie-Hellman key size for tests for modern OpenSSL.  Pull
  request #1290 by Vít Ondruch.
* RubyGems handles invalid config files better.  Pull request #1367 by Agis
  Anastasopoulos.

# 2.4.8 / 2015-06-08

## Bug fixes:

* Tightened API endpoint checks for CVE-2015-3900

# 2.4.7 / 2015-05-14

## Bug fixes:

* Limit API endpoint to original security domain for CVE-2015-3900.
  Fix by claudijd

# 2.4.6 / 2015-02-05

## Bug fixes:

* Fixed resolving gems with both upper and lower requirement boundaries.
  Issue #1141 by Jakub Jirutka.
* Moved extension directory after require_paths to fix missing constant bugs
  in some gems with C extensions.  Issue #784 by André Arko, pull request
  #1137 by Barry Allard.
* Use Gem::Dependency#requirement when adding a dependency to an existing
  dependency instance.  Pull request #1101 by Josh Cheek.
* Fixed warning of shadowed local variable in Gem::Specification.  Pull request
  #1109 by Rohit Arondekar
* Gem::Requirement should always sort requirements before coercion to Hash.
  Pull request #1139 by Eito Katagiri.
* The `gem open` command should change the current working directory before
  opening the editor.  Pull request #1142 by Alex Wood.
* Ensure quotes are stripped from the Windows launcher script used to install
  gems.  Pull request #1115 by Youngjun Song.
* Fixed errors when writing to NFS to to 0444 files.  Issue #1161 by Emmanuel
  Hadoux.
* Removed dead code in Gem::StreamUI.  Pull request #1117 by mediaslave24.
* Fixed typos.  Pull request #1096 by hakeda.
* Relaxed CMake dependency for RHEL 6 and CentOS 6.  Pull request #1124 by Vít
  Ondruch.
* Relaxed Psych dependency.  Pull request #1128 by Vít Ondruch.

# 2.4.5 / 2014-12-03

## Bug fixes:

* Improved speed of requiring gems.  (Around 25% for a 60 gem test).  Pull
  request #1060 by unak.
* RubyGems no longer attempts to look up gems remotely with the --local flag.
  Pull request #1084 by Jeremy Evans.
* Executable stubs use the correct gem version when RUBYGEMS_GEMDEPS is
  active.  Issue #1072 by Michael Kaiser-Nyman.
* Fixed handling of pinned gems in lockfiles with versions.  Issue #1078 by
  Ian Ker-Seymer.
* Fixed handling of git@example:gem.git URIs.  Issue #1054 by Mogutan Mogu.
* Fixed handling of platforms retrieved from the dependencies API.  Issue
  #1058 and patch suggestion by tux-mind.
* RubyGems now suggests a copy-pasteable `gem pristine` command when
  extensions are missing.  Pull request #1057 by Shannon Skipper.
* Improved errors for long file names when packaging.  Pull request #1016 by
  Piotrek Bator.
* `gem pristine` now skips gems cannot be found remotely.  Pull request #1064
  by Tuomas Kareinen.
* `gem pristine` now caches gems to the proper directory.  Pull request #1064
  by Tuomas Kareinen.
* `gem pristine` now skips bundled gems properly.  Pull request #1064 by
  Tuomas Kareinen.
* Improved interoperability of Vagrant with RubyGems.  Pull request #1057 by
  Vít Ondruch.
* Renamed CONTRIBUTING to CONTRIBUTING.rdoc to allow markup.  Pull request
  #1090 by Roberto Miranda.
* Switched from #partition to #reject as only one collection is used.  Pull
  request #1074 by Tuomas Kareinen.
* Fixed installation of gems on systems using memory-mapped files.  Pull
  request #1038 by Justin Li.
* Fixed bug in Gem::Text#min3 where `a == b < c`.  Pull request #1026 by
  fortissimo1997.
* Fixed uninitialized variable warning in BasicSpecification.  Pull request
  #1019 by Piotr Szotkowski.
* Removed unneeded exception handling for cyclic dependencies.  Pull request
  #1043 by Jens Wille.
* Fixed grouped expression warning.  Pull request #1081 by André Arko.
* Fixed handling of platforms when writing lockfiles.

# 2.4.4 / 2014-11-12

## Bug fixes:

* Add alternate Root CA for upcoming certificate change. Fixes #1050 by
  Protosac

# 2.4.3 / 2014-11-10

## Bug fixes:

* Fix redefine MirrorCommand issue. Pull request #1044 by @akr.
* Fix typo in platform= docs.  Pull request #1048 by @jasonrclark
* Add root SSL certificates for upcoming certificate change.  Fixes #1050 by
  Protosac

# 2.4.2 / 2014-10-01

This release was sponsored by Ruby Central.

## Bug fixes:

* RubyGems now correctly matches wildcard no_proxy hosts.  Issue #997 by
  voelzemo.
* Added support for missing git_source method in the gem dependencies API.
* Fixed handling of git gems with an alternate install directory.
* Lockfiles will no longer be truncated upon resolution errors.
* Fixed messaging for `gem owner -a`.  Issue #1004 by Aaron Patterson, Ryan
  Davis.
* Removed meaningless ensure.  Pull request #1003 by gogotanaka.
* Improved wording of --source option help.  Pull request #989 by Jason Clark.
* Empty build_info files are now ignored.  Issue #903 by Adan Alvarado.
* Gem::Installer ignores dependency checks when installing development
  dependencies.  Issue #994 by Jens Willie.
* `gem update` now continues after dependency errors.  Issue #993 by aaronchi.
* RubyGems no longer warns about semantic version dependencies for the 0.x
  range.  Issue #987 by Jeff Felchner, pull request #1006 by Hsing-Hui Hsu.
* Added minimal lock to allow multithread installation of gems.  Issue #982
  and pull request #1005 by Yorick Peterse
* RubyGems now considers prerelease dependencies as it did in earlier versions
  when --prerelease is given.  Issue #990 by Jeremy Tryba.
* Updated capitalization in README.  Issue #1010 by Ben Bodenmiller.
* Fixed activating gems from a Gemfile for default gems.  Issue #991 by khoan.
* Fixed windows stub script generation for Cygwin.  Issue #1000 by Brett
  DiFrischia.
* Allow gem bindir and ruby.exe to live in separate directories.  Pull request
  #942 by Ian Flynn.
* Fixed handling of gemspec in gem dependencies files to match Bundler
  behavior.  Issue #1020 by Michal Papis.
* Fixed `gem update` when updating to prereleases.  Issue #1028 by Santiago
  Pastorino.
* RubyGems now fails immediately when a git reference cannot be found instead
  of spewing git errors.  Issue #1031 by Michal Papis

# 2.4.1 / 2014-07-17

## Bug fixes:

* RubyGems can now be updated on Ruby implementations that do not support
  vendordir in RbConfig::CONFIG.  Issue #974 by net1957.

# 2.4.0 / 2014-07-16

## Enhancements:

* The contents command now supports a --show-install-dir option that shows
  only the directory the gem is installed in.  Feature request #966 by Akinori
  MUSHA.
* Added a --build-root option to the install command for packagers.  Pull
  request #965 by Marcus Rückert.
* Added vendor gem support to RubyGems.  Package managers may now install gems
  in Gem.vendor_dir with the --vendor option to gem install.  Issue #943 by
  Marcus Rückert.

## Bug fixes:

* Kernel#gem now respects the prerelease flag when activating gems.
  Previously this behavior was undefined which could lead to bugs when a
  prerelease version was unintentionally activated.  Bug #938 by Joe Ferris.
* RubyGems now prefers gems from git over installed gems.  This allows gems
  from git to override an installed gem with the same name and version.  Bug
  #944 by Thomas Kriechbaumer.
* Fixed handling of git gems in a lockfile with unversioned dependencies.  Bug
  #940 by Michael Kaiser-Nyman.
* The ruby directive in a gem dependencies file is ignored when installing.
  Bug #941 by Michael Kaiser-Nyman.
* Added open to list of builtin commands (`gem open` now works).  Reported by
  Espen Antonsen.
* `gem open` now works with command-line editors.  Pull request #962 by Tim
  Pope.
* `gem install -g` now respects `--conservative`.  Pull request #950 by Jeremy
  Evans.
* RubyGems releases announcements now now include checksums.  Bug #939 by
  Alexander E. Fischer.
* RubyGems now expands ~ in $PATH when checking if installed executables will
  be runnable.  Pull request #945 by Alex Talker.
* Fixed `gem install -g --explain`.  Issue #947 by Luis Lavena.  Patch by
  Hsing-Hui Hsu.
* RubyGems locks less during gem activation.  Pull request #951 by Aaron
  Patterson and Justin Searls, #969 by Jeremy Tryba.
* Kernel#gem is now thread-safe.  Pull request #967 by Aaron Patterson.
* RubyGems now handles spaces in directory names for some parts of extension
  building.  Pull request #949 by Tristan Hill.
* RubyGems no longer defines an empty Date class.  Pull Request #948 by Benoit
  Daloze.
* RubyGems respects --document options for `gem update` again.  Bug 946 by
  jonforums.  Patch by Hsing-Hui Hsu.
* RubyGems generates documentation again with --ignore-dependencies.  Bug #961
  by Pulfer.
* RubyGems can install extensions across partitions now.  Pull request #970 by
  Michael Scherer.
* `-s` is now short for `--source` which resolves an ambiguity with
  --no-suggestions.  Pull request #955 by Alexander Kahn.
* Added extra test for ~> for 0.0.X versions.  Pull request #958 by Mark
  Lorenz.
* Fixed typo in gem updated help.  Pull request #952 by Per Modin.
* Clarified that the gem description should not be excessively long.  Part of
  bug #956 by Renier Morales.
* Hid documentation of outdated test_files related methods in Specification.
  Guides issue #90 by Emil Soman.
* RubyGems now falls back to the old index if the rubygems.org API fails
  during gem resolution.


# 2.3.0 / 2014-06-10

## Enhancements:

* Added the `open` command which allows you to inspect the source of a gem
  using your editor.
  Issue #789 by Mike Perham. Pull request #804 by Vitali F.
* The `update` command shows a summary of which gems were and were not
  updated.  Issue #544 by Mark D. Blackwell.
  Pull request #777 by Tejas Bubane.
* Improved "could not find 'gem'" error reporting.  Pull request #913 by
  Richard Schneeman.
* Gem.use_gemdeps now accepts an argument specifying the path of the gem
  dependencies file.  When the file is not found an ArgumentError is raised.
* Writing a .lock file for a gem dependencies file is now controlled by the
  --[no-]lock option.  Pull request #774 by Jeremy Evans.
* Suggestion of alternate names and spelling corrections during install can be
  suppressed with the --no-suggestions option.  Issue #867 by Jimmy Cuadra.
* Added mswin64 support.  Pull request #881 by U. Nakamura.
* A gem is installable from an IO again (as in RubyGems 1.8.x and older).
  Pull request #716 by Xavier Shay.
* RubyGems no longer attempts to build extensions during activation.  Instead
  a warning is issued instructing you to run `gem pristine` which will build
  the extensions for the current platform.  Issue #796 by dunric.
* Added Gem::UserInteraction#verbose which prints when the --verbose option is
  given.  Pull request #811 by Aaron Patterson.
* RubyGems can now fetch gems from private repositories using S3.  Pull
  request #856 by Brian Palmer.
* Added Gem::ConflictError subclass of Gem::LoadError so you can distinguish
  conflicts from other problems.  Pull request #841 by Aaron Patterson.
* Cleaned up unneeded load_yaml bootstrapping in Rakefile.  Pull request #815
  by Zachary Scott.
* Improved performance of conflict resolution.  Pull request #842 by Aaron
  Patterson.
* Add documentation of "~> 0" to Gem::Version.  Issue #896 by Aaron Suggs.
* Added CONTRIBUTING file.  Pull request #849 by Mark Turner.
* Allow use of bindir in windows_stub_script in .bat
  Pull request #818 by @unak and @nobu
* Use native File::PATH_SEPARATOR and remove $ before gem env on
  Gem::Dependency#to_specs. Pull request #915 by @parkr
* RubyGems recommends SPDX IDs for licenses now.  Pull request #917 by
  Benjamin Fleischer.

## Bug fixes:

* RubyGems now only fetches the latest specs to find misspellings which speeds
  up gem suggestions.  Pull request #808 by Aaron Patterson.
* The given .gem is installed again when multiple versions of the same gem
  exist in the current directory.  Bug #875 by Prem Sichanugrist.
* Local gems are preferred by name over remote gems again.  Bug #834 by
  jonforums.
* RubyGems can install local prerelease gems again.  Pull request #866 by
  Aaron Patterson.  Issue #813 by André Arko.
* RubyGems installs development dependencies correctly again.  Issue #893 by
  Jens Wille.
* RubyGems only installs prerelease versions when they are requested again.
  Issue #853 by Seth Vargo, special thanks to Zachary Scott and Ben Moss.
  Issue #884 by Nathaniel Bibler.
* Fixed RubyGems list and search command help.  Pull request #905 and #928 by
  Gabriel Gilder.
* The list of gems to uninstall is always sorted now.  Bug #918 by postmodern.
* The update command only updates exactly matching gem names now.  Bug #919 by
  postmodern.
* Gem::Server now supports prerelease versions.  Bug #857 by Marcelo Alvim.
* RubyGems no longer raises an exception immediately when gems are missing
  with RUBYGEMS_GEMDEPS.  A warning is printed instead.  Issue #886 by Michael
  Kaiser-Nyman.
* Commands using the rubygems.org API no longer try to sign-in when a
  non-rubygems API key has been chosen.  Bug #826 by Ben Sedat.
* Updated documentation of Gem::Specification#executables to indicate that
  only ruby scripts are allowed.  Bug #830 by Geoff Nixon.
* Gem dependency API supports multiple platforms for #platform and #platforms
  now.  Bug #821 by johnny5-.
* Gem dependency API supports lockfiles without explicit sources.  Bug #820 by
  johnny5-.
* Gem dependency API supports lockfiles with multiple sources.  Bug #822 by
  johnny5-, bug #851 by sumit shah.
* Gem dependency API supports lockfiles with git sources using branch, tag and
  ref.  Bug #822 by johnny5-, #931 by Christoph Blank.
* Gem dependency API no longer raises an exception when a gem does not exist
  in one of the configured sources.  Bug #897 by Michael Kaiser-Nyman.
* Gem dependency API no longer lists development dependencies in the lockfile.
  Bug #768 by Diego Viola, #916 by Santiago Pastorino.
* SSL configuration entries in ~/.gemrc are properly round-tripped.  Bug #837
  by Noah Luck Easterly.
* The environment command now shows the system configuration directory where
  the all-users gemrc lives.  Bug #827 by Ben Langfeld.
* Improved speed of conflict checking when activating gems.  Pull request #843
  by Aaron Patterson.
* Improved speed of levenshtein distance for gem suggestion misspellings.
  Pull requests #809, #812 by Aaron Patterson.
* Restored persistent connections.  Pull request #869 by Aaron Patterson.
* Reduced requests when fetching gems with the bundler API.  Pull request #773
  by Charlie Somerville.
* Reduced dependency prefetching to improve install speed.  Pull requests
  #871, #872 by Matthew Draper.
* RubyGems now avoids net/http auto-proxy detection.  Issue #824 by HINOHARA
  Hiroshi.
* Removed conversion of Gem::List (used for debugging installs) to unless
  necessary.  Pull request #870 by Aaron Patterson.
* RubyGems now prints release notes from the current release.  Bug #814 by
  André Arko.
* RubyGems allows installation of unsigned gems again with -P MediumSecurity
  and lower.  Bug #859 by Justin S. Collins.
* Fixed typo in Jim Weirich's name.  Ruby pull request #577 by Mo Khan.
* Fixed typo in Gem.datadir documentation.  Pull request #868 by Patrick
  Jones.
* Fixed File.exists? warnings.  Pull request #829 by SHIBATA Hiroshi.
* Fixed show_release_notes test for LANG=C.  Issue #862 by Luis Lavena.
* Fixed Gem::Package from IO tests on windows.  Patch from issue #861 by Luis
  Lavena.
* Check for nil extensions as BasicSpecification does not initialize them.
  Pull request #882 by André Arko.
* Fixed Gem::BasicSpecification#require_paths receives a String for
  @require_paths. Pull request #904 by @danielpclark
* Fixed circular require warnings.  Bug #908 by Zachary Scott.
* Gem::Specification#require_paths can no longer accidentally be an Array.
  Pull requests #904, #909 by Daniel P. Clark.
* Don't build extensions if `build_dir/extensions` isn't writable.
  Pull request #912 by @dunric
* Gem::BasicSpecification#require_paths respects default_ext_dir_for now.  Bug
  #852 by Vít Ondruch.

# 2.2.5 / 2015-06-08

## Bug fixes:

* Tightened API endpoint checks for CVE-2015-3900

# 2.2.4 / 2015-05-14

## Bug fixes:

* Backport: Limit API endpoint to original security domain for CVE-2015-3900.
  Fix by claudijd

# 2.2.3 / 2014-12-21

## Bug fixes:

* Backport: Add alternate Root CA for upcoming certificate change.
  Fixes #1050 by Protosac

# 2.2.2 / 2014-02-05

## Bug fixes:

* Fixed ruby tests when BASERUBY is not set.  Patch for #778 by Nobuyoshi
  Nakada.
* Removed double requests in RemoteFetcher#cache_update_path to improve remote
  install speed.  Pull request #772 by Charlie Somerville.
* The mkmf.log is now placed next to gem_make.out when building extensions.
* `gem install -g --local` no longer accesses the network.  Bug #776 by Jeremy
  Evans.
* RubyGems now correctly handles URL passwords with encoded characters.  Pull
  request #781 by Brian Fletcher.
* RubyGems now correctly escapes URL characters.  Pull request #788 by Brian
  Fletcher.
* RubyGems can now unpack tar files where the type flag is not given.  Pull
  request #790 by Cody Russell.
* Typo corrections.  Pull request ruby/ruby#506 by windwiny.
* RubyGems now uses both the default certificates and ssl_ca_cert instead of
  one or the other.  Pull request #795 by zebardy.
* RubyGems can now use the bundler API against hosted gem servers in a
  directory.  Pull request #801 by Brian Fletcher.
* RubyGems bin stubs now ignore non-versions.  This allows RubyGems bin stubs
  to list file names like "_foo_".  Issue #799 by Postmodern.
* Restored behavior of Gem::Version::new when subclassed.  Issue #805 by
  Sergio Rubio.

# 2.2.1 / 2014-01-06

## Bug fixes:

* Platforms in the Gemfile.lock GEM section are now handled correctly.  Bug
  #767 by Diego Viola.
* RubyGems now displays which gem couldn't be uninstalled from the home
  directory.  Pull request #757 by Michal Papis.
* Removed unused method Gem::Resolver#find_conflict_state.  Pull request #759
  by Smit Shah.
* Fixed installing gems from local files without dependencies.  Issue #760 by
  Arash Mousavi, pull request #764 by Tim Moore.
* Removed TODO about syntax that works in Ruby 1.8.7.  Pull request #765 by
  Benjamin Fleischer.
* Switched Gem.ruby_api_version to use RbConfig::CONFIG['ruby_version'] which
  has the same value but is overridable by packagers through
  --with-ruby-version= when configuring ruby.  Bug #770 by Jeremy Evans.
* RubyGems now prefers the bundler API for `gem install` to reduce HTTP
  requests.  (This change was intended for RubyGems 2.2.0 but was missed.)
  This should address bug #762 by Dan Peterson and bug #766 by mipearson.
* Added Gem::BasicSpecification#source_paths so documentation or analysis
  tools can work properly as require_paths no longer returns extension source
  directories.  Bug #758 Vít Ondruch.
* Gem.read_binary can read read-only files again.  This caused file://
  repositories to stop working.  Bug #761 by John Anderson.
* Fixed specification file sorting for Ruby 1.8.7 compatibility.  Pull
  request #763 by James Mead

# 2.2.0 / 2013-12-26

Special thanks to Vít Ondruch and Michal Papis for testing and finding bugs in
RubyGems as it was prepared for the 2.2.0 release.

## Enhancements:

* RubyGems can check for gem dependencies files (gem.deps.rb or Gemfile) when
  rubygems executables are started and uses the found dependencies.  This
  means `rake` will work similar to `bundle exec rake`.  To enable this set
  the `RUBYGEMS_GEMDEPS` environment variable to the location of your
  dependencies file.

  See Gem::use_gemdeps for further details.

* A RubyGems directory may now be shared amongst multiple ruby versions.  Upon
  activation RubyGems will automatically compile missing extensions for the
  current platform when the built objects are missing.  Issue #596 by Michal
  Papis

  By default different platforms do not share gem install locations so this
  must be configured by setting GEM_HOME to a common directory.  Some gems use
  fixed paths for requiring extensions and are not compatible with sharing gem
  directories.

  The default sharing location may be configured by RubyGems packagers through
  Gem.default_ext_dir_for.  Pull Request #744 by Vít Ondruch.

* RubyGems checks the 'allowed_push_host' metadata value when pushing a gem to
  prevent an accidental push to a public repository (such as rubygems.org).
  If you have private gems you should set this value in your gem specification
  metadata.  Pull request #603 by Seamus Abshere.
* `gem list` now shows results for multiple arguments.  Pull request #604 by
  Zach Rabinovich.
* `gem pristine --extensions` will restore only gems with extensions.  Issue
  #619 by Postmodern.
* Gem::Specification#files is now sorted.  Pull request #612 by Justin George.
* For `gem list` and friends, "LOCAL" and "REMOTE" headers are omitted if
  only local or remote gem information is requested with --quiet.  Pull
  request #615 by Michal Papis.
* Added Gem::Specification#full_require_paths which is like require_paths, but
  returns a fully-qualified results.  Pull request #632 by Vít Ondruch.
* RubyGems now looks for the https_proxy environment variable for https://
  sources.  RubyGems will fall back to http_proxy if there is no https_proxy.
  Issue #610 by mkristian.
* RubyGems now creates directories in .gem files.  Issue #631 by marksolaris.
* RubyGems raises an exception when a specification includes its gem.  Issue
  #623 by notEthan.
* RubyGems now displays relevant release note information when updating
  RubyGems.  Issue #647 by Trevor Wennblom.
* Deprecated Gem::Installer::ExtensionBuildError in favor of
  Gem::Ext::BuildError.  The old constant is an alias for the new constant.
* When extensions are built the gem_make.out file is always written now, even
  on success.  This will help with debugging bad builds that report success.
* If a specification fails to validate RubyGems shows a link to the
  specification reference guide.  Issue #656 by Markus Heiler.
* When using `gem install -g`, RubyGems now detects the presence of an
  Isolate, Gemfile or gem.deps.rb file.
* Added Gem::StubSpecification#stubbed? to help determine if a user should run
  `gem pristine` to speed up gem loading.  Pull request #694 and #701 by Jon
  Leighton.
* RubyGems now warns when a gem has a pessimistic version dependency that may
  be too strict.
* RubyGems now warns when a gem has an open-ended dependency.
* RubyGems now raises an exception when a dependency for a gem is defined
  twice.
* Marked the license specification attribute as recommended.  Pull request
  #713 by Benjamin Fleischer.
* RubyGems uses io/console instead of `stty` when available.  Pull request
  #740 by Nobuyoshi Nakada
* Relaxed Gem.ruby tests for platforms that override where ruby lives.  Pull
  Request #755 by strzibny.

## Bug fixes:

* RubyGems now returns an error status when any file given to `gem which`
  cannot be found.  Ruby bug #9004 by Eugene Vilensky.
* Fixed command escaping when building rake extensions.  Pull request #721 by
  Dmitry Ratnikov.
* Fixed uninstallation of gems when GEM_HOME is a relative directory.  Issue
  #708 by Ryan Davis.
* Default gems are now ignored by Gem::Validator#alien.  Issue #717 by David
  Bahar.
* Fixed typos in RubyGems.  Pull requests #723, #725, #731 by Akira Matsuda,
  pull request #736 by Leo Gallucci, pull request #746 by DV Suresh.
* RubyGems now holds exclusive locks on cached gem files to prevent incorrect
  updates.  Pull Request #737 by Smit Shah
* Improved speed of `gem install --ignore-dependencies`.  Patch by Terence
  Lee.

# 2.1.11 / 2013-11-12

## Bug fixes:

* Gem::Specification::remove_spec no longer checks for existence of the spec
  to be removed.  Issue #698 by Tiago Macedo.
* Restored wildcard handling when installing gems.  Issue #697 by Chuck Remes.
* Added DigiCert High Assurance EV Root CA certificate for the cloudfront.net
  certificate change.
* The Gem::RemoteFetcher tests now choose the test server port more reliably.
  Pull Request #706 by akr.

# 2.1.10 / 2013-10-24

## Bug fixes:

* Use class check instead of :version method check when creating Gem::Version
  objects.  Fixes #674 by jkanywhere.
* Fail during `gem update` when an error occurs checking for newer versions.
  This means RubyGems no longer reports "nothing to update" when it cannot
  communicate with the server.  Issue #688 by Jimmy Dee.
* Allow installation of gems when the home directory does not exist.  Issue
  #689 by Laurence Rowe
* Fix updating gems which have multiple platforms.  Issue #693 by Ookami
  Kenrou.
* The gem server now uses user-provided directories.  Issue #696 by Marcelo
  Alvim.
* Improved resolution of gems when specific versions have conflicting
  dependencies.
* RubyGems installs local gems regardless of platform again.  Issue #695
* The --ignore-dependencies option for gem installation works again.  Issue
  #695

# 2.1.9 / 2013-10-14

## Bug fixes:

* Reduce sorting when fetching specifications.  This speeds up the update and
  outdated commands, and others.  Issue #657 by windwiny.
* Proxy usernames and passwords are now escaped properly.  Ruby Bug #8979 by
  Masahiro Tomita, Issue #668 by Kouhei Sutou.

# 2.1.8 / 2013-10-10

## Bug fixes:

* Fixed local installation of platform gem files.  Issue #664 by Ryan Melton.
* Files starting with "." in the root directory are installed again.  Issue
  #680 by Ivo Wever, Pull Request #681 by Jeremy Evans.
* The index generator no longer indexes default gems.  Issue #661 by
  Jeremy Hinegardner.

# 2.1.7 / 2013-10-09

## Bug fixes:

* `gem sources --list` now displays a list of sources.  Pull request #672 by
  Nathan Marley.
* RubyGems no longer alters Gem::Specification.dirs when installing.  Pull
  Request #670 by Vít Ondruch
* Use RFC 2616-compatible time in HTTP headers.  Pull request #655 by Larry
  Marburger.
* RubyGems now gives a more descriptive message for missing licenses on
  validation.  Issue #656 by Markus Heiler.
* Expand unpack destination directory.  This fixes problems when File.realpath
  is missing and $GEM_HOME contains "..".  Issue #679 by Charles Nutter.

# 2.1.6 / 2013-10-08

## Bug fixes:

* Added certificates to follow the s3.amazonaws.com certificate change.  Fixes
  #665 by emeyekayee.  Fixes #671 by jonforums.
* Remove redundant built-in certificates not needed for https://rubygems.org
  Fixes #654 by Vít Ondruch.
* Added test for missing certificates for https://s3.amazonaws.com or
  https://rubygems.org.  Pull request #673 by Hannes Georg.
* RubyGems now allows a Pathname for Kernel#require like the built-in
  Kernel#require.  Pull request #663 by Aaron Patterson.
* Required rbconfig in Gem::ConfigFile for Ruby 1.9.1 compatibility.  (Ruby
  1.9.1 is no longer receiving security fixes, so please update to a newer
  version.)  Issue #676 by Michal Papis.  Issue wayneeseguin/rvm#2262 by
  Thomas Sänger.

# 2.1.5 / 2013-09-24

Security fixes:

* RubyGems 2.1.4 and earlier are vulnerable to excessive CPU usage due to a
  backtracking in Gem::Version validation.  See CVE-2013-4363 for full details
  including vulnerable APIs.  Fixed versions include 2.1.5, 2.0.10, 1.8.27 and
  1.8.23.2 (for Ruby 1.9.3).

# 2.1.4 / 2013-09-17

## Bug fixes:

* `gem uninstall foo --all` now force-uninstalls all versions of foo.  Issue
  #650 by Kyle (remkade).
* Fixed uninstalling gems installed in the home directory (as in
  `--user-install`).  Issue #653 by Lin Jen-Shin.

# 2.1.3 / 2013-09-12

## Bug fixes:

* Gems with files entries starting with "./" no longer install 0 files.  Issue
  #644 by Darragh Curran, #645 by Brandon Turner, #646 by Alex Tambellini

# 2.1.2 / 2013-09-11

## Bug fixes:

* Restore concurrent requires following the fix for ruby bug #8374.  Pull
  request #637 and issue #640 by Charles Nutter.
* Gems with extensions are now installed correctly when the --install-dir
  option is used.  Issue #642 by Lin Jen-Shin.
* Gem fetch now fetches the newest (not oldest) gem when --version is given.
  Issue #643 by Brian Shirai.

# 2.1.1 / 2013-09-10

## Bug fixes:

* Only matching gems matching your local platform are considered for
  installation.  Issue #638 by José M. Prieto, issue #639 by sawanoboly.

# 2.1.0 / 2013-09-09

Security fixes:

* RubyGems 2.0.7 and earlier are vulnerable to excessive CPU usage due to a
  backtracking in Gem::Version validation.  See CVE-2013-4287 for full details
  including vulnerable APIs.  Fixed versions include 2.0.8, 1.8.26 and
  1.8.23.1 (for Ruby 1.9.3).  Issue #626 by Damir Sharipov.

## Enhancements:

* RubyGems uses a new dependency resolver for gem installation which works
  similar to the bundler resolver.  The new resolver can resolve conflicts the
  previous resolver could not and offers improved diagnostics when conflicts
  are discovered.

* RubyGems now has improved platform matching for the ARM architecture.  Gems
  built with a CPU of "arm" will match any specific ARM CPU.  See `gem help
  platform` for further details.  Fixes #532 by Kim Burgestrand.
* The --version option now accepts compound requirements the same as in a gem
  dependency.  The following invocation will install rails between 4.0.0.beta
  and 4.2:

    gem install rails -v '>= 4.0.0.beta, < 4.2'

  Fixes #531 by Gary S. Weaver
* `gem clean` now allows `-n` as an alias for `--dryrun`.  Pull Request #517
  by Gastón Ramos
* Added `gem update --system` to `gem help`.  Pull Request #514 by Vince
  Wadhwani
* Added PATH to `gem env` output.  Pull Request #490 by Michal Papis
* Added --host option to `gem owner` to match other commands using the
  gemcutter API.  Pull Request #462 and issue #461 by Hugo Lopes Tavares
* Added --abort-on-dependent to `gem uninstall`.  This will abort instead of
  asking to uninstall a gem that is depended upon by another gem.  Pull
  request #549 by Philip Arndt.
* RubyGems no longer alters Gem::Specification.dirs when installing.  Based on
  Pull Request #452 by Vít Ondruch
* RubyGems uses ENV['MAKE'] or ENV['make'] over rbconfig.rb's make if present.
  Pull Request #443 by Erik Hollensbe
* RubyGems can now save remote source cache files in an alternate directory
  controlled by `ENV["GEM_SPEC_CACHE"]`.  Pull Request #489 by Michal Papis
* Generated private keys are now encrypted.  Pull Request #453 by pietro
* Separated Gem::Request from Gem::RemoteFetcher.  Pull Request #283 by Steve
  Klabnik.
* RubyGems indicates when a .gem's content is corrupt while verifying.  Bug
  #519 by William T Nelson.
* Refactored common installer setup.  Pull request #520 by Gastón Ramos
* Moved activation tests to Gem::Specification.  Pull request #521 by Gastón
  Ramos
* When a --version option with a prerelease version is given RubyGems
  automatically enables prerelease versions but only the last version is
  used.  If the first version is a prerelease version this is no longer sticky
  unless an explicit --[no-]prerelease was also given.  Fixes part of #531.
* RubyGems now supports an SSL client certificate.  Pull request #550 by
  Robert Kenny.
* RubyGems now suggests how to fix permission errors.  Pull request #553 by
  Odin Dutton.
* Added support for installing a gem as default gems for alternate ruby
  implementations.  Pull request #566 by Charles Nutter.
* Improved performance of Gem::Specification#load by caching the loaded
  gemspec.  Pull request #569 by Charlie Somerville.
* RubyGems now warns when an unsigned gem is verified if -P was given during
  installation even if the security policy allows unsigned gems and warns when
  an untrusted certificate is seen even if the security policy allows
  untrusted certificates.  Issue #474 by Grant Olson
* RubyGems can now rewrite executables with or without a shebang of
  /usr/bin/env via <code>gem pristine --all --only-executables
  --env-[no-]shebang</code>.  Issue #579 by Paul Annesley.
* RubyGems can now run its tests without OpenSSL.  Ruby Bug #8557 by nobu.
* Improved performance by caching Gem::Version objects and avoiding
  method_missing in Gem::Specification.  Pull request #447 by Jon Leighton.
* Files in a .gem now preserve their modification times.  Pull request #582 by
  Jesse Bowes
* Improved speed of looking up dependencies in SpecFetcher through
  Array#bsearch (when present).  Pull request #595 by Andras Suller
* Added `--all` option to `gem uninstall` which removes all gems in GEM_HOME.
  Pull request #584 by Shannon Skipper.
* Added Gem.find_latest_files which is equivalent to Gem.find_files but only
  returns matching files from the latest version of each gem.  Issue #186 by
  Ryan Davis.
* Improved performance of `gem outdated` by reducing duplicate work (it is
  still slow, but I see a near 50% improvement for 250 gems on a fast
  connection).  See also Gem::Specification::outdated_and_latest_version

## Bug fixes:

* rubygems_plugin.rb files are now only loaded from the latest installed gem.
* Fixed Gem.clear_paths when Security is defined at top-level.  Pull request
  #625 by elarkin
* Fixed credential creation for `gem push` when `--host` is not given.  Pull
  request #622 by Arthur Nogueira Neves

# 2.0.17 / 2015-06-08

## Bug fixes:

* Tightened API endpoint checks for CVE-2015-3900

# 2.0.16 / 2015-05-14

## Bug fixes:

* Backport: Limit API endpoint to original security domain for CVE-2015-3900.
  Fix by claudijd

# 2.0.15 / 2014-12-21

## Bug fixes:

* Backport: Add alternate Root CA for upcoming certificate change.
  Fixes #1050 by Protosac

# 2.0.14 / 2013-11-12

## Bug fixes:

* Gem::Specification::remove_spec no longer checks for existence of the spec
  to be removed.  Issue #698 by Tiago Macedo.
* Restored wildcard handling when installing gems.  Issue #697 by Chuck Remes.
* Added DigiCert High Assurance EV Root CA certificate for the cloudfront.net
  certificate change.
* The Gem::RemoteFetcher tests now choose the test server port more reliably.
  Pull Request #706 by akr.

# 2.0.13 / 2013-10-24

## Bug fixes:

* Use class check instead of :version method check when creating Gem::Version
  objects.  Fixes #674 by jkanywhere.
* Allow installation of gems when the home directory does not exist.  Issue
  #689 by Laurence Rowe
* Fix updating gems which have multiple platforms.  Issue #693 by Ookami
  Kenrou.

# 2.0.12 / 2013-10-14

## Bug fixes:

* Proxy usernames and passwords are now escaped properly.  Ruby Bug #8979 by
  Masahiro Tomita, Issue #668 by Kouhei Sutou.

# 2.0.11 / 2013-10-08

## Bug fixes:

* Added certificates to follow the s3.amazonaws.com certificate change.  Fixes
  #665 by emeyekayee.  Fixes #671 by jonforums.
* Remove redundant built-in certificates not needed for https://rubygems.org
  Fixes #654 by Vít Ondruch.
* Added test for missing certificates for https://s3.amazonaws.com or
  https://rubygems.org.  Pull request #673 by Hannes Georg.
* RubyGems now allows a Pathname for Kernel#require like the built-in
  Kernel#require.  Pull request #663 by Aaron Patterson.
* Required rbconfig in Gem::ConfigFile for Ruby 1.9.1 compatibility.  (Ruby
  1.9.1 is no longer receiving security fixes, so please update to a newer
  version.)  Issue #676 by Michal Papis.  Issue wayneeseguin/rvm#2262 by
  Thomas Sänger.

# 2.0.10 / 2013-09-24

Security fixes:

* RubyGems 2.1.4 and earlier are vulnerable to excessive CPU usage due to a
  backtracking in Gem::Version validation.  See CVE-2013-4363 for full details
  including vulnerable APIs.  Fixed versions include 2.1.5, 2.0.10, 1.8.27 and
  1.8.23.2 (for Ruby 1.9.3).

# 2.0.9 / 2013-09-13

## Bug fixes:

* Gem fetch now fetches the newest (not oldest) gem when --version is given.
  Issue #643 by Brian Shirai.
* Fixed credential creation for `gem push` when `--host` is not given.  Pull
  request #622 by Arthur Nogueira Neves

# 2.0.8 / 2013-09-09

Security fixes:

* RubyGems 2.0.7 and earlier are vulnerable to excessive CPU usage due to a
  backtracking in Gem::Version validation.  See CVE-2013-4287 for full details
  including vulnerable APIs.  Fixed versions include 2.0.8, 1.8.26 and
  1.8.23.1 (for Ruby 1.9.3).  Issue #626 by Damir Sharipov.

## Bug fixes:

* Fixed Gem.clear_paths when Security is defined at top-level.  Pull request
  #625 by elarkin

# 2.0.7 / 2013-08-15

## Bug fixes:

* Extensions may now be built in parallel (therefore gems may be installed in
  parallel).  Bug #607 by Hemant Kumar.
* Changed broken link to RubyGems Bookshelf to point to RubyGems guides.  Ruby
  pull request #369 by 謝致邦.
* Fixed various test failures due to platform differences or poor tests.
  Patches by Yui Naruse and Koichi Sasada.
* Fixed documentation for Kernel#require.

# 2.0.6 / 2013-07-24

## Bug fixes:

* Fixed the `--no-install` and `-I` options to `gem list` and friends.  Bug
  #593 by Blargel.
* Fixed crash when installing gems with extensions under the `-V` flag.  Bug
  #601 by Nick Hoffman.
* Fixed race condition retrieving HTTP connections in Gem::Request on JRuby.
  Bug #597 by Hemant Kumar.
* Fixed building extensions on ruby 1.9.3 under mingw.  Bug #594 by jonforums,
  Bug #599 by Chris Riesbeck
* Restored default of remote search to `gem search`.

# 2.0.5 / 2013-07-11

* Fixed building of extensions that run ruby in their makefiles.  Bug #589 by
  Zachary Salzbank.

# 2.0.4 / 2013-07-09

## Bug fixes:

* Fixed error caused by gem install not finding the right platform for your
  platform. Bug #576 by John Anderson
* Fixed pushing gems with the default host.  Bug #495 by Utkarsh Kukreti
* Improved unhelpful error message from `gem owner --remove`.  Bug #488 by
  Steve Klabnik
* Fixed typo in `gem spec` help.  Pull request #563 by oooooooo
* Fixed creation of build_info with --install-dir.  Bug #457 by Vít Ondruch.
* RubyGems converts non-string dependency names to strings now.  Bug #505 by
  Terence Lee
* Outdated prerelease versions are now listed in `gem outdated`.
* RubyGems now only calls fsync() on the specification when installing, not
  every file from the gem.  This improves the performance of gem installation
  on some systems.  Pull Request #556 by Grzesiek Kolodziejczyk
* Removed surprise search term anchoring in `gem search` to restore 1.8-like
  search behavior while still defaulting to --remote.  Pull request #562 by
  Ben Bleything
* Fixed handling of DESTDIR when building extensions.  Pull request #573 by
  Akinori MUSHA
* Fixed documentation of `gem pristine` defaults (--all is not a default).
  Pull request #577 by Shannon Skipper
* Fixed a windows extension-building test failure.  Pull request #575 by
  Hiroshi Shirosaki
* Fixed issue with `gem update` where it would attempt to use a Version
  instead of a Requirement to find the latest gem.  Fixes #570 by Nick Cox.
* RubyGems now ignores an empty but set RUBYGEMS_HOST environment variable.
  Based on pull request #558 by Robin Dupret.
* Removed duplicate creation of gem subdirectories in
  Gem::DependencyInstaller.  Pull Request #456 by Vít Ondruch
* RubyGems now works with Ruby built with `--with-ruby-version=''`.  Pull
  Request #455 by Vít Ondruch
* Fixed race condition when two threads require the same gem.  Ruby bug report
  #8374 by Joel VanderWerf
* Cleaned up siteconf between extension build and extension install.  Pull
  request #587 by Dominic Cleal
* Fix deprecation warnings when converting gemspecs to yaml.  Ruby commit
  r41148 by Yui Naruse

# 2.0.3 / 2013-03-11

## Bug fixes:
  * Reverted automatic upgrade to HTTPS as it breaks RubyGems APIs.  Fixes
    #506 by André Arko
  * Use File.realpath to remove extra / while checking if files are
    installable.  Issue #508 by Jacob Evans.
  * When installing RubyGems on JRuby, the standard library is no longer
    deleted.  Fixes #504 by Juan Sanchez, #507 by Charles Oliver Nutter.
  * When building extconf.rb extensions use the intermediate destination
    directory.  This addresses further issues with C extension building.
  * Use the absolute path to the generated siteconf in case the extension
    changes directories to run extconf.rb (like memcached).  Fixes #498 by
    Chris Morris.
  * Fixed default gem key and cert locations.  Pull request #511 by Samuel
    Cochran.

# 2.0.2 / 2013-03-06

## Bug fixes:
  * HTTPS URLs are preferred over HTTP URLs.  RubyGems will now attempt to
    upgrade any HTTP source to HTTPS.  Credit to Alex Gaynor.
  * SSL Certificates are now installed properly.  Fixes #491 by hemanth.hm
  * Fixed HTTP to HTTPS upgrade for rubygems.org.

# 2.0.1 / 2013-03-05

## Bug fixes:
  * Lazily load RubyGems.org API credentials to avoid failure during
    RubyGems installation.  Bug #465 by Isaac Sanders.
  * RubyGems now picks the latest prerelease to install.  Fixes bug #468 by
    Santiago Pastorino.
  * Improved detection of missing Zlib::GzipReader encoding support.  Works
    around JRuby-only bug #472 by Matt Beedle.
  * "Done installing documentation" is no longer displayed when documentation
    generation is disabled.  Fixes bug #469 by Jeff Sandberg
  * The existing executable check now respects --format-executable.  Pull
    request #471 by Jeremy Evans.
  * RubyGems no longer creates gem subdirectories when fetching gems.  Fixes
    #482 by Loren Segal.
  * RubyGems does not require OpenSSL like RubyGems 1.8, but still prefers it.
    Fixes #481 by André Arko.
  * RubyGems only fetches specs for list, search and query commands when
    needed like RubyGems 1.x.  Fixes bug #487 by bitbuerster, Ruby bug #8019
    by Ike Miller.
  * Allow specification of mode for gem subdirectory creation.
    Ruby bug #7713 by nobu
  * Fix tests when an 'a.rb' exists.  Ruby bug #7749 by nobu.

# 2.0.0 / 2013-02-24

RubyGems 2.0 includes several new features and many breaking changes.  Some of
these changes will cause existing software to break.  These changes are a
result of improvements to the internals of RubyGems that make it more
maintainable and improve APIs for RubyGems users.

If you are using bundler be sure to install a 1.3.0.prerelease version or
newer.  Older versions of bundler will not work with RubyGems 2.0.

Changes since RubyGems 1.8.25 (including past pre-releases):

## Breaking changes:

  * Deprecated Gem.unresolved_deps in favor of
    Gem::Specification.unresolved_deps
  * Merged Gem::Builder into Gem::Package.  Use Gem::Package.build(spec)
    instead of Gem::Builder.new(spec).build
  * Merged Gem::Format into Gem::Package.  Use Gem::Package.new instead
    of Gem::Format.from_file_by_path
  * Moved Gem::OldFormat to Gem::Package::Old.  Gem::Package will
    automatically detect old gems for you, so there is no need to refer to it.
  * Removed Gem::DocManager, replaced by Gem::RDoc and done_installing hook
  * Removed Gem::Package::TarInput in favor of Gem::Package
  * Removed Gem::Package::TarOutput in favor of Gem::Package
  * Removed Gem::RemoteFetcher#open_uri_or_path. (steveklabnik)
  * Removed Gem::SSL in favor of using OpenSSL directly
  * Removed Gem.loaded_path
  * Removed RSS generation from the gem indexer
  * Removed benchmark option from .gemrc
  * Removed broken YAML gemspec support in `gem build`
  * Removed support for Ruby 1.9.1
  * Removed many deprecated methods

## Enhancements:

  * Improved support for default gems shipping with ruby 2.0.0+
  * A gem can have arbitrary metadata through Gem::Specification#metadata
  * `gem search` now defaults to --remote and is anchored like gem list.  Fixes
    #166
  * Added --document to replace --rdoc and --ri.  Use --no-document to disable
    documentation, --document=rdoc to only generate rdoc.
  * Only ri-format documentation is generated by default.
  * `gem server` uses RDoc::Servlet from RDoc 4.0 to generate HTML
    documentation.
  * Add ability to install gems directly from a compatible gemdep
    file (Gemfile, Isolate, gem.deps.rb)
    <code>gem install --file path</code>
  * Add ability to load gem activation information from a gemdeps
    file (Gemfile, Isolate, gem.deps.rb).
    Set RUBYGEMS_GEMDEPS=path to have it loaded. Use - as the path
    to autodetect (current and parent directories are searched).
  * Added `gem check --doctor` to clean up after failed uninstallation.  Bug
    #419 by Erik Hollensbe
  * RubyGems no longer defaults to uninstalling gems if a dependency would be
    broken.  Now you must manually say "yes".  Pull Request #406 by Shannon
    Skipper.
  * Gem::DependencyInstaller now passes build_args down to the installer.
    Pull Request #412 by Sam Rawlins.
  * Added a cmake builder.  Pull request #265 by Allan Espinosa.
  * Removed rubyforge page from gem list output
  * Added --only-executables option to `gem pristine`.  Fixes #326
  * Added -I flag for 'gem query' to exclude installed items
  * Added Gem.install(name, version=default) for interactive sessions
  * Added Gem::FilePermissionError#directory
  * Added Gem::rubygems_version which is like Gem::ruby_version
  * Added RUBYGEMS_HOST documentation to `gem env`
  * Added a post_installs hook that runs after Gem::DependencyInstaller
    finishes installing a set of gems
  * Added a usage method for Gem::Commands::OwnerCommand. (ffmike)
  * Added an optional type parameter to Gem::Specification#doc_dir.
  * Added announcements url and clarified how to file tickets
  * Added guidance for how to use rdoc and ri in setup command. (jjb)
  * Attempting to install multiple gems with --version is now an error.  You
    can specify per-gem versions like <code>rake:0.9.5</code>
  * Clarified Gem::CommandManager example code to avoid multi load problems.
    (baroquebobcat)
  * Corrupt or bad cached specs are now re-downloaded. (cookrn)
  * Extension build arguments are saved from install and reused for pristine
  * If the OS allows it, documentation is built in a forked background
    process. (alexch)
  * Imported gem yank from the gemcutter gem.  Fixes #177, #343
  * Packaged gems now contain and verify SHA1 checksums
  * Removed commas from gem update summary so you can paste it back to
    cleanup.  (amatsuda)
  * RubyGems will now warn when building gems with prerelease dependencies.
    Fixes #255
  * The RUBYGEMS_HOST environment variable is used to determine appropriate
    API key for pushing or yanking gems
  * Uninstall is now performed in reverse topological order.
  * Users are told what to type when they try to uninstall a gem outside
    GEM_HOME
  * When building gems with non-world-readable files a warning is shown.

## Bug fixes:
  * Gem.refresh now maintains the active gem list.  Clearing the list would
    cause double-loads which would cause other bugs.  Pull Request #427 by
    Jeremy Evans
  * RubyGems now refuses to read the gem push credentials file if it has
    insecure permissions.  Pull Request #438 by Shannon Skipper
  * RubyGems now requires a local gem name to end in '.gem'.  Issue #407 by
    Santiago Pastorino.
  * Do not allow old-format gems to be installed with a security policy that
    verifies data.
  * Gem installation will fail if RubyGems cannot load the specification from
    the gem.  Bug #419 by Erik Hollensbe
  * RubyGems tests now run in FIPS mode.  Issue #365 by Vít Ondruch
  * Only update the spec cache when we have permission.  Ruby Bug #7509
  * gem install now ignores directories and non .gem files that match the gem
    to install.  Bug #407 by Santiago Pastorino.
  * Added PID to setup bin_file while installing RubyGems to protect against
    errors. Fixes #328 by ConradIrwin
  * Added missing require in Gem::Uninstaller when format_executable is set.
    (sakuro)
  * Exact gem command name matches are now chosen even if a longer command
    overlaps the exact name
  * Fixed Gem.loaded_path? with a Pathname instance. (mattetti)
  * Fixed Gem::Dependency.new mismatch with rubygems.org checks
  * Fixed SecurityError in Gem::Specification.load when $SAFE=1. (ged)
  * Fixed SystemStackError with "gem list -r -a" on 1.9 (cldwalker)
  * Fixed `gem owners` command so that exceptions don't stop the rest of the
    command from completing
  * Fixed `gem unpack uninstalled_gem` default version picker.
  * Fixed defunct rubyforge urls in gem command line help
  * Fixed documentation for the various hooks collections
  * Fixed documentation generation on setup when the gem directory does not
    exist.  Fixes #253
  * Fixed documentation to reflect where defaults overrides are loaded from.
    (ferrous26)
  * Fixed editing of a Makefile with 8-bit characters.  Fixes #181
  * Fixed gem loading issue caused by dependencies not resolving.
  * Fixed independent testing of test_gem_package_tar_output.  Ruby Bug #4686
    by Shota Fukumori
  * Fixed typo in uninstall message. (sandal)
  * Gem::Requirement#<=> returns nil on non-requirement arg.
  * Gem::Requirement.satisfied_by? raises ArgumentError if given a non-version
    argument
  * Gem::Version#initialize no longer modifies its parameter. (miaout17)
  * Group-writable permissions are now allowed for gem repositories. (ctcherry)
  * Memoized values in Gem::Specification are now reset the version or
    platform changes. Fixes #78
  * More specific errors are raised for bad requirements. (arsduo)
  * Removed reference to 'sources' gem in documentation
  * Removed unused block arguments to avoid creating Proc objects. (k-tsj)
  * RubyGems now asks before overwriting executable wrappers.  Ruby Bug #1800
  * The bindir is now created with mkdir_p during install. (voxik)
  * URI scheme matching is no longer case-sensitive.  Fixes #322
  * ext/builder now checks $MAKE as well as $make (okkez)

Changes since RubyGems 2.0.0.rc.2:

## Bug fixes:
  * Gem.gzip and Gem.gunzip now return strings with BINARY encoding.  Issue
    #450 by Jeremy Kemper
  * Fixed placement of executables with --user-install.  Ruby bug #7779 by Jon
    Forums.
  * Fixed `gem update` with --user-install.  Ruby bug #7779 by Jon Forums.
  * Fixed test_initialize_user_install for windows.  Ruby bug #7885 by Luis
    Lavena.
  * Create extension destination directory before building extensions.  Ruby
    Bug #7897 and patch by Kenta Murata.
  * Fixed verification of gems at LowSecurity due to missing signature.
    Thanks to André Arko.

# 2.0.0.rc.2 / 2013-02-08

## Bug fixes:
  * Fixed signature verification of gems which was broken only on master.
    Thanks to Brian Buchanan.
  * Proper exceptions are raised when verifying an unsigned gem.  Thanks to
    André Arko.

# 2.0.0.rc.1 / 2013-01-08

## Enhancements:
  * This release of RubyGems can push gems to rubygems.org.  Ordinarily
    prerelease versions of RubyGems cannot push gems.
  * Added `gem check --doctor` to clean up after failed uninstallation.  Bug
    #419 by Erik Hollensbe

## Bug fixes:
  * Fixed exception raised when attempting to push gems to rubygems.org.  Bug
    #418 by André Arko
  * Gem installation will fail if RubyGems cannot load the specification from
    the gem.  Bug #419 by Erik Hollensbe

# 2.0.0.preview2.2 / 2012-12-14

## Enhancements:
  * Added a cmake builder.  Pull request #265 by Allan Espinosa.
  * Removed rubyforge page from gem list output

## Bug fixes:
  * Restored RubyGems 1.8 packaging behavior of omitting directories.  Bug
    #413 by Jeremy Kemper.

# 2.0.0.preview2.1 / 2012-12-08

## Enhancements:
  * Gem::DependencyInstaller now passes build_args down to the installer.
    Pull Request #412 by Sam Rawlins.
  * RubyGems no longer defaults to uninstalling gems if a dependency would be
    broken.  Now you must manually say "yes".  Pull Request #406 by Shannon
    Skipper.

## Bug fixes:
  * RubyGems tests now run in FIPS mode.  Issue #365 by Vít Ondruch
  * Fixed Gem::Specification#base_dir for default gems.  Ruby Bug #7469
  * Only update the spec cache when we have permission.  Ruby Bug #7509
  * Restored order of version marking.  Fixes an issue with bundler.  Thanks
    to Aaron Patterson and Terence Lee.
  * Gem cleanup now skips default gems.  Pull Request #409 by Kouhei Sutou
  * gem list, search and query can show remote gems again.  Bug #410 by
    Henry Maddocks
  * gem install now ignores directories that match the gem to install.  Bug
    #407 by Santiago Pastorino.

# 2.0.0.preview2 / 2012-12-01

This release contains two commits not present in Ruby 2.0.0.preview2.  One
commit is for ruby 1.8.7 support, the second allows RubyGems to work under
$SAFE=1.  There is no functional difference compared to Ruby 2.0.0.preview2

## Breaking changes:

  * Deprecated Gem.unresolved_deps in favor of
    Gem::Specification.unresolved_deps
  * Merged Gem::Builder into Gem::Package.  Use Gem::Package.build(spec)
    instead of Gem::Builder.new(spec).build
  * Merged Gem::Format into Gem::Package.  Use Gem::Package.new instead
    of Gem::Format.from_file_by_path
  * Moved Gem::OldFormat to Gem::Package::Old.  Gem::Package will
    automatically detect old gems for you, so there is no need to refer to it.
  * Removed Gem::DocManager, replaced by Gem::RDoc and done_installing hook
  * Removed Gem::Package::TarInput in favor of Gem::Package
  * Removed Gem::Package::TarOutput in favor of Gem::Package
  * Removed Gem::RemoteFetcher#open_uri_or_path. (steveklabnik)
  * Removed Gem::SSL in favor of using OpenSSL directly
  * Removed Gem.loaded_path
  * Removed RSS generation from the gem indexer
  * Removed benchmark option from .gemrc
  * Removed broken YAML gemspec support in `gem build`
  * Removed support for Ruby 1.9.1
  * Removed many deprecated methods

## Enhancements:

  * Improved support for default gems shipping with ruby 2.0.0+
  * A gem can have arbitrary metadata through Gem::Specification#metadata
  * `gem search` now defaults to --remote and is anchored like gem list.  Fixes
    #166
  * Added --document to replace --rdoc and --ri.  Use --no-document to disable
    documentation, --document=rdoc to only generate rdoc.
  * Only ri-format documentation is generated by default.
  * `gem server` uses RDoc::Servlet from RDoc 4.0 to generate HTML
    documentation.
  * Add ability to install gems directly from a compatible gemdep
    file (Gemfile, Isolate, gem.deps.rb)
    <code>gem install --file path</code>
  * Add ability to load gem activation information from a gemdeps
    file (Gemfile, Isolate, gem.deps.rb).
    Set RUBYGEMS_GEMDEPS=path to have it loaded. Use - as the path
    to autodetect (current and parent directories are searched).
  * Added --only-executables option to `gem pristine`.  Fixes #326
  * Added -I flag for 'gem query' to exclude installed items
  * Added Gem.install(name, version=default) for interactive sessions
  * Added Gem::FilePermissionError#directory
  * Added Gem::rubygems_version which is like Gem::ruby_version
  * Added RUBYGEMS_HOST documentation to `gem env`
  * Added a post_installs hook that runs after Gem::DependencyInstaller
    finishes installing a set of gems
  * Added a usage method for Gem::Commands::OwnerCommand. (ffmike)
  * Added an optional type parameter to Gem::Specification#doc_dir.
  * Added announcements url and clarified how to file tickets
  * Added guidance for how to use rdoc and ri in setup command. (jjb)
  * Attempting to install multiple gems with --version is now an error.  You
    can specify per-gem versions like <code>rake:0.9.5</code>
  * Clarified Gem::CommandManager example code to avoid multi load problems.
    (baroquebobcat)
  * Corrupt or bad cached specs are now re-downloaded. (cookrn)
  * Extension build arguments are saved from install and reused for pristine
  * If the OS allows it, documentation is built in a forked background
    process. (alexch)
  * Imported gem yank from the gemcutter gem.  Fixes #177, #343
  * Packaged gems now contain and verify SHA1 checksums
  * Removed commas from gem update summary so you can paste it back to
    cleanup.  (amatsuda)
  * RubyGems will now warn when building gems with prerelease dependencies.
    Fixes #255
  * The RUBYGEMS_HOST environment variable is used to determine appropriate
    API key for pushing or yanking gems
  * Uninstall is now performed in reverse topological order.
  * Users are told what to type when they try to uninstall a gem outside
    GEM_HOME
  * When building gems with non-world-readable files a warning is shown.

## Bug fixes:

  * Added PID to setup bin_file while installing RubyGems to protect against
    errors. Fixes #328 by ConradIrwin
  * Added missing require in Gem::Uninstaller when format_executable is set.
    (sakuro)
  * Exact gem command name matches are now chosen even if a longer command
    overlaps the exact name
  * Fixed Gem.loaded_path? with a Pathname instance. (mattetti)
  * Fixed Gem::Dependency.new mismatch with rubygems.org checks
  * Fixed SecurityError in Gem::Specification.load when $SAFE=1. (ged)
  * Fixed SystemStackError with "gem list -r -a" on 1.9 (cldwalker)
  * Fixed `gem owners` command so that exceptions don't stop the rest of the
    command from completing
  * Fixed `gem unpack uninstalled_gem` default version picker.
  * Fixed defunct rubyforge urls in gem command line help
  * Fixed documentation for the various hooks collections
  * Fixed documentation generation on setup when the gem directory does not
    exist.  Fixes #253
  * Fixed documentation to reflect where defaults overrides are loaded from.
    (ferrous26)
  * Fixed editing of a Makefile with 8-bit characters.  Fixes #181
  * Fixed gem loading issue caused by dependencies not resolving.
  * Fixed independent testing of test_gem_package_tar_output.  Ruby Bug #4686
    by Shota Fukumori
  * Fixed typo in uninstall message. (sandal)
  * Gem::Requirement#<=> returns nil on non-requirement arg.
  * Gem::Requirement.satisfied_by? raises ArgumentError if given a non-version
    argument
  * Gem::Version#initialize no longer modifies its parameter. (miaout17)
  * Group-writable permissions are now allowed for gem repositories. (ctcherry)
  * Memoized values in Gem::Specification are now reset the version or
    platform changes. Fixes #78
  * More specific errors are raised for bad requirements. (arsduo)
  * Removed reference to 'sources' gem in documentation
  * Removed unused block arguments to avoid creating Proc objects. (k-tsj)
  * RubyGems now asks before overwriting executable wrappers.  Ruby Bug #1800
  * The bindir is now created with mkdir_p during install. (voxik)
  * URI scheme matching is no longer case-sensitive.  Fixes #322
  * ext/builder now checks $MAKE as well as $make (okkez)

# 1.8.29 / 2013-11-23

## Bug fixes:

* Fixed installation when the LANG environment variable is empty.
* Added DigiCert High Assurance EV Root CA to the default SSL certificates for
  cloudfront.

# 1.8.28 / 2013-10-08

## Bug fixes:

* Added the Verisign Class 3 Public Primary Certification Authority G5
  certificate and its intermediary to follow the s3.amazonaws.com certificate
  change.  Fixes #665 by emeyekayee.  Fixes #671 by jonforums.
* Remove redundant built-in certificates not needed for https://rubygems.org
  Fixes #654 by Vít Ondruch.
* Added test for missing certificates for https://s3.amazonaws.com or
  https://rubygems.org.  Pull request #673 by Hannes Georg.

# 1.8.27 / 2013-09-24

Security fixes:

* RubyGems 2.1.4 and earlier are vulnerable to excessive CPU usage due to a
  backtracking in Gem::Version validation.  See CVE-2013-4363 for full details
  including vulnerable APIs.  Fixed versions include 2.1.5, 2.0.10, 1.8.27 and
  1.8.23.2 (for Ruby 1.9.3).

# 1.8.26 / 2013-09-09

Security fixes:

* RubyGems 2.0.7 and earlier are vulnerable to excessive CPU usage due to a
  backtracking in Gem::Version validation.  See CVE-2013-4287 for full details
  including vulnerable APIs.  Fixed versions include 2.0.8, 1.8.26 and
  1.8.23.1 (for Ruby 1.9.3).  Issue #626 by Damir Sharipov.

## Bug fixes:

* Fixed editing of a Makefile with 8-bit characters.  Fixes #181

# 1.8.25 / 2013-01-24

## Bug fixes:
  * Added 11627 to setup bin_file location to protect against errors. Fixes
    #328 by ConradIrwin
  * Specification#ruby_code didn't handle Requirement with multiple
  * Fix error on creating a Version object with a frozen string.
  * Fix incremental index updates
  * Fix missing load_yaml in YAML-related requirement.rb code.
  * Manually backport encoding-aware YAML gemspec

# 1.8.24 / 2012-04-27

## Bug fixes:

  * Install the .pem files properly. Fixes #320
  * Remove OpenSSL dependency from the http code path

# 1.8.23.2 / 2013-09-24

Security fixes:

* RubyGems 2.1.4 and earlier are vulnerable to excessive CPU usage due to a
  backtracking in Gem::Version validation.  See CVE-2013-4363 for full details
  including vulnerable APIs.  Fixed versions include 2.1.5, 2.0.10, 1.8.27 and
  1.8.23.2 (for Ruby 1.9.3).

# 1.8.23.1 / 2013-09-09

Security fixes:

* RubyGems 2.0.7 and earlier are vulnerable to excessive CPU usage due to a
  backtracking in Gem::Version validation.  See CVE-2013-4287 for full details
  including vulnerable APIs.  Fixed versions include 2.0.8, 1.8.26 and
  1.8.23.1 (for Ruby 1.9.3).  Issue #626 by Damir Sharipov.

# 1.8.23 / 2012-04-19

This release increases the security used when RubyGems is talking to
an https server. If you use a custom RubyGems server over SSL, this
release will cause RubyGems to no longer connect unless your SSL cert
is globally valid.

You can configure SSL certificate usage in RubyGems through the
:ssl_ca_cert and :ssl_verify_mode options in ~/.gemrc and /etc/gemrc.
The recommended way is to set :ssl_ca_cert to the CA certificate for
your server or a certificate bundle containing your CA certification.

You may also set :ssl_verify_mode to 0 to completely disable SSL
certificate checks, but this is not recommended.


Security fixes:
  * Disallow redirects from https to http
  * Turn on verification of server SSL certs

## Enhancements:
  * Add --clear-sources to fetch

## Bug fixes:
  * Use File.identical? to check if two files are the same.
  * Fixed init_with warning when using psych

# 1.8.22 / 2012-04-13

## Bug fixes:

  * Workaround for psych/syck YAML date parsing issue
  * Don't trust the encoding of ARGV. Fixes #307
  * Quiet default warnings about missing spec variables
  * Read a binary file properly (windows fix)

# 1.8.21 / 2012-03-22

## Bug fixes:

  * Add workaround for buggy yaml output from 1.9.2
  * Force 1.9.1 to remove it's prelude code. Fixes #305

# 1.8.20 / 2012-03-21

## Bug fixes:

  * Add --force to `gem build` to skip validation. Fixes #297
  * Gracefully deal with YAML::PrivateType objects in Marshal'd gemspecs
  * Treat the source as a proper url base. Fixes #304
  * Warn when updating the specs cache fails. Fixes #300

# 1.8.19 / 2012-03-14

## Bug fixes:

  * Handle loading psych vs syck properly. Fixes #298
  * Make sure Date objects don't leak in via Marshal
  * Perform Date => Time coercion on yaml loading. Fixes #266

# 1.8.18 / 2012-03-11

## Bug fixes:

  * Use Psych API to emit more compatible YAML
  * Download and write inside `gem fetch` directly. Fixes #289
  * Honor sysconfdir on 1.8. Fixes #291
  * Search everywhere for a spec for `gem spec`. Fixes #288
  * Fix Gem.all_load_path. Fixes #171

# 1.8.17 / 2012-02-17

## Enhancements:

  * Add MacRuby to the list of special cases for platforms (ferrous26)
  * Add a default for where to install rubygems itself

## Bug fixes:

  * Fixed gem loading issue caused by dependencies not resolving.
  * Fixed umask error when stdlib is required and unresolved dependencies exist.
  * Shebang munging would only take one arg after the cmd
  * Define SUCKAGE better, ie only MRI 1.9.2
  * Propagate env-shebang to the pristine command if set for install.

# 1.8.16 / 2012-02-12

## Bug fixes:

  * Fix gem specification loading when encoding is not UTF-8. #146
  * Allow group writable if umask allows it already.
  * Uniquify the spec list based on directory order priority

# 1.8.15 / 2012-01-06

## Bug fixes:

  * Don't eager load yaml, it creates a bad loop. Fixes #256

# 1.8.14 / 2012-01-05

## Bug fixes:

  * Ignore old/bad cache data in Version
  * Make sure our YAML workarounds are loaded properly. Fixes #250.

# 1.8.13 / 2011-12-21

## Bug fixes:

  * Check loaded_specs properly when trying to satisfy a dep

## Enhancements:

  * Remove using #loaded_path? for performance
  * Remove Zlib workaround for Windows build.

# 1.8.12 / 2011-12-02

## Bug fixes:

  * Handle more cases where Syck's DefaultKey showed up in requirements
    and wasn't cleaned out.

# 1.8.11 / 2011-10-03

## Bug fixes:

  * Deprecate was moved to Gem::Deprecate to stop polluting the top-level
    namespace.

# 1.8.10 / 2011-08-25

RubyGems 1.8.10 contains a security fix that prevents malicious gems from
executing code when their specification is loaded.  See
https://github.com/rubygems/rubygems/pull/165 for details.

## Bug fixes:

  * RubyGems escapes strings in ruby-format specs using #dump instead of #to_s
    and %q to prevent code injection.  Issue #165 by Postmodern
  * RubyGems attempt to activate the psych gem now to obtain bugfixes from
    psych.
  * Gem.dir has been restored to the front of Gem.path.  Fixes remaining
    problem with Issue #115
  * Fixed Syck DefaultKey infecting ruby-format specifications.
  * `gem uninstall a b` no longer stops if gem "a" is not installed.

# 1.8.9 / 2011-08-23

## Bug fixes:

  * Fixed uninstalling multiple gems using `gem uninstall`
  * Gem.use_paths splatted to take multiple paths!  Issue #148

# 1.8.8 / 2011-08-11

## Bug fixes:
  * The encoding of a gem's YAML spec is now UTF-8.  Issue #149

# 1.8.7 / 2011-08-04

## Bug fixes:
  * Added missing require for `gem uninstall --format-executable`
  * The correct name of the executable being uninstalled is now displayed with
    --format-executable
  * Fixed `gem unpack uninstalled_gem` default version picker
  * RubyGems no longer claims a nonexistent gem can be uninstalled
  * `gem which` no longer claims directories are requirable files
  * `gem cleanup` continues cleaning up gems if one can't be uninstalled due
    to permissions.  Issue #82
  * Gem repository directories are no longer created world-writable.  Patch by
    Sakuro OZAWA.  Ruby Bug #4930

# 1.8.6 / 2011-07-25

## Enhancements:

  * Add autorequires and delay startup of RubyGems until require is called.
    See Ruby bug #4962

## Bug fixes:

  * Restore behavior of Gem::Specification#loaded?  Ruby Bug #5032
  * Clean up SourceIndex.add_specs to not be so damn noisy. (tadman)
  * Added missing APPLE_GEM_HOME in paths.
  * Extend YAML::Syck::DefaultKey fixing to `marshal_dump` as well.
  * Fix #29216: check correct bin_dir in check_that_user_bin_dir_is_in_path.
  * Revert Gem.latest_load_paths to working order (PathSupport revert).
  * Restore normalization of GEM_HOME.
  * Handle the Syck DefaultKey problem once and for all.
  * Fix SystemStackError occurring with "gem list -r -a" on 1.9.

# 1.8.5 / 2011-05-31

## Enhancements:

  * The -u option to 'update local source cache' is official deprecated.
  * Remove has_rdoc deprecations from Specification.

## Bug fixes:

  * Handle bad specs more gracefully.
  * Reset any Gem paths changed in the installer.

# 1.8.4 / 2011-05-25

## Enhancements:

  * Removed default_executable deprecations from Specification.

# 1.8.3 / 2011-05-19

## Bug fixes:

  * Fix independent testing of test_gem_package_tar_output.  Ruby Bug #4686 by
    Shota Fukumori
  * Fix test failures for systems with separate ruby versions.  Ruby Bug #3808
    by Jeremy Evans
  * Fixed some bad calls left behind after rolling out some refactorings.
  * Syck has a parse error on (good) times output from Psych. (dazuma, et al)

# 1.8.2 / 2011-05-11

## Enhancements:

  * Moved #outdated from OutdatedCommand to Specification (for Isolate).
  * Print out a warning about missing executables.

## Bug fixes:

  * Added missing requires to fix various upgrade issues.
  * `gem pristine` respects multiple gem repositories.
  * setup.rb now execs with --disable-gems when possible

# 1.8.1 / 2011-05-05

## Enhancements:

  * Added Gem::Requirement#specific? and Gem::Dependency#specific?

## Bug fixes:

  * Typo on Indexer rendered it useless on Windows
  * gem dep can fetch remote dependencies for non-latest gems again.
  * gem uninstall with multiple versions no longer crashes with ArgumentError
  * Always use binary mode for File.open to keep Windows happy

# 1.8.0 / 2011-04-34

This release focused on properly encapsulating functionality.  Most of this
work focused on moving functionality out of Gem::SourceIndex and
Gem::GemPathSearcher into Gem::Specification where it belongs.

After installing RubyGems 1.8.0 you will see deprecations when loading your
exsting gems.  Run `gem pristine --all --no-extensions` to regenerate your
gem specifications safely.

Currently RubyGems does not save the build arguments used to build gems with
extensions.  You will need to run `gem pristine gem_with_extension --
--build-arg` to regenerate a gem with an extension where it requires special
build arguments.

## Deprecations:

  * DependencyList.from_source_index deprecated the source_index argument.
  * Deprecated Dependency.new(/regex/).
  * Deprecated Gem.searcher.
  * Deprecated Gem.source_index and Gem.available?
  * Deprecated Gem: activate_dep, activate_spec, activate,
    report_activate_error, and required_location.
  * Deprecated Gem::all_partials
  * Deprecated Gem::cache_dir
  * Deprecated Gem::cache_gem
  * Deprecated Gem::default_system_source_cache_dir
  * Deprecated Gem::default_user_source_cache_dir
  * Deprecated Platform#empty?
  * Deprecated Specification.cache_gem
  * Deprecated Specification.installation_path
  * Deprecated Specification.loaded, loaded?, and loaded=
  * Deprecated all of Gem::SourceIndex.
  * Deprecated all of Gem::GemPathSearcher.
  * Deprecated Gem::Specification#default_executable.

## Enhancements:

  * Gem::SourceIndex functionality has been moved to Gem::Specification.
    Gem::SourceIndex is completely disconnected from Gem::Specification
  * Refactored GemPathSearcher entirely out. RIPMF
  * Added CommandManager#unregister_command
  * Added Dependency#matching_specs + to_specs.
  * Added Dependency#to_spec
  * Added Gem.pre_reset_hook/s and post_reset_hook/s.
  * Added GemCommand.reset to reinitialize the singleton
  * Added Specification#activate.
  * Added Specification#activated, activated=, and activated?
  * Added Specification#base_dir.
  * Added Specification#bin_dir and bin_file.
  * Added Specification#cache_dir and cache_file. Aliased cache_gem.
  * Added Specification#doc_dir and ri_dir.
  * Added Specification#find(name_or_dep, *requirements).
  * Added Specification#gem_dir and gems_dir.
  * Added Specification#spec_dir and spec_file.
  * Added Specification.add_spec, add_specs, and remove_spec.
  * Added Specification.all=. If you use this, we will light you on fire.
  * Added Specification.all_names.
  * Added Specification.dirs and dirs=. dirs= resets.
  * Added Specification.find_all_by_name(name, *reqs)
  * Added Specification.latest_specs. SO TINY!
  * Added TestCase#all_spec_names to help clean up tests
  * Added TestCase#assert_path_exists and refute_path_exists. Will move to
    minitest.
  * Gem.sources no longer tries to load sources gem. Only uses default_sources.
  * Installer no longer accepts a source_index option.
  * More low-level integration.
  * Removed Gem::FileOperations since it is a dummy class
  * Removed a comment because I am dumb
  * Removed pkgs/sources/lib/sources.rb
  * Revamped indexer to mostly not use SourceIndex (legacy index requires it).
  * Rewrote our last functional test suite to be happy and fast
  * RubyGems is now under the Ruby License or the MIT license
  * Specification#== now only checks name, version, and platform.
  * Specification#authors= now forcefully flattens contents (bad rspec! no
    cookie!)
  * Specification#eql? checks all fields.
  * Specification#installation_path no longer raises if it hasn't been
    activated.
  * Specification#validate now ensures that authors is not empty.
  * TestCase.util_setup_spec_fetcher no longer returns a SourceIndex.
  * Uninstaller no longer passes around SourceIndex instances
  * Warn on loading bad spec array values (ntlm-http gem has nil in its cert
    chain)
  * `gem pristine` now accepts --no-executables to skip restoring gems with
    extensions.
  * `gem pristine` can now restore multiple gems.

## Bug fixes:

  * DependencyInstaller passed around a source_index instance but used
    Gem.source_index.
  * Fixed Platform#== and #hash so instances may be used as hash keys.
  * Fixed broken Specification#original_platform. It should never be nil.
  * Gem::Text#format_text now strips trailing whitespace
  * Normalize LOAD_PATH with File.expand_path
  * `gem build` errors should exit 1.
  * `gem pristine` can now restore non-latest gems where the cached gem was
    removed.

# 1.7.1 / 2011-03-32

## Bug fixes:
  * Fixed missing file in Manifest.txt.  (Also a bug in hoe was fixed where
    `rake check_manifest` showing a diff would not exit with an error.)

# 1.7.0 / 2011-03-32

## Deprecations:
  * Deprecated Gem.all_load_paths, latest_load_paths, promote_load_path, and
    cache.
  * Deprecated RemoteFetcher#open_uri_or_path.
  * Deprecated SourceIndex#all_gems.
  * Deprecated SourceIndex#initialize(hash_of_specs).
  * Deprecated SourceIndex.from_installed_gems, from_gems_in, and
    load_specification.
  * Deprecated Specification#has_rdoc, default_executable, and
    test_suite_file(=).
  * Deprecated Specification#has_rdoc= and default_executable=

## Enhancements:
  * Added stupid simple deprecation module.
  * Added --spec option to `gem unpack` to output a gem's original metadata
  * Added packaging option to Specification#validate
  * Gem.bin_path requires the exec_name argument.
  * Read from cached specs if fetch fails for some reason
  * Refactored Specification#assign_defaults into #initialize.
  * RemoteFetcher#fetch_path now dispatches dynamically to 'fetch_<uri.schema>'
  * Removed Specification @@gather.
  * Removed Specification.attribute.
  * Removed Specification.attribute_alias_singular.
  * Removed Specification.attribute_defaults.
  * Removed Specification.attributes
  * Removed Specification.overwrite_accessor.
  * Removed Specification.read_only.
  * Removed Specification.required_attribute.
  * Removed Specification::SPECIFICATION_VERSION_HISTORY and turned into rdoc
  * Removed blanket rescue in default_executable. Hope it doesn't blow up! :P
  * Removed nearly all metaprogramming from Specification. Yay for
    attr_accessor!
  * SourceIndex#initialize changed to prefer an array of spec dirs, defaulting
    to none.
  * SourceIndex.new is now the preferred way to create SourceIndex instances.
    *gasp*
  * Specification#validate now checks that array attribs are indeed arrays.
  * Specification.default_value is now an instance method.
  * Switched Specification::TODAY to be proper midnight @ UTC
  * Update Gem::RemoteFetcher\'s User-Agent to handle RUBY_ENGINE and
    RUBY_REVISION when patchlevel is -1
  * UpdateCommand#gems_to_update now returns (name, version) pairs.
  * UpdateCommand#which_to_update now takes an optional system argument.

## Bug fixes:
  * Added missing remote fetcher require to pristine command (aarnell)
  * Building gems now checks to ensure all required fields are non-nil
  * Fix option parser when summary is nil.
  * Fixed `gem contents` to work with the lightweight specifications
  * Fixed `gem update --system x.y.z` where x.y.z == latest version. (MGPalmer)
  * Fixed gem contents sorting and tests. (MGPalmer)
  * Fixed intermittent problem in `gem fetch` with --platform specified (quix)
  * Fixed lightweight specifications so `gem rdoc` will generate proper
    documentation
  * MockGemUI#terminate_interaction should not raise Gem::SystemExitException.
    (MGPalmer)
  * RubyGems now raises a better error for broken .gem files.  Bug #29067 by
    Elias Baixas
  * `gem update` now uniq's command line arguments.

# 1.6.2 / 2011-03-08

## Bug fixes:

* require of an activated gem could cause activation conflicts.  Fixes
  Bug #29056 by Dave Verwer.
* `gem outdated` now works with up-to-date prerelease gems.

# 1.6.1 / 2011-03-03

## Bug fixes:

* Installation no longer fails when a dependency from a version that won't be
  installed is unsatisfied.
* README.rdoc now shows how to file tickets and get help.  Pull Request #40 by
  Aaron Patterson.
* Gem files are cached correctly again.  Patch #29051 by Mamoru Tasaka.
* Tests now pass with non-022 umask.  Patch #29050 by Mamoru Tasaka.

# 1.6.0 / 2011-02-29

## Deprecations:

* RubyGems no longer requires 'thread'.  Rails < 3 will need to add require
  'thread' to their applications.
* Gem.cache is deprecated.  Use Gem.source_index.
* RbConfig.datadir is deprecated.  Use Gem.datadir.
* Gem::LoadError#version_requirements has been removed.  Use
  Gem::LoadError#requirement.

## Enhancements:

* Rewrote how Gem::activate (gem and require) resolves dependencies.
* Gem::LoadError#version_requirement has been removed. Use
  Gem::LoadError#requirement.
* Added --key to `gem push` for setting alternate API keys.
* Added --format-executable support to gem uninstall.
* Added Gem::DependencyList#clear.
* Added Gem::DependencyList#remove_specs_unsatisfied_by
* Added Gem.latest_spec_for, latest_version_for, and latest_rubygems_version.
* Added Gem::Dependency#merge which merges requirements for two
  dependencies.
* Added Gem::TestCase#util_spec for faster tests.
* Added Gem::Specification#dependent_specs.
* Added Gem::TestCase#new_spec and Gem::TestCase#install_specs.
* Added flag to include prerelease gems in Gem::SourceIndex#latest_specs.
* Gem.cache_dir always references the proper cache dir.
  Pass true to support a user path.
* Gem.cache_gem, given a filename always references the cache gem.
  Pass true to support a user path.
* Added Gem::Specification#conflicts
* Removed rdoc gem/require from test_case.rb.
* Rubygems will no longer let you push if you're using beta or unreleased
  rubygems.
* Save RAM / GC churn by removing spec.files and rdoc options from
  locally cached gem specifications.
* SpecFetcher.fetch_spec can now take a string source_uri.

## Bug fixes:

* Added missing require of Gem::RemoteFetcher to the unpack command.
* RubyGems now completely removes a previous install when reinstalling.
* Fixed Gem::Installer#generate_bin to only chmod files that exist.
* Fixed handling of Windows style file:/// uris.
* Fixed requires in tests. (shota)
* Fixed script generation on Windows.
* Fixed test issues if you have older rubygems installed.
* Gem::DependencyInstaller tests use Gem::Security, add the missing require.
* Gem::Security used FileUtils but didn't require it.  Reported by Elia Schito.
* Gem::Uninstaller now respects --format-executable.

# 1.5.3 / 2011-02-26

## Bug fixes:

* Fix for a bug in Syck which causes install failures for gems packaged with
  Psych.  Bug #28965 by Aaron Patterson.

# 1.5.2 / 2011-02-10

## Bug fixes:

* Fixed <tt>gem update --system</tt>.  RubyGems can now update itself again.

# 1.5.1 / 2011-02-09

#= NOTE: `gem update --system` is broken. See UPGRADING.rdoc.

## Enhancements:

* Added ability to do gem update --system X.Y.Z.

## Bug fixes:

* Scrub !!null YAML from 1.9.2 (install and build).
* Added missing requires for user_interaction.
* Wrote option processing tests for gem update.
* Updated upgrading doco for new gem update --system option.
* Fixed SilentUI for cygwin; try /dev/null first then fall back to NUL.
* RubyGems now enforces ruby 1.8.7 or newer.

# 1.5.0 / 2011-01-31

#= NOTE: `gem update --system` is broken. See UPGRADING.rdoc.

## Enhancements:

* Finally fixed all known 1.9.x issues. Upgrading is now possible!
* Merged huge 1.3.7/ruby-core changes to master.
* Added UPGRADING.rdoc to help deal with 1.9 issues.
* Gem::Format now gives better errors for corrupt gem files and includes paths
* Pre-install hooks can now abort gem installation by returning false
* Move shareable TestCase classes to lib/ to help plugin authors with tests.
* Add post-build hooks that can cancel the gem install
* Always require custom_require now that require_gem is gone
* Added GemInstaller accessors for @options so plugins can reference them.
* Optimized Gem.find_files. ~10% faster than 1.4.2. ~40% faster than ruby 1.9.
* Gem::SilentUI now behaves like Gem::StreamUI for asking questions.  Patch by
  Erik Hollensbe.

## Bug fixes:

* `gem update` was implicitly doing --system.
* 1.9.3: Fixed encoding errors causing gem installs to die during rdoc phase.
* Add RubyForge URL to README. Closes #28825
* 1.9.3: Use chdir {} when building extensions to prevent warnings. Fixes #4337
* 1.9.2: Fix circular require warning.
* Make requiring openssl even lazier at request of NaHi
* `gem unpack` will now download the gem if it is not in the cache. Patch by
  Erik Hollensbe.
* rubygems-update lists its development dependencies again

# 1.4.2 / 2011-01-06

## Bug fixes:

* Gem::Versions: "1.b1" != "1.b.1", but "1.b1" eql? "1.b.1". Fixes gem indexing.
* Fixed Gem.find_files.
* Removed otherwise unused #find_all_dot_rb. Only 6 days old and hella buggy.

# 1.4.1 / 2010-12-31

Since apparently nobody reads my emails, blog posts or the README:

DO NOT UPDATE RUBYGEMS ON RUBY 1.9! See UPGRADING.rdoc for details.

## Bug fixes:

* Specification#load was untainting a frozen string (via `gem build *.spec`)

# 1.4.0 / 2010-12-30

NOTE: In order to better maintain rubygems and to get it in sync with
the world (eg, 1.9's 1.3.7 is different from our 1.3.7), rubygems is
switching to a 4-6 week release schedule. This release is the
precursor to that process and as such may be a bit on the wild side!
You have been warned!

NOTE: We've switched to git/github. See README.rdoc for details.

## Features:

* Added --launch option to `gem server`. (gthiesfeld)
* Added fuzzy name matching on install failures. (gstark/presidentbeef)
* Allow searching w/ file extensions: gem which fileutils.rb
* Progress indicator during download (Ryan Melton)
* Speed up Gem::Version#<=> by 2-3x in common cases. (raggi)
* --source is now additive with your current sources.
  Use --clear-sources first to maintain previous behavior.

## Bug fixes:

* Dependency "~>"s now respect lower-bound prerelease versions.
* Ensure the gem directories exist on download.
* Expand Windows user home candidates for Ruby 1.8. Bug #28371 & #28494
* Fix find_files to order by version.
* Fix ivar typo. [Josh Peek]
* Normalized requires and made many of them lazy.
  Do not depend on rubygems to require stdlib stuff for you. (raggi/tmm1)
* Treat 1.0.a10 like 1.0.a.10 for sorting, etc. Fixes #27903. (dchelimsky)

# 1.3.7 / 2010-05-13

NOTE:

https://rubygems.org/ is now the default source for downloading gems.

You may have sources set via ~/.gemrc, so you should replace
http://gems.rubyforge.org with https://rubygems.org/

http://gems.rubyforge.org will continue to work for the foreseeable future.

## Features:

* `gem` commands
  * `gem install` and `gem fetch` now report alternate platforms when a
    matching one couldn't be found.
  * `gem contents` --prefix is now the default as specified in --help.  Bug
    #27211 by Mamoru Tasaka.
  * `gem fetch` can fetch of old versions again.  Bug #27960 by Eric Hankins.
  * `gem query` and friends output now lists platforms.  Bug #27856 by Greg
    Hazel.
  * `gem server` now allows specification of multiple gem dirs for
    documentation.  Bug #27573 by Yuki Sonoda.
  * `gem unpack` can unpack gems again.  Bug #27872 by Timothy Jones.
  * `gem unpack` now unpacks remote gems.
  * --user-install is no longer the default.  If you really liked it, see
    Gem::ConfigFile to learn how to set it by default.  (This change was made
    in 1.3.6)
* RubyGems now has platform support for IronRuby.  Patch #27951 by Will Green.

## Bug fixes:

* Require rubygems/custom_require if --disable-gem was set.  Bug #27700 by
  Roger Pack.
* RubyGems now protects against exceptions being raised by plugins.
* rubygems/builder now requires user_interaction.  Ruby Bug #1040 by Phillip
  Toland.
* Gem::Dependency support #version_requirements= with a warning.  Fix for old
  Rails versions.  Bug #27868 by Wei Jen Lu.
* Gem::PackageTask depends on the package dir like the other rake package
  tasks so dependencies can be hooked up correctly.

# 1.3.6 / 2010-02-17

## Features:

* `gem` commands
  * Added `gem push` and `gem owner` for interacting with modern/Gemcutter
    sources
  * `gem dep` now supports --prerelease.
  * `gem fetch` now supports --prerelease.
  * `gem server` now supports --bind.  Patch #27357 by Bruno Michel.
  * `gem rdoc` no longer overwrites built documentation.  Use --overwrite
    force rebuilding.  Patch #25982 by Akinori MUSHA.
* Capital letters are now allowed in prerelease versions.

## Bug fixes:

* Development deps are no longer added to rubygems-update gem so older
  versions can update successfully.
* Installer bugs:
  * Prerelease gems can now depend on non-prerelease gems.
  * Development dependencies are ignored unless explicitly needed.  Bug #27608
    by Roger Pack.
* `gem` commands
  * `gem which` now fails if no paths were found.  Adapted patch #27681 by
    Caio Chassot.
  * `gem server` no longer has invalid markup.  Bug #27045 by Eric Young.
  * `gem list` and friends show both prerelease and regular gems when
    --prerelease --all is given
* Gem::Format no longer crashes on empty files.  Bug #27292 by Ian Ragsdale.
* Gem::GemPathSearcher handles nil require_paths. Patch #27334 by Roger Pack.
* Gem::RemoteFetcher no longer copies the file if it is where we want it.
  Patch #27409 by Jakub Šťastný.

## Deprecations:

* lib/rubygems/timer.rb has been removed.
* Gem::Dependency#version_requirements is deprecated and will be removed on or
  after August 2010.
* Bulk index update is no longer supported.
* Gem::manage_gems was removed in 1.3.3.
* Time::today was removed in 1.3.3.

# 1.3.5 / 2009-07-21

## Bug fixes:

* Fix use of prerelease gems.
* Gem.bin_path no longer escapes path with spaces. Bug #25935 and #26458.

## Deprecations:

* Bulk index update is no longer supported (the code currently remains, but not
  the tests)
* Gem::manage_gems was removed in 1.3.3.
* Time::today was removed in 1.3.3.

# 1.3.4 / 2009-05-03

## Bug fixes:

* Fixed various warnings
* Gem::ruby_version works correctly for 1.8 branch and trunk
* Prerelease gems now show up in `gem list` and can be used
* Fixed option name for `gem setup --format-executable`
* RubyGems now matches Ruby > 1.9.1 gem paths
* Gem::RemoteFetcher#download now works for explicit Windows paths across
  drives.  Bug #25882 by Lars Christensen
* Fix typo in Gem::Requirement#parse.  Bug #26000 by Mike Gunderloy.

## Deprecations:

* Bulk index update is no longer supported (the code currently remains, but not
  the tests)
* Gem::manage_gems was removed in 1.3.3.
* Time::today was removed in 1.3.3.

# 1.3.3 / 2009-05-04

## Features:

* `gem server` allows port names (from /etc/services) with --port.
* `gem server` now has search that jumps to RDoc.  Patch #22959 by Vladimir
  Dobriakov.
* `gem spec` can retrieve single fields from a spec (like `gem spec rake
  authors`).
* Gem::Specification#has_rdoc= is deprecated and ignored (defaults to true)
* RDoc is now generated regardless of Gem::Specification#has_rdoc?

## Bug fixes:

* `gem clean` now cleans up --user-install gems.  Bug #25516 by Brett
  Eisenberg.
* Gem.bin_path now escapes paths with spaces.
* Rake extension builder uses explicit correctly loads rubygems when invoking
  rake.
* Prerelease versions now match "~>" correctly.  Patch #25759 by Yossef
  Mendelssohn.
* Check bindir for executables, not root when validating.  Bug reported by
  David Chelimsky.
* Remove Time.today, no way to override it before RubyGems loads.  Bug #25564
  by Emanuele Vicentini
* Raise Gem::Exception for #installation_path when not installed.  Bug #25741
  by Daniel Berger.
* Don't raise in Gem::Specification#validate when homepage is nil.  Bug #25677
  by Mike Burrows.
* Uninstall executables from the correct directory.  Bug #25555 by Brett
  Eisenberg.
* Raise Gem::LoadError if Kernel#gem fails due to previously-loaded gem.  Bug
  reported by Alf Mikula.

## Deprecations:

* Gem::manage_gems has been removed.
* Time::today has been removed early.  There was no way to make it warn and be
  easy to override with user code.

# 1.3.2 / 2009-04-15

## Features:

* RubyGems now loads plugins from rubygems_plugin.rb in installed gems.
  This can be used to add commands (See Gem::CommandManager) or add
  install/uninstall hooks (See Gem::Installer and Gem::Uninstaller).
* Gem::Version now understands prerelease versions using letters. (eg.
  '1.2.1.b')  Thanks to Josh Susser, Alex Vollmer and Phil Hagelberg.
* RubyGems now includes a Rake task for creating gems which replaces rake's
  Rake::GemPackageTask.  See Gem::PackageTask.
* Gem::find_files now returns paths in $LOAD_PATH.
* Added Gem::promote_load_path for use with Gem::find_files
* Added Gem::bin_path to make finding executables easier.  Patch #24114 by
  James Tucker.
* Various improvements to build arguments for installing gems.
* `gem contents` added --all and --no-prefix.
* Gem::Specification
  * #validate strips directories and errors on not-files.
  * #description no longer removes newlines.
  * #name must be a String.
  * FIXME and TODO are no longer allowed in various fields.
  * Added support for a license attribute.  Feature #11041 (partial).
  * Removed Gem::Specification::list, too much process growth.  Bug #23668 by
    Steve Purcell.
* `gem generate_index`
  * Can now generate an RSS feed.
  * Modern indicies can now be updated incrementally.
  * Legacy indicies can be updated separately from modern.

## Bug fixes:

* Better gem activation error message. Patch #23082.
* Kernel methods are now private.  Patch #20801 by James M. Lawrence.
* Fixed various usability issues with `gem check`.
* `gem update` now rescues InstallError and continues.  Bug #19268 by Gabriel
  Wilkins.
* Allow 'https', 'file' as a valid schemes for --source.  Patch #22485.
* `gem install`
  * Now removes existing path before installing.  Bug #22837.
  * Uses Gem::bin_path in executable stubs to work around Kernel#load bug in
    1.9.
  * Correctly handle build args (after --) via the API.  Bug #23210.
* --user-install
  * `gem install --no-user-install` now works.  Patch #23573 by Alf Mikula.
  * `gem uninstall` can now uninstall from ~/.gem.  Bug #23760 by Roger Pack.
* setup.rb
  * Clarify RubyGems RDoc installation location.  Bug #22656 by Gian Marco
    Gherardi.
  * Allow setup to run from read-only location.  Patch #21862 by Luis Herrera.
  * Fixed overwriting ruby executable when BASERUBY was not set.  Bug #24958
    by Michael Soulier.
  * Ensure we're in a RubyGems dir when installing.
  * Deal with extraneous quotation mark when autogenerating .bat file on MS
    Windows.  Bug #22712.

## Deprecations:

* Gem::manage_gems has been removed.
* Time::today will be removed in RubyGems 1.4.

Special thanks to Chad Wooley for backwards compatibility testing and Luis
Lavena and Daniel Berger for continuing windows support.

# 1.3.1 / 2008-10-28

## Bug fixes:

* Disregard ownership of ~ under Windows while creating ~/.gem.  Fixes
  issues related to no uid support under Windows.
* Fix requires for Gem::inflate, Gem::deflate, etc.
* Make Gem.dir respect :gemhome value from config.  (Note: this feature may be
  removed since it is hard to implement on 1.9.)
* Kernel methods are now private.  Patch #20801 by James M. Lawrence.
* Gem::location_of_caller now behaves on Windows.  Patch by Daniel Berger.
* Silence PATH warning.

## Deprecations:

* Gem::manage_gems will be removed on or after March 2009.

# 1.3.0 / 2008-09-25

## Features:

* RubyGems doesn't print LOCAL/REMOTE titles for `gem query` and friends if
  stdout is not a TTY, except with --both.
* Added Gem.find_files, allows a gem to discover features provided by other
  gems.
* Added pre/post (un)install hooks for packagers of RubyGems.  (Not for gems
  themselves).
* RubyGems now installs gems into ~/.gem if GEM_HOME is not writable.  Use
  --no-user-install command-line switch to disable this behavior.
* Fetching specs for update now uses If-Modified-Since requests.
* RubyGems now updates the ri cache when the rdoc gem is installed and
  documentation is generated.

## Deprecations:

* Gem::manage_gems now warns when called.  It will be removed on or after March
  2009.

## Bug fixes:

* RubyGems 1.3.0+ now updates when no previous rubygems-update is installed.
  Bug #20775 by Hemant Kumar.
* RubyGems now uses the regexp we already have for `gem list --installed`.  Bug
  #20876 by Nick Hoffman.
* Platform is now forced to Gem::Platform::RUBY when nil or blank in the
  indexer.  Fixes various uninstallable gems.
* Handle EINVAL on seek.  Based on patch in bug #20791 by Neil Wilson.
* Fix HTTPS support.  Patch #21072 by Alex Arnell.
* RubyGems now loads all cache files even if latest has been loaded.  Bug
  #20776 by Uwe Kubosch.
* RubyGems checks for support of development dependencies for #to_ruby.  Bug
  #20778 by Evan Weaver.
* Now specifications from the future can be loaded.
* Binary script uninstallation fixed.  Bug #21234 by Neil Wilson.
* Uninstallation with -i fixed.  Bug #20812 by John Clayton.
* Gem::Uninstaller#remove_all now calls Gem::Uninstaller#uninstall_gem so hooks
  get called.  Bug #21242 by Neil Wilson.
* Gem.ruby now properly escaped on windows.  Fixes problem with extension
  compilation.
* `gem lock --strict` works again.  Patch #21814 by Sven Engelhardt.
* Platform detection for Solaris was improved.  Patch #21911 by Bob Remeika.

## Enhancements:

* `gem help install` now describes _version_ argument to executable stubs
* `gem help environment` describes environment variables and ~/.gemrc and
  /etc/gemrc
* On-disk gemspecs are now read in UTF-8 and written with a UTF-8 magic comment
* Rakefile
  * If the SETUP_OPTIONS environment variable is set, pass its contents as
    arguments to setup.rb
* lib/rubygems/platform.rb
  * Remove deprecated constant warnings and really deprecate them.  (WIN32,
    etc).
* lib/rubygems/remote_fetcher.rb
  * Now uses ~/.gem/cache if the cache dir in GEM_HOME is not writable.
* lib/rubygems/source_index.rb
  * Deprecate options to 'search' other than Gem::Dependency instances and
    issue warning until November 2008.
* setup.rb
  * --destdir folder structure now built using Pathname, so it works for
    Windows platforms.
* test/*
  * Fixes to run tests when under test/rubygems/.  Patch by Yusuke ENDOH
    [ruby-core:17353].
* test/test_ext_configure_builder.rb
  * Locale-free patch by Yusuke Endoh [ruby-core:17444].

# 1.2.0 / 2008-06-21

## Features:

* RubyGems no longer performs bulk updates and instead only fetches the gemspec
  files it needs.  Alternate sources will need to upgrade to RubyGems 1.2 to
  allow RubyGems to take advantage of the new metadata updater.  If a pre 1.2
  remote source is in the sources list, RubyGems will revert to the bulk update
  code for compatibility.
* RubyGems now has runtime and development dependency types.  Use
  #add_development_dependency and #add_runtime_dependency.  All typeless
  dependencies are considered to be runtime dependencies.
* RubyGems will now require rubygems/defaults/operating_system.rb and
  rubygems/defaults/#{RBX_ENGINE}.rb if they exist.  This allows packagers and
  ruby implementers to add custom behavior to RubyGems via these files.  (If
  the RubyGems API is insufficient, please suggest improvements via the
  RubyGems list.)
* /etc/gemrc (and windows equivalent) for global settings
* setup.rb now handles --vendor and --destdir for packagers
* `gem stale` command that lists gems by last access time

## Bug fixes:

* File modes from gems are now honored, patch #19737
* Marshal Gem::Specification objects from the future can now be loaded.
* A trailing / is now added to remote sources when missing, bug #20134
* Gems with legacy platforms will now be correctly uninstalled, patch #19877
* `gem install --no-wrappers` followed by `gem install --wrappers` no longer
  overwrites executables
* `gem pristine` now forces reinstallation of gems, bug #20387
* RubyGems gracefully handles ^C while loading .gemspec files from disk, bug
  #20523
* Paths are expanded in more places, bug #19317, bug #19896
* Gem::DependencyInstaller resets installed gems every install, bug #19444
* Gem.default_path is now honored if GEM_PATH is not set, patch #19502

## Enhancements:

* setup.rb
  * stub files created by RubyGems 0.7.x and older are no longer removed.  When
    upgrading from these ancient versions, upgrade to 1.1.x first to clean up
    stubs.
  * RDoc is no longer required until necessary, patch #20414
* `gem server`
  * Now completely matches the output of `gem generate_index` and
    has correct content types
  * Refreshes from source directories for every hit.  The server will no longer
    need to be restarted after installing gems.
* `gem query --details` and friends now display author, homepage, rubyforge url
  and installed location
* `gem install` without -i no longer reinstalls dependencies if they are in
  GEM_PATH but not in GEM_HOME
* Gem::RemoteFetcher now performs persistent connections for HEAD requests,
  bug #7973

# 1.1.1 / 2008-04-11

## Bug fixes:

* Gem.prefix now returns non-nil only when RubyGems was installed outside
  sitelibdir or libdir.
* The `gem server` gem list now correctly links to gem details.
* `gem update --system` now passes --no-format-executable to setup.rb.
* Gem::SourceIndex#refresh! now works with multiple gem repositories.
* Downloaded gems now go into --install-dir's cache directory.
* Various fixes to downloading gem metadata.
* `gem install --force` now ignores network errors too.
* `gem pristine` now rebuilds extensions.
* `gem update --system` now works on virgin Apple ruby.
* Gem::RemoteFetcher handles Errno::ECONNABORTED.
* Printing of release notes fixed.

# 1.1.0 / 2008-03-29

## Features:

* RubyGems now uses persistent connections on index updates.  Index updates are
  much faster now.
* RubyGems only updates from a latest index by default, cutting candidate gems
  for updates to roughly 1/4 (at present).  Index updates are even faster
  still.
  * `gem list -r` may only show the latest version of a gem, add --all to see
    all gems.
* `gem spec` now extracts specifications from .gem files.
* `gem query --installed` to aid automation of checking for gems.

## Bug fixes:

* RubyGems works with both Config and RbConfig now.
* Executables are now cleaned upon uninstall.
* You can now uninstall from a particular directory.
* Updating from non-default sources fixed.
* Executable stubs now use ruby install name in shebang.
* `gem unpack` checks every directory in Gem.path now.
* `gem install` now exits with non-zero exit code when appropriate.
* `gem update` only updates gems that need updates.
* `gem update` doesn't force remote-only updates.
* `gem update` handles dependencies properly when updating.
* Gems are now loaded in Gem.path order.
* Gem stub scripts on windows now work outside Gem.bindir.
* `gem sources -r` now works without network access.

## Enhancements:

* RubyGems now requires Ruby > 1.8.3.
* Release notes are now printed upon installation.
* `gem env path` now prints a usable path.
* `gem install` reverts to local-only installation upon network error.
* Tar handling code refactoring and cleanup.
* Gem::DependencyInstaller's API has changed.

For a full list of changes to RubyGems, see the git log.

# 1.0.1 / 2007-12-20

## Bug fixes:

* Installation on Ruby 1.8.3 through 1.8.5 fixed
* `gem build` on 1.8.3 fixed

## Enhancements:

* Since RubyGems 0.9.5, RubyGems is no longer supported on Ruby 1.8.2 or older,
  this is official in RubyGems 1.0.1.

# 1.0.0 / 2007-12-20

## Features:

* RubyGems warns about various problems with gemspecs during gem building
* More-consistent versioning for the RubyGems software

## Enhancements:

* Fixed various bugs and problems with installing gems on Windows
* Fixed using `gem server` for installing gems
* Various operations are even more verbose with --verbose
* Built gems are now backwards compatible with 0.9.4
* Improved detection of RUBYOPT loading rubygems
* `ruby setup.rb` now has a --help option
* Gem::Specification#bindir is now respected on installation
* Executable stubs can now be installed to match ruby's name, so if ruby is
  installed as 'ruby18', foo_exec will be installed as 'foo_exec18'
* `gem unpack` can now unpack into a specific directory with --target
* OpenSSL is no longer required by default

## Breaking changes:

* Kernel#require_gem has been removed
* Executables without a shebang will not be wrapped in a future version, this
  may cause such executables to fail to operate on installation
* Gem::Platform constants other than RUBY and CURRENT have been removed
* Gem::RemoteInstaller was removed
* Gem::Specification#test_suite_file and #test_suite_file= are deprecated in
  favor of #test_file and #test_file=
* Gem::Specification#autorequire= has been deprecated
* Time::today will be removed in a future version

# 0.9.5 / 2007-11-19

## Features:

* Platform support
* Automatic installation of platform gems
* New bandwidth and memory friendlier index file format
* "Offline" mode (--no-update-sources)
* Bulk update threshold can be specified (-B, --bulk-threshold)
* New `gem fetch` command
* `gem` now has "really verbose" output when you specify -v
* Improved stubs and `gem.bat` on mswin, including better compatibility
  with the One-Click Installer.

## Enhancements:

* Time::today is deprecated and will be removed at a future date
* Gem::manage_gems is deprecated and will be removed at a future date
* `gem install --include-dependencies` (-y) is now deprecated since it is the
  default, use --ignore-dependencies to turn off automatic dependency
  installation
* Multi-version diamond dependencies only are installed once
* Processing a YAML bulk index update takes less memory
* `gem install -i` makes sure all dependencies are installed
* `gem update --system` reinstalls into the prefix it was originally installed
  in
* `gem update --system` respects --no-rdoc and --no-ri flags
* HTTP basic authentication support for proxies
* Gem::Specification#platforms should no longer be a String, use
  Gem::Platform::CURRENT when building binary gems instead
* `gem env` has more diagnostic information
* require 'rubygems' loads less code
* sources.gem is gone, RubyGems now uses built-in defaults
* `gem install --source` will no longer add --source by default, use `gem
  sources --add` to make it a permanent extra source
* `gem query` (list) no longer prints details by default
* Exact gem names are matched in various places
* mkrf extensions are now supported
* A gem can depend on a specific RubyGems version
* `gem_server` is now `gem server`
* `gemlock` is now `gem lock`
* `gem_mirror` is now `gem mirror`
* `gemwhich` is now `gem which`
* `gemri` is no longer included with RubyGems
* `index_gem_repository.rb` is now `gem generate_index`
* `gem` performs more validation of parameters
* Custom rdoc styles are now supported
* Gem indexer no longer removes quick index during index creation
* Kernel#require only rescues a LoadError for the file being required now
* `gem dependencies` can now display some information for remote gems
* Updating RubyGems now works with RUBYOPT=-rubygems

Special thanks to:

* Daniel Berger
* Luis Lavena
* Tom Copeland
* Wilson Bilkovich

# 0.9.4 / 2007-05-23

If you are experiencing problems with the source index (e.g. strange
"No Method" errors), or problems with zlib (e.g. "Buffer Error"
message), we recommend upgrading to RubyGems 0.9.4.

## Bug fixes:

* Several people have been experiencing problems with no method errors
  on the source index cache.  The source index cache is now a bit more
  self healing.  Furthermore, if the source index cache is
  irreparable, then it is automatically dropped and reloaded.
* The source cache files may now be dropped with the "gem sources
  --clear-all" command.  (This command may require root is the system
  source cache is in a root protected area).
* Several sub-commands were accidentally dropped from the "gem" command.
  These commands have been restored.

# 0.9.3 / 2007-05-10

## Bug fixes:

The ZLib library on Windows will occasionally complains about a buffer error
when unpacking gems.  The Gems software has a workaround for that problem, but
the workaround was only enabled for versions of ZLib 1.2.1 or earlier.  We
have received several reports of the error occurring with ZLib 1.2.3, so we
have permanently enabled the work around on all versions.

# 0.9.2 / 2007-02-05

## Bug fixes:

* The "unpack" command now works properly.
* User name and password are now passed properly to the authenticating
  proxy when downloading gems.

# 0.9.1 / 2007-01-16

See git log

# 0.9.0 / 2006-06-28

Finally, the much anticipated RubyGems version 0.9.0 is now available.
This release includes a number of new features and bug fixes.  The
number one change is that we can now download the gem index
incrementally.  This will greatly speed up the gem command when only a
few gems are out of date.

## Enhancements:

* The gem index is now downloaded incrementally, only updating entries
  that are out of date.  If more than 50 entries are out of date, we
  revert back to a bulk download.
* Several patches related to allowing RubyGems to work with
  authenticating proxies (from Danie Roux and Anatol Pomozov).  Just
  put the user and password in the proxy URL (e.g. -p
  http://user:password@proxy.address.com:8080) or use the
  HTTP_PROXY_USER and HTTP_PROXY_PASS environment variables.
* The gem unpack command can now accept a file path rather than just a
  install gem name.
* Both RI and RDOC documents are now generated by default.
* A gemri command is included to read gem RI docs (only needed for
  Ruby 1.8.4 or earlier).
* Version 0.0.0 is now a valid gem version.
* Better detection of missing SSL functionality.
* SSL is not required if the security policy does not require
  signature checking.
* Rake built extensions are now supported (Tilman Sauerbeck).
* Several autorequire bug fixes.
* --traceback is now an alias for --backtrace (I can never remember
  which one it is).
* SAFE=1 compatibility fixes.
* .rbw is now a supported suffix for RubyGem's custom require.
* Several Ruby 1.9 compatibility fixes (Eric Hodel).

## Bug fixes:

* Added dashes to gemspecs generated in Ruby 1.8.3.  This solves some
  cross-Ruby version compatibility issues.
* Fixed bug where the wrong executables could be uninstalled (Eric
  Hodel).
* Fixed bug where gem unpack occasionally unpacked the wrong gem.
* Fixed bug where a fatal error occurred when permissions on .gemrc
  were too restrictive (reported by Luca Pireddu).
* Fixed prefix handling for native expressions (patch by Aaron Patterson).
* Fixed several Upgrade => Update typos.

# 0.8.11 / 2005-07-13

* -y is a synonym for --include-dependencies.
* Better handling of errors in the top level rescue clause.
* Package list command (e.g. gem inspect GEM).
* .gemrc now allows cvsrc-like options to set defaults per subcommand.
* The autorequire gem spec field will now accept a list.
* Substituted Time for Date in specs, increasing performance
  dramatically.
* Fixed reported bug of gem directories ending in "-" (reported by
  Erik Hatcher).
* Fixed but in installer that caused dependency installation to not
  work.
* Added Paul Duncan's gem signing patch.
* Added Mark Hubbart's Framework patch (for better integration with OS
  X).
* Added David Glasser's install-from-mirror patch.
* Additional internal structural cleanup and test reorganization.

# 0.8.10 / 2005-03-27

* In multi-user environments, it is common to supply multiple versions of gems
  (for example Rails), allowing individual users to select the version of the
  gem they desire.  This allows a user to be insulated from updates to that
  gem.  RubyGems 0.8.10 fixes a problem where gems could occasionally become
  confused about the current versions of libraries selected by the user.
* The other annoying bug is that if there are any existing rubygems-update gems
  installed, then the "gem update --system" command will download a new
  update, but install the latest update prior to the download.

# 0.8.9

Never released

# 0.8.8 / 2005-03-14

* Moved the master definition of class Requirement back under version.
  Kept the body of Requirement under Gem.

# 0.8.7 / 2005-03-14

Even though it has only been a few weeks since that last release,
there are quite a number of new features in 0.8.7.  A complete list of
new features will be given below, but here is a summary of the hot
items.

* The bug that prevented some users from installing rails has been
  squashed.  A big thanks to Bill Guindon (aGorilla) for helping track
  that one down.

There are several new commands available on the gem command:

* gem cleanup GEMNAME -- Cleanup (uninstall) all the old versions of
  gem.  If the gem name is omitted, the entire repository is cleaned.
* gem dependency GEMNAME -- Show the dependencies for the named gems.
  This is really helpful when trying to figure out what gem needs what
  other gem.

There changes to the existing commands as well.

* gem uninstall is much smarter about removing gems from the
  repository.  Lists of gems are now uninstalled in proper dependency
  order (ie. if A depends on B, A is uninstalled first).  Also,
  warnings about broken dependencies occur only when removing the
  *last* gem that supports a dependency is removed.

Both gem install and gem uninstall support some new command line
options that can reduce the amount of yes/no queries given the user.
For install we have:

* --ignore-dependencies -- Only install requests gems, no
  dependendecies are automatically installed.
* --include-dependencies -- Automatically install dependencies,
  without confirmation.

For gem uninstall, the new options are:

* --all -- Uninstall all matching gems without confirmation.
* --ignore-dependencies -- Uninstall, even if dependencies are broken.
* --executables -- Remove executables without confirmation

Under general cleanup, gems will not, by default, run RDoc on packages
that do not have the RDoc flag set.

And finally there is a new library file 'gemconfigure' to aid in
writing version sensitive applications (without undue dependencies on
RubyGems); and 'gemwhich', a short script to locate libraries in the
file system.  You can read more about them here:

* gemconfigure: http://docs.rubygems.org/read/chapter/4#page73
* gemwhich: http://docs.rubygems.org/read/chapter/17

# 0.8.6 / 2005-02-27

* Fixed a small bug with shebang construction

# 0.8.5 / 2005-02-26

Do you know how you used to dread getting the following message while
installing gems?

  Updating Gem source index for: http://gems.rubyforge.org

It could take up to 30 seconds (on my machine, even worse on others) for
that crazy source index to update.

This latest release of RubyGems speeds that wait time up considerably.
The following table gives the following times for installing RedCloth
with a required source index update on three system we had available to
us.  No RDoc generation was included in the following times.

  RubyGems    Linux         Mac OSX      Windows
  0.8.4       33 secs       73 secs      58 secs
  0.8.5        8 secs       14 secs      21 secs

The new caching code is at least 3x faster than previous versions.  Woo
Hoo!

# 0.8.4 / 2005-01-01

* Rubygems 0.8.3's installer was broken unless you already had an older
  version of RubyGems installed.  That's fixed.
* Change in the way Gem::Specification internally deals with lazy attributes
  and defaults, bringing (with some loadpath_manager changes) a fairly
  significant increase in speed.
* Support for lower-cased Gem file names (for you, Paul Duncan :)
* Erik Veenstra's patch for making Gem versions sortable.

# 0.8.3 / 2004-12-07

No real earth shattering news here, but there were a number of really
annoying issues involving other libraries that RubyGems depends upon.
0.8.3 contains some workarounds for these issues.  In particular:

* Added workaround for the null byte in Dir string issue. (see
  http://blade.nagaokaut.ac.jp/cgi-bin/scat.rb/ruby/ruby-talk/121702).
  (Thanks to Mauricio Fernández for the quick response on this one).
* Added workaround for old version of Zlib on windows that caused
  Ruwiki to fail to install. (see
  http://blade.nagaokaut.ac.jp/cgi-bin/scat.rb/ruby/ruby-talk/121770)
* Added workaround for large YAML file issues.  (We dynamically cut
  down the size of the source index YAML file and seem to have worked
  around immediate issues.

There has been some minor usability enhancements and changes ...

* A user specific source index cache can be used when the site-wide
  cache is unwritable (i.e. because you are running as a non-admin).
  This *greatly* speeds up gem commands run in non-admin mode when the
  site-wide cache is out of date.
* The gem command now used an HTTP HEAD command to detect if the
  server's source index needs to be downloaed.
* gem check gemname --test will run unit tests on installed gems that
  have unit tests.
* Multiple gem names are allowed on the gem install command line.
  This means you can do:

    gem install rake rails needle postgres-pr pimki

  (Ok, you get the idea)
* Multiple authors my be specified in a Gem spec.
* Switched to using setup.rb (rather than a custom install script) for
  the installation of RubyGems itself.  If you have installed RubyGems
  before, double check the installation instructions and make sure you
  use setup.rb instead of install.rb.
* Ryan Davis has provided a patch so you can use an env variable
  (GEM_SKIP), to tell loadpath_manager not to load gems of those
  names.  This was useful for him while testing libs that he had in
  development.

# 0.8.1 / 2004-09-17

* Quick release to capture some bug fixes.

# 0.8.0 / 2004-09-15

* Remove need for library stubs.  Set the RUBYOPT environment variable to
  include "rrubygems", and a normal require will find gem files.  Continue to
  use 'require_gem gem_name, version' to specify gem versions.
* Deprecated "test_suite_file" gemspec attribute in favor of "test_files" array.
* Generates rdoc by default on installs.
* Adopted tar/gzip file format, thanks to Mauricio Fernandez.
* "gem rdoc" allows generation of rdoc after gem installation (will add a "gem
  test"
* Application stubs can now accept an optional parameter of _VERSION_ that will
  run an arbitrary version of the application requested.
* Various bug fixes
* Various platform-independency improvements
* "gem spec --all" displays spec info for all installed version of a given gem.
* Dynamic caching of sources
* Support for user-definable sources on the command line (thanks Assaph Mehr)
* More intelligent support for platform-dependent gems.  Use Platform::CURRENT
  when building a gem to set its platform to the one you're building on.
  Installation displays a choice of platform-dependent gems, allowing the user
  to pick.
* Added "gem unpack" for "unpacking" a gem to the current directory

# 0.7.0 / 2004-07-09

See git log

# 0.6.1 / 2004-06-08

See git log

# 0.6.0 / 2004-06-08

* Collapse output of --search and --list (and gem_server) operations so that
  each gem is listed only once, with each of its versions listed on the same
  line.
* bin/gem: new --upgrade-all option allows one to upgrade every installed gem
* new #required_ruby_version attribute added to gem specification for
  specifying a dependency on which version of ruby the gem needs.  Format it
  accepts is the same as the Gem::Version::Requirement format:

    spec.required_ruby_version = "> 1.8.0"
* --install-stub defaults to true, so library stubs are created

# 0.5.0 / 2004-06-06

* Jim added the ability to specify version constraints to avoid API
  incompatibilities.  This has been the subject of much debate for the past
  couple of months, with many ideas and code contributed by Eivind Eklund and
  Mauricio Fernandez.  The following set of assertions shows how it works:

    assert_inadequate("1.3", "~> 1.4")
    assert_adequate(  "1.4", "~> 1.4")
    assert_adequate(  "1.5", "~> 1.4")
    assert_inadequate("2.0", "~> 1.4") # This one is key--the new operator
				       # disallows major version number
				       # differences.
* Group gem search output when multiple versions exist for a given gem:

    activerecord (0.7.8, 0.7.7, 0.7.6, 0.7.5)
      Implements the ActiveRecord pattern for ORM.
* Add arbitrary RDoc-able files via gemspec (not just Ruby source files) for
  people who have, for example, README.rdoc in their distributions.  Add to
  gemspec via: spec.extra_rdoc_files = ["list", "of", "files"].  Ruby files are
  automatically included.
* Some small bug fixes

# 0.4.0 / 2004-05-30

* Minor bug fixes including Windows compatibility issues

# 0.3.0 / 2004-04-30

* Cleanup of command-line arguments and handling.  Most commands accept a
  --local or --remote modifier.
* Creation of Application Gems (packages that include executable programs).
  See http://rubygems.rubyforge.org/wiki/wiki.pl?DeveloperGuide for information
  on how to use it.
* Basic functionality for installing binary gems from source (:extensions
  property of gem specification holds an array of paths to extconf.rb files to
  be used for compilation)
* Install library "stub" allowing a normal 'require' to work (which then does
  the rubygems require and 'require_gem'
* --run-tests runs the test suite specified by the "test_suite_file" property
  of a gem specification
* HTTP Proxy support works.  Rewrite of HTTP code.
* Unit and functional tests added (see Rakefile).
* Prompt before remote-installing dependencies during gem installation.
* Config file for storing preferences for 'gem' command usage.
* Generally improved error messages (still more work to do)
* Rearranged gem directory structure for cleanliness.

# 0.2.0 / 2004-03-14

* Initial public release
