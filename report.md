bari@ubuntu24:~$ export GITHUB_USERNAME=YaQQrQ
bari@ubuntu24:~$ export GITHUB_TOKEN=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
bari@ubuntu24:~$ cd ${GITHUB_USERNAME}/workspace
bari@ubuntu24:~/YaQQrQ/workspace$ pushd .
~/YaQQrQ/workspace ~/YaQQrQ/workspace
bari@ubuntu24:~/YaQQrQ/workspace$ source scripts/activate
bari@ubuntu24:~/YaQQrQ/workspace$ \curl -sSL https://get.rvm.io | bash -s -- --ignore-dotfiles
Turning on ignore dotfiles mode.
Downloading https://github.com/rvm/rvm/archive/master.tar.gz
Installing RVM to /home/bari/.rvm/
Installation of RVM in /home/bari/.rvm/ is almost complete:

  * To start using RVM you need to run `source /home/bari/.rvm/scripts/rvm`
    in all your open shell windows, in rare cases you need to reopen all shell windows.
Thanks for installing RVM 🙏
Please consider donating to our open collective to help us maintain RVM.

👉  Donate: https://opencollective.com/rvm/donate


bari@ubuntu24:~/YaQQrQ/workspace$ echo "source $HOME/.rvm/scripts/rvm" >> scripts/activate
bari@ubuntu24:~/YaQQrQ/workspace$ . scripts/activate
bari@ubuntu24:~/YaQQrQ/workspace$ rvm autolibs disable
bari@ubuntu24:~/YaQQrQ/workspace$ rvm install ruby
Searching for binary rubies, this might take some time.
No binary rubies available for: ubuntu/25.04/x86_64/ruby-3.4.1.
Continuing with compilation. Please read 'rvm help mount' to get more information on binary rubies.
Installing Ruby from source to: /home/bari/.rvm/rubies/ruby-3.4.1, this may take a while depending on your cpu(s)...
ruby-3.4.1 - #downloading ruby-3.4.1, this may take a while depending on your connection...
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100 22.0M  100 22.0M    0     0  7599k      0  0:00:02  0:00:02 --:--:-- 7597k
ruby-3.4.1 - #extracting ruby-3.4.1 to /home/bari/.rvm/src/ruby-3.4.1.....
ruby-3.4.1 - #autogen.sh.
Error running '/home/bari/.rvm/src/ruby-3.4.1/autogen.sh',
please read /home/bari/.rvm/log/1744981663_ruby-3.4.1/autogen.sh.log
There has been an error while running autogen.sh. Halting the installation.
bari@ubuntu24:~/YaQQrQ/workspace$ rvm install ruby-2.4.2
Searching for binary rubies, this might take some time.
No binary rubies available for: ubuntu/25.04/x86_64/ruby-2.4.2.
Continuing with compilation. Please read 'rvm help mount' to get more information on binary rubies.
Installing Ruby from source to: /home/bari/.rvm/rubies/ruby-2.4.2, this may take a while depending on your cpu(s)...
ruby-2.4.2 - #downloading ruby-2.4.2, this may take a while depending on your connection...
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100 12.0M  100 12.0M    0     0  7799k      0  0:00:01  0:00:01 --:--:-- 7802k
ruby-2.4.2 - #extracting ruby-2.4.2 to /home/bari/.rvm/src/ruby-2.4.2.....
Error running '__rvm_package_extract /home/bari/.rvm/archives/ruby-2.4.2.tar.bz2 /home/bari/.rvm/tmp/rvm_src_6252',
please read /home/bari/.rvm/log/1744981699_ruby-2.4.2/extract.log
There has been an error while trying to extract the source. Halting the installation.
There has been an error fetching the ruby interpreter. Halting the installation.
bari@ubuntu24:~/YaQQrQ/workspace$ rvm use 2.4.2 --default
Required ruby-2.4.2 is not installed.
To install do: 'rvm install "ruby-2.4.2"'
bari@ubuntu24:~/YaQQrQ/workspace$ rvm install ruby-2.4.2
Searching for binary rubies, this might take some time.
No binary rubies available for: ubuntu/25.04/x86_64/ruby-2.4.2.
Continuing with compilation. Please read 'rvm help mount' to get more information on binary rubies.
Installing Ruby from source to: /home/bari/.rvm/rubies/ruby-2.4.2, this may take a while depending on your cpu(s)...
ruby-2.4.2 - #downloading ruby-2.4.2, this may take a while depending on your connection...
ruby-2.4.2 - #extracting ruby-2.4.2 to /home/bari/.rvm/src/ruby-2.4.2.....
Error running '__rvm_package_extract /home/bari/.rvm/archives/ruby-2.4.2.tar.bz2 /home/bari/.rvm/tmp/rvm_src_6252',
please read /home/bari/.rvm/log/1744981854_ruby-2.4.2/extract.log
There has been an error while trying to extract the source. Halting the installation.
There has been an error fetching the ruby interpreter. Halting the installation.
bari@ubuntu24:~/YaQQrQ/workspace$ gem install travis
Fetching net-http-pipeline-1.0.1.gem
Fetching connection_pool-2.5.1.gem
Fetching net-http-persistent-4.0.5.gem
Fetching multi_json-1.15.0.gem
Fetching ffi-1.17.2-x86_64-linux-gnu.gem
Fetching ethon-0.16.0.gem
Fetching typhoeus-1.4.1.gem
Fetching faraday-net_http-3.0.2.gem
Fetching faraday-2.7.12.gem
Fetching faraday-typhoeus-1.1.0.gem
Fetching faraday-retry-2.3.1.gem
Fetching public_suffix-6.0.1.gem
Fetching addressable-2.8.7.gem
Fetching concurrent-ruby-1.3.5.gem
Fetching tzinfo-2.0.6.gem
Fetching i18n-1.14.7.gem
Fetching activesupport-7.0.8.7.gem
Fetching travis-gh-0.21.0.gem
Fetching rack-3.1.13.gem
Fetching rack-test-2.1.0.gem
Fetching websocket-1.2.11.gem
Fetching pusher-client-0.6.2.gem
Fetching launchy-2.5.2.gem
Fetching json_pure-2.6.3.gem
Fetching travis-1.14.0.gem
Fetching highline-2.1.0.gem
Fetching faraday-rack-2.1.2.gem
Defaulting to user installation because default installation directory (/var/lib/gems/3.3.0) is not writable.
Successfully installed net-http-pipeline-1.0.1
Defaulting to user installation because default installation directory (/var/lib/gems/3.3.0) is not writable.
Successfully installed connection_pool-2.5.1
Defaulting to user installation because default installation directory (/var/lib/gems/3.3.0) is not writable.
Successfully installed net-http-persistent-4.0.5
Defaulting to user installation because default installation directory (/var/lib/gems/3.3.0) is not writable.
Successfully installed multi_json-1.15.0
Defaulting to user installation because default installation directory (/var/lib/gems/3.3.0) is not writable.
Successfully installed ffi-1.17.2-x86_64-linux-gnu
Defaulting to user installation because default installation directory (/var/lib/gems/3.3.0) is not writable.
Successfully installed ethon-0.16.0
Defaulting to user installation because default installation directory (/var/lib/gems/3.3.0) is not writable.
Successfully installed typhoeus-1.4.1
Defaulting to user installation because default installation directory (/var/lib/gems/3.3.0) is not writable.
Successfully installed faraday-net_http-3.0.2
Defaulting to user installation because default installation directory (/var/lib/gems/3.3.0) is not writable.
Successfully installed faraday-2.7.12
Defaulting to user installation because default installation directory (/var/lib/gems/3.3.0) is not writable.
Successfully installed faraday-typhoeus-1.1.0
Defaulting to user installation because default installation directory (/var/lib/gems/3.3.0) is not writable.
Successfully installed faraday-retry-2.3.1
Defaulting to user installation because default installation directory (/var/lib/gems/3.3.0) is not writable.
Successfully installed public_suffix-6.0.1
Defaulting to user installation because default installation directory (/var/lib/gems/3.3.0) is not writable.
Successfully installed addressable-2.8.7
Defaulting to user installation because default installation directory (/var/lib/gems/3.3.0) is not writable.
Successfully installed concurrent-ruby-1.3.5
Defaulting to user installation because default installation directory (/var/lib/gems/3.3.0) is not writable.
Successfully installed tzinfo-2.0.6
Defaulting to user installation because default installation directory (/var/lib/gems/3.3.0) is not writable.
Successfully installed i18n-1.14.7
Defaulting to user installation because default installation directory (/var/lib/gems/3.3.0) is not writable.
Successfully installed activesupport-7.0.8.7
Defaulting to user installation because default installation directory (/var/lib/gems/3.3.0) is not writable.
Successfully installed travis-gh-0.21.0
Defaulting to user installation because default installation directory (/var/lib/gems/3.3.0) is not writable.
Successfully installed rack-3.1.13
Defaulting to user installation because default installation directory (/var/lib/gems/3.3.0) is not writable.
Successfully installed rack-test-2.1.0
Defaulting to user installation because default installation directory (/var/lib/gems/3.3.0) is not writable.
Successfully installed websocket-1.2.11
Defaulting to user installation because default installation directory (/var/lib/gems/3.3.0) is not writable.
Successfully installed pusher-client-0.6.2
Defaulting to user installation because default installation directory (/var/lib/gems/3.3.0) is not writable.
WARNING:  You don't have /home/bari/.local/share/gem/ruby/3.3.0/bin in your PATH,
	  gem executables (launchy) will not run.
