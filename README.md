<!-- this file is generated via docker-builder, do not edit it directly -->


# What is docker-devel?

docker-devel is a a platform to develop [Perl](https://www.perl.org) apps.

All images, unless explicitly defined, are based on [alpine:3.20](https://hub.docker.com/repository/docker/alpine) and provide installed together with these Perl modules:

* [Term::ReadLine::Perl](https://metacpan.org/pod/Term::ReadLine::Perl) v1.0303.

# Supported tags and respective Dockerfile links

* docker-devel: [2.1, latest (main/Dockerfile)](https://github.com/EmilianoBruni/docker-devel/blob/master/main/Dockerfile) (size: **303MB**)

* docker-devel: [2.1-dzil, dzil (dzil/Dockerfile)](https://github.com/EmilianoBruni/docker-devel/blob/master/dzil/Dockerfile) (size: **374MB**) based on [alpine:3.20](https://hub.docker.com/repository/docker/alpine) with these additional Perl modules
	* [Dist::Zilla](https://metacpan.org/pod/Dist::Zilla) v6.032,
	* [Dist::Zilla::Plugin::ChangelogFromGit::CPAN::Changes](https://metacpan.org/pod/Dist::Zilla::Plugin::ChangelogFromGit::CPAN::Changes) v0.230680,
	* [Dist::Zilla::Plugin::GithubMeta](https://metacpan.org/pod/Dist::Zilla::Plugin::GithubMeta) v0.58,
	* [Dist::Zilla::Plugin::MinimumPerlFast](https://metacpan.org/pod/Dist::Zilla::Plugin::MinimumPerlFast) v0.005,
	* [Dist::Zilla::Plugin::MinimumPerl](https://metacpan.org/pod/Dist::Zilla::Plugin::MinimumPerl) v1.006,
	* [Dist::Zilla::Plugin::PodWeaver](https://metacpan.org/pod/Dist::Zilla::Plugin::PodWeaver) v4.010,
	* [Dist::Zilla::Plugin::ReadmeAnyFromPod](https://metacpan.org/pod/Dist::Zilla::Plugin::ReadmeAnyFromPod) v0.163250,
	* [Dist::Zilla::Plugin::Regenerate::AfterReleasers](https://metacpan.org/pod/Dist::Zilla::Plugin::Regenerate::AfterReleasers) v0.001002,
	* [Dist::Zilla::PluginBundle::Starter::Git](https://metacpan.org/pod/Dist::Zilla::PluginBundle::Starter::Git) vv5.0.1,
	* [Dist::Zilla::Plugin::AutoPrereqs](https://metacpan.org/pod/Dist::Zilla::Plugin::AutoPrereqs) v6.032,
	* [Dist::Zilla::Plugin::PkgVersion](https://metacpan.org/pod/Dist::Zilla::Plugin::PkgVersion) v6.032,
	* [Dist::Zilla::Plugin::Prereqs](https://metacpan.org/pod/Dist::Zilla::Plugin::Prereqs) v6.032,
	* [Software::License::Perl_5](https://metacpan.org/pod/Software::License::Perl_5) v0.104006.

# How to use this image

Start the application as

    $ docker run --rm -ti ebruni/devel

# Authors

Emiliano Bruni (EB) <info@ebruni.it>

# Changes

| AUTHOR | DATE | VER. | COMMENTS |
|:---|:---:|:---:|:---|
| EB | 2024-11-04 | 2.1 | Removed Term::ReadLine::Gnu for problem in debug and ignore git save.directory warnings |
| EB | 2024-10-30 | 2.0 | Update alpine to 3.20. Support for autocomplete in debug |
| EB | 2021-09-29 | 1.3 | Add Autoprereqs, Prereqs, PkgVersion |
| EB | 2021-09-06 | 1.2 | Add MinimumPerl to Dist::Zilla |
| EB | 2021-08-29 | 1.1 | Add Data::Printer |
| EB | 2021-08-26 | 1.0 | Initial Version |

# Source

The source of this image on [GitHub](https://github.com/EmilianoBruni/docker-devel).
