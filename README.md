# NAME

Plack::Middleware::Woothee - Set woothee information based on User-Agent

# VERSION

This document describes Plack::Middleware::Woothee version 0.02.

# SYNOPSIS

    use Plack::Middleware::Woothee;
    use Plack::Builder;

    my $app = sub {
        my $env = shift;
        # automatically assigned by Plack::Middleware::Woothee
        my $woothee = $env->{'psgix.woothee'};
        ...
    };
    builder {
        enable 'Woothee';
        $app;
    };

# DESCRIPTION

This middleware get woothee information based on User-Agent and assign
this to \`$env->{'psgix.woothee'}\`.

You can use this information in your application.

# DEPENDENCIES

Perl 5.8.1 or later.

# BUGS

All complex software has bugs lurking in it, and this module is no
exception. If you find a bug please either email me, or add the bug
to cpan-RT.

# SEE ALSO

[perl](http://search.cpan.org/perldoc?perl) [Woothee](http://search.cpan.org/perldoc?Woothee)

# AUTHOR

Masayuki Matsuki <y.songmu@gmail.com>

# LICENSE AND COPYRIGHT

Copyright (c) 2013, Masayuki Matsuki. All rights reserved.

This library is free software; you can redistribute it and/or modify
it under the same terms as Perl itself.