Successfully installed launchy-2.5.2
Defaulting to user installation because default installation directory (/var/lib/gems/3.3.0) is not writable.
Successfully installed json_pure-2.6.3
Defaulting to user installation because default installation directory (/var/lib/gems/3.3.0) is not writable.
Successfully installed highline-2.1.0
Defaulting to user installation because default installation directory (/var/lib/gems/3.3.0) is not writable.
Successfully installed faraday-rack-2.1.2
Defaulting to user installation because default installation directory (/var/lib/gems/3.3.0) is not writable.
WARNING:  You don't have /home/bari/.local/share/gem/ruby/3.3.0/bin in your PATH,
	  gem executables (travis) will not run.
Successfully installed travis-1.14.0
Parsing documentation for net-http-pipeline-1.0.1
Installing ri documentation for net-http-pipeline-1.0.1
Parsing documentation for connection_pool-2.5.1
Installing ri documentation for connection_pool-2.5.1
Parsing documentation for net-http-persistent-4.0.5
Installing ri documentation for net-http-persistent-4.0.5
Parsing documentation for multi_json-1.15.0
Installing ri documentation for multi_json-1.15.0
Parsing documentation for ffi-1.17.2-x86_64-linux-gnu
Installing ri documentation for ffi-1.17.2-x86_64-linux-gnu
Parsing documentation for ethon-0.16.0
Installing ri documentation for ethon-0.16.0
Parsing documentation for typhoeus-1.4.1
Installing ri documentation for typhoeus-1.4.1
Parsing documentation for faraday-net_http-3.0.2
Installing ri documentation for faraday-net_http-3.0.2
Parsing documentation for faraday-2.7.12
Installing ri documentation for faraday-2.7.12
Parsing documentation for faraday-typhoeus-1.1.0
Installing ri documentation for faraday-typhoeus-1.1.0
Parsing documentation for faraday-retry-2.3.1
Installing ri documentation for faraday-retry-2.3.1
Parsing documentation for public_suffix-6.0.1
Installing ri documentation for public_suffix-6.0.1
Parsing documentation for addressable-2.8.7
Installing ri documentation for addressable-2.8.7
Parsing documentation for concurrent-ruby-1.3.5
Installing ri documentation for concurrent-ruby-1.3.5
Parsing documentation for tzinfo-2.0.6
Installing ri documentation for tzinfo-2.0.6
Parsing documentation for i18n-1.14.7
Installing ri documentation for i18n-1.14.7
Parsing documentation for activesupport-7.0.8.7
Installing ri documentation for activesupport-7.0.8.7
Parsing documentation for travis-gh-0.21.0
Installing ri documentation for travis-gh-0.21.0
Parsing documentation for rack-3.1.13
Installing ri documentation for rack-3.1.13
Parsing documentation for rack-test-2.1.0
Installing ri documentation for rack-test-2.1.0
Parsing documentation for websocket-1.2.11
Installing ri documentation for websocket-1.2.11
Parsing documentation for pusher-client-0.6.2
Installing ri documentation for pusher-client-0.6.2
Parsing documentation for launchy-2.5.2
Installing ri documentation for launchy-2.5.2
Parsing documentation for json_pure-2.6.3
Installing ri documentation for json_pure-2.6.3
Parsing documentation for highline-2.1.0
Installing ri documentation for highline-2.1.0
Parsing documentation for faraday-rack-2.1.2
Installing ri documentation for faraday-rack-2.1.2
Parsing documentation for travis-1.14.0
Installing ri documentation for travis-1.14.0
Done installing documentation for net-http-pipeline, connection_pool, net-http-persistent, multi_json, ffi, ethon, typhoeus, faraday-net_http, faraday, faraday-typhoeus, faraday-retry, public_suffix, addressable, concurrent-ruby, tzinfo, i18n, activesupport, travis-gh, rack, rack-test, websocket, pusher-client, launchy, json_pure, highline, faraday-rack, travis after 7 seconds
27 gems installed
bari@ubuntu24:~/YaQQrQ/workspace$ git clone https://github.com/${GITHUB_USERNAME}/lab03 projects/lab04
Cloning into 'projects/lab04'...
remote: Enumerating objects: 16, done.
remote: Counting objects: 100% (16/16), done.
remote: Compressing objects: 100% (12/12), done.
remote: Total 16 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
Receiving objects: 100% (16/16), 6.13 KiB | 3.07 MiB/s, done.
Resolving deltas: 100% (1/1), done.
bari@ubuntu24:~/YaQQrQ/workspace$ cd projects/lab04
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab04$ git remote remove origin
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab04$ git remote add origin https://github.com/${GITHUB_USERNAME}/lab04
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab04$ cat > .travis.yml <<EOF
> language: cpp
> EOF
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab04$ cat >> .travis.yml <<EOF
> script:
- cmake -H. -B_build -DCMAKE_INSTALL_PREFIX=_install
- cmake --build _build
- cmake --build _build --target install
> EOF
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab04$ cat >> .travis.yml <<EOF
> addons:
  apt:
    sources:
      - george-edison55-precise-backports
    packages:
      - cmake
      - cmake-data
