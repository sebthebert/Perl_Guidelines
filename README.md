Perl Guidelines
===============

Perl Guidelines for code, documentation and tests

## Code Guidelines

### File manipulation

  * Don't use bareword filehandles (checked by [InputOutput::ProhibitBarewordFileHandles](https://metacpan.org/pod/Perl::Critic::Policy::InputOutput::ProhibitBarewordFileHandles) Perlcritic policy)
  * Always use the three-argument form of `open` (checked by [InputOutput::ProhibitTwoArgOpen](https://metacpan.org/pod/Perl::Critic::Policy::InputOutput::ProhibitTwoArgOpen) Perlcritic policy)

Example:
```perl
open($fh, '<', 'foo.txt');
```

It's probably a good idea to use [File::Slurp module](https://metacpan.org/pod/File::Slurp) for bigger programs/scripts.

## Documentation Guidelines

```perl
package My::Module;

=head1 NAME

My::Module - Module doing great stuff

=head1 DESCRIPTION

Module doing great stuff and a lot more !

=head1 SYNOPSIS

    use My::Module;

    my $mine = My::Module->new({user => $user, password => $password});

    $mine->something($var);

=cut

...

1;

=head1 AUTHOR

Firstname Lastname <user@somedomain.com>

=cut

```

## Tests Guidelines
