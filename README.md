# tools
My documents and tools on stuff I learn.

24 NOV 17

EXAMPLE csv_in kid with monitoring

echo -e foo\nbar\neee\nxxx\n' | metaproc 'csv_in -i X | noop | slowdown -t 1.1 | bandwidth ; monitor -t 1 '

echo -e foo\nbar\neee\nxxx\n' | metaproc-parallel '%thread(0) {csv_in -i X | noop | slowdown -t 1.1 | bandwidth} ; %thread(1) {monitor -t 1}'