> EOF
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab04$ travis login --github-token ${GITHUB_TOKEN}
Command 'travis' not found, but can be installed with:
sudo snap install travis  # version 1.8.9, or
sudo apt  install travis  # version 220729-1
See 'snap info travis' for additional versions.
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab04$ ^C
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab04$ sudo apt  install travis
[sudo] password for bari: 
Installing:                     
  travis

Suggested packages:
  cp2k  gnuplot  grace  graphviz  pymol

Summary:
  Upgrading: 0, Installing: 1, Removing: 0, Not Upgrading: 0
  Download size: 1 526 kB
  Space needed: 3 864 kB / 19,7 GB available

Get:1 http://ru.archive.ubuntu.com/ubuntu plucky/universe amd64 travis amd64 220729-1 [1 526 kB]
Fetched 1 526 kB in 1s (1 025 kB/s)     
Selecting previously unselected package travis.
(Reading database ... 194188 files and directories currently installed.)
Preparing to unpack .../travis_220729-1_amd64.deb ...
Unpacking travis (220729-1) ...
Setting up travis (220729-1) ...
Processing triggers for man-db (2.13.0-1) ...
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab04$ travis login --github-token ${GITHUB_TOKEN}

  ________                                 __
 /        |                               /  |
 ########/ ______    ______    __     __  ##/    _______
    ## |  /      \  /      \  /  \   /  | /  |  /       |
    ## | /######  | ######  | ##  \ /##/  ## | /#######/
    ## | ## |  ##/  /    ## |  ##  /##/   ## | ##      \
    ## | ## |      /####### |   ## ##/    ## |  ######  |
    ## | ## |      ##    ## |    ###/     ## | /     ##/
    ##/  ##/        #######/      #/      ##/  #######/

    TRajectory Analyzer and VISualizer  -  Open-source free software under GNU GPL v3

    Copyright (c) Martin Brehm      (2009-2022), University of Halle (Saale)
                  Martin Thomas     (2012-2022)
                  Sascha Gehrke     (2016-2022), University of Bonn
                  Barbara Kirchner  (2009-2022), University of Bonn

    http://www.travis-analyzer.de

    Please cite: J. Chem. Phys. 2020, 152 (16), 164105.         (DOI 10.1063/5.0005078 )
                 J. Chem. Inf. Model. 2011, 51 (8), 2007-2023.  (DOI 10.1021/ci200217w )

    There is absolutely no warranty on any results obtained from TRAVIS.

 #  Running on ubuntu24 at Fri Apr 18 13:18:48 2025 (PID 10464)
 #  Running in /home/bari/YaQQrQ/workspace/projects/lab04
 #  Version: Jul 29 2022, built at Jan 14 2023, 12:32:45, compiler "12.2.0", GCC 12.2.0
 #  Target platform: Linux, __cplusplus=201703L, Compile flags: NEW_CHARGEVAR DEBUG_ARRAYS 
 #  Compiled with OpenMP, but USE_OMP not switched on in "config.h"!
 #  Machine: x86_64, char=1b, int=4b, long=8b, addr=8b, 0xA0B0C0D0=D0,C0,B0,A0.
 #  Home: /home/bari,  Executable: /usr/bin/travis
 #  Input from terminal,  Output to terminal

    >>> Please use a color scheme with dark background or specify "-nocolor"! <<<

    No configuration file found.
    Writing default configuration to /home/bari/.travis.conf ...

