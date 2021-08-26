
<!-- this file is generated via docker-builder, do not edit it directly -->

# What is docker-devel?

docker-devel is a platform to develop [Perl](https://www.perl.org) apps.

The images are based on alpine:3.14 and provide installed together with this perl modules:
.

# Supported tags and respective Dockerfile links

* docker-devel: [1.0, latest (main/Dockerfile)](https://github.com/EmilianoBruni/docker-devel/blob/master/main/Dockerfile) (size: **197MB**)
* docker-devel: [1.0-dzil, dzil (dzil/Dockerfile)](https://github.com/EmilianoBruni/docker-devel/blob/master/dzil/Dockerfile) (size: **321MB**)
with library
	* [Dist::Zilla](https://metacpan.org/pod/Dist::Zilla),
	* [Dist::Zilla::Plugin::ChangelogFromGit::CPAN::Changes](https://metacpan.org/pod/Dist::Zilla::Plugin::ChangelogFromGit::CPAN::Changes),
	* [Dist::Zilla::Plugin::GithubMeta](https://metacpan.org/pod/Dist::Zilla::Plugin::GithubMeta),
	* [Dist::Zilla::Plugin::MinimumPerlFast](https://metacpan.org/pod/Dist::Zilla::Plugin::MinimumPerlFast),
	* [Dist::Zilla::Plugin::PodWeaver](https://metacpan.org/pod/Dist::Zilla::Plugin::PodWeaver),
	* [Dist::Zilla::Plugin::ReadmeAnyFromPod](https://metacpan.org/pod/Dist::Zilla::Plugin::ReadmeAnyFromPod),
	* [Dist::Zilla::Plugin::Regenerate::AfterReleasers](https://metacpan.org/pod/Dist::Zilla::Plugin::Regenerate::AfterReleasers),
	* [Dist::Zilla::PluginBundle::Starter::Git](https://metacpan.org/pod/Dist::Zilla::PluginBundle::Starter::Git).

# How to use this image

Start the application as

    $ docker run --rm -ti ebruni/devel

# Source

The source of this image on [GitHub](https://github.com/EmilianoBruni/docker-devel).
