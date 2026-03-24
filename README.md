# Bash Server

This is a simple bash server that can be used to serve files from a directory.

> [!WARNING]
> This is a project mad for educational purposes ONLY. It barely follows any of
> the specifications specified in
> [RFC 9112](https://datatracker.ietf.org/doc/html/rfc9112)
> and in [RFC 9110](https://datatracker.ietf.org/doc/html/rfc9110). It has
> practically no error handling and is not meant to be used in production.
> But is a lot of fun implementing and learning about bash.

## Heads up

Bash does not have a built-in way to listen on a port, but we can use the `accept`
command from the loadable builtins that come with bash.
A list of the loadable commands can be found at `$BASH_LOADABLES_PATH`, some systems
do not come with the loadable
builtins installed. In that case, you can build them from source form [https://git.savannah.gnu.org/git/bash.git](https://git.savannah.gnu.org/git/bash.git)
you will need to place the dir in the `$BASH_LOADABLES_PATH`, of add it to the
`$BASH_LOADABLES_PATH`, and follow the INSTALL file.

## Usage

This is a single file bash script, so you can just run it with:

```bash
chmod +x ./bashServer
```

```bash
./bashServer <port>
```

This will start the server on port `http://127.0.01:<port>` and serve files from
the current directory. In another terminal run:

```bash
curl http://localhost:8080/foo.txt
```

Make sure to have a file called `foo.txt` in the current directory.

## Credits

Thanks to [https://www.youtube.com/@yousuckatprogramming](https://www.youtube.com/watch?v=L967hYylZuc&t=2120s)
for the inspiration. Go check out his video.

## License

MIT
