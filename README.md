Simple progress bar package for Python 3.

Usage
-----
`lightbar` takes advantage of Python's generator. To use it, you'll need to
provide a generator functions that produces a progress number from 1 to 100.
The rest is taken care of by `lightbar` itself.

    def progress():
        for i in range(1, 101):
            yield i
            time.sleep(0.1)

    from lightbar import LightBar
    LightBar(progress)()

You can customize the block character and the width of the bar:

    LightBar(progress(), block='-', width=20)


TODO
----
1. Disable cursor
2. Allow customized output
