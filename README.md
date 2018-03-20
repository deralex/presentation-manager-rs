# slideman - a manager for reveal.js slides, written in Rust

## How does it work?

First of all create a _Markdown_ file with the content of your presentation,
assign a name that identifies it and save it in `/static/slides`.

You can use *reveal.js* themes or create your own and put it in `/static/css/theme`.

Finally, you need to add the following information in `/static/slides.json`, which
is the file that contains the list of your presentations.

- `id` - A number to assign and identify each of your presentations
- `file` - The name of the Markdown file
- `title` - The title of your presentation
- `description` - A short description of your presentations' content
- `style` - The name of the theme file

### Example

```
[
  {
    "id": "1",
    "file": "rust-and-perl-love.md",
    "title": "Rust and Perl - You got to love them!,
    "description": "A lovestory about Rust and Perl",
    "style": "league.css"
  }
]
```

## Usage

If you freshly cloned the repo, you have to execute

```
cargo build
```

before starting slideman.

*Important!*: You need the `nightly` builds of Rust!

If you're using `rustup`, just execute the following commands:
```
rustup install nightly
rustup default nightly
```

After a successful build, you can call Cargo to run slideman or execute the binary directly:
```
cargo run
```
or
```
./target/debug/slideman
```

## Author

Alexander Kluth <deralex@cpan.org>, 2018. Licensed under MIT.

## Credits

Based on [presentation-manager-rs](https://github.com/mattdark/presentation-manager-rs) developed by Mario Garcia (mattdark), (c) 2018.