Unknown parameter: "login".

    List of supported command line options:

      -p <file>       Load position data from specified trajectory file.
                      Format may be *.xyz, *.pdb, *.lmp (LAMMPS), HISTORY (DLPOLY), POSCAR/XDATCAR (VASP),
                                    *.gro, *.dcd, or *.prmtop/*.mdcrd (Amber).
                      The bqb format (*.bqb, *.btr, *.emp, *.blist) as well as *.voronoi are also supported.
      -vel <file>     Read atom velocities from a file in addition to the position trajectory.
                      Currently, only .xyz format is supported for velocity data.
      -i <file>       Read input from specified text file.
      -c <file>       Read and execute control file (experimental).
      cubetool        Execute the CubeTool for modifying Gaussian Cube files.
      -sankey <file>  Create Sankey diagrams (file name is optional).
      -ramanfrompola  Compute Raman spectra from existing polarizability time series.
      (de-)compress   Start built-in bqbtool (compress trajectories to BQB format).
      check           Check BQB file integrity.

      -config <file>  Load the specified configuration file.
      -stream         Treat input trajectory as a stream (e.g. named pipe): No fseek, etc.
      -showconf       Show a tree structure of the configuration file.
      -writeconf      Write the default configuration file, including all defines values.

      -verbose        Show detailed information about what's going on.
      -nocolor        Execute TRAVIS in monochrome mode (suitable for white background).
      -dimcolor       Use dim instead of bright colors.

      -credits        Display a list of persons who contributed to TRAVIS.
      -help, -?       Shows this help.

    If only one argument is specified, it is assumed to be the name of a trajectory file.
    If no argument is specified at all, TRAVIS asks for the trajectory file to open.

    Note: To show a list of all persons who contributed to TRAVIS,
          please add "-credits" to your command line arguments, or set the
          variable "SHOWCREDITS" to "TRUE" in your travis.conf file.

    Source code from other projects used in TRAVIS:
      - lmfit     from Joachim Wuttke
      - kiss_fft  from Mark Borgerding
      - voro++    from Chris Rycroft

    http://www.travis-analyzer.de

    Please cite all of the following articles for the analyses you have used:

  * For TRAVIS in general:

    "TRAVIS - A Free Analyzer for Trajectories from Molecular Simulation",
    M. Brehm, M. Thomas, S. Gehrke, B. Kirchner; J. Chem. Phys. 2020, 152 (16), 164105.   (DOI 10.1063/5.0005078 )

    "TRAVIS - A Free Analyzer and Visualizer for Monte Carlo and Molecular Dynamics Trajectories",
    M. Brehm, B. Kirchner; J. Chem. Inf. Model. 2011, 51 (8), pp 2007-2023.   (DOI 10.1021/ci200217w )

*** The End ***

bari@ubuntu24:~/YaQQrQ/workspace/projects/lab04$ travis lint
[Renaming existing File travis.log to #1#travis.log ...OK.]

  ________                                 __
 /        |                               /  |
 ########/ ______    ______    __     __  ##/    _______
    ## |  /      \  /      \  /  \   /  | /  |  /       |
    ## | /######  | ######  | ##  \ /##/  ## | /#######/
    ## | ## |  ##/  /    ## |  ##  /##/   ## | ##      \
    ## | ## |      /####### |   ## ##/    ## |  ######  |
    ## | ## |      ##    ## |    ###/     ## | /     ##/
    ##/  ##/        #######/      #/      ##/  #######/

    TRajectory Analyzer and VISualizer  -  Open-source free software under GNU GPL v3

    Copyright (c) Martin Brehm      (2009-2022), University of Halle (Saale)
                  Martin Thomas     (2012-2022)
                  Sascha Gehrke     (2016-2022), University of Bonn
                  Barbara Kirchner  (2009-2022), University of Bonn

    http://www.travis-analyzer.de

    Please cite: J. Chem. Phys. 2020, 152 (16), 164105.         (DOI 10.1063/5.0005078 )
                 J. Chem. Inf. Model. 2011, 51 (8), 2007-2023.  (DOI 10.1021/ci200217w )

    There is absolutely no warranty on any results obtained from TRAVIS.

 #  Running on ubuntu24 at Fri Apr 18 13:20:37 2025 (PID 10495)
 #  Running in /home/bari/YaQQrQ/workspace/projects/lab04
 #  Version: Jul 29 2022, built at Jan 14 2023, 12:32:45, compiler "12.2.0", GCC 12.2.0
 #  Target platform: Linux, __cplusplus=201703L, Compile flags: NEW_CHARGEVAR DEBUG_ARRAYS 
 #  Compiled with OpenMP, but USE_OMP not switched on in "config.h"!
 #  Machine: x86_64, char=1b, int=4b, long=8b, addr=8b, 0xA0B0C0D0=D0,C0,B0,A0.
 #  Home: /home/bari,  Executable: /usr/bin/travis
 #  Input from terminal,  Output to terminal

    >>> Please use a color scheme with dark background or specify "-nocolor"! <<<

    Loading configuration from /home/bari/.travis.conf ...

[Renaming existing File input.txt to #1#input.txt ...OK.]
Unknown parameter: "lint".

    List of supported command line options:

      -p <file>       Load position data from specified trajectory file.
                      Format may be *.xyz, *.pdb, *.lmp (LAMMPS), HISTORY (DLPOLY), POSCAR/XDATCAR (VASP),
                                    *.gro, *.dcd, or *.prmtop/*.mdcrd (Amber).
                      The bqb format (*.bqb, *.btr, *.emp, *.blist) as well as *.voronoi are also supported.
      -vel <file>     Read atom velocities from a file in addition to the position trajectory.
                      Currently, only .xyz format is supported for velocity data.
      -i <file>       Read input from specified text file.
      -c <file>       Read and execute control file (experimental).
      cubetool        Execute the CubeTool for modifying Gaussian Cube files.
      -sankey <file>  Create Sankey diagrams (file name is optional).
      -ramanfrompola  Compute Raman spectra from existing polarizability time series.
      (de-)compress   Start built-in bqbtool (compress trajectories to BQB format).
      check           Check BQB file integrity.

      -config <file>  Load the specified configuration file.
      -stream         Treat input trajectory as a stream (e.g. named pipe): No fseek, etc.
      -showconf       Show a tree structure of the configuration file.
      -writeconf      Write the default configuration file, including all defines values.

      -verbose        Show detailed information about what's going on.
      -nocolor        Execute TRAVIS in monochrome mode (suitable for white background).
      -dimcolor       Use dim instead of bright colors.

      -credits        Display a list of persons who contributed to TRAVIS.
      -help, -?       Shows this help.

    If only one argument is specified, it is assumed to be the name of a trajectory file.
    If no argument is specified at all, TRAVIS asks for the trajectory file to open.

    Note: To show a list of all persons who contributed to TRAVIS,
          please add "-credits" to your command line arguments, or set the
          variable "SHOWCREDITS" to "TRUE" in your travis.conf file.

    Source code from other projects used in TRAVIS:
      - lmfit     from Joachim Wuttke
      - kiss_fft  from Mark Borgerding
      - voro++    from Chris Rycroft

    http://www.travis-analyzer.de

    Please cite all of the following articles for the analyses you have used:

  * For TRAVIS in general:

    "TRAVIS - A Free Analyzer for Trajectories from Molecular Simulation",
    M. Brehm, M. Thomas, S. Gehrke, B. Kirchner; J. Chem. Phys. 2020, 152 (16), 164105.   (DOI 10.1063/5.0005078 )

    "TRAVIS - A Free Analyzer and Visualizer for Monte Carlo and Molecular Dynamics Trajectories",
    M. Brehm, B. Kirchner; J. Chem. Inf. Model. 2011, 51 (8), pp 2007-2023.   (DOI 10.1021/ci200217w )

*** The End ***

bari@ubuntu24:~/YaQQrQ/workspace/projects/lab04$ ex -sc '1i|<фрагмент_вставки_значка>' -cx README.md
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab04$ git add .travis.yml
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab04$ git add README.md
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab04$ git commit -m"added CI"
[master 29e4abf] added CI
 2 files changed, 13 insertions(+)
 create mode 100644 .travis.yml
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab04$ git push origin master\
> 
Username for 'https://github.com': s
Password for 'https://s@github.com': 
remote: Support for password authentication was removed on August 13, 2021.
remote: Please see https://docs.github.com/get-started/getting-started-with-git/about-remote-repositories#cloning-with-https-urls for information on currently recommended modes of authentication.
fatal: Authentication failed for 'https://github.com/YaQQrQ/lab04/'
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab04$ ^C
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab04$ git push origin master
Username for 'https://github.com': YaQQrQ
Password for 'https://YaQQrQ@github.com': 
Enumerating objects: 20, done.
Counting objects: 100% (20/20), done.
Delta compression using up to 8 threads
Compressing objects: 100% (15/15), done.
Writing objects: 100% (20/20), 6.61 KiB | 6.61 MiB/s, done.
Total 20 (delta 3), reused 14 (delta 1), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (3/3), done.
remote: 
remote: Create a pull request for 'master' on GitHub by visiting:
remote:      https://github.com/YaQQrQ/lab04/pull/new/master
remote: 
To https://github.com/YaQQrQ/lab04
 * [new branch]      master -> master
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab04$ ^C
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab04$ git push origin main
error: src refspec main does not match any
error: failed to push some refs to 'https://github.com/YaQQrQ/lab04'
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab04$ 

