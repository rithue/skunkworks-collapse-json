# Steps to render FlameGraph svg file from explain output

## Clone the FlameGraph repo and the rithue/skunkworks-collapse-json repo

git clone https://github.com/brendangregg/FlameGraph.git

git clone https://github.com/rithue/skunkworks-collapse-json.git

## Run the following commands to get the collapsed output text file under the file name “explain.json.txt”

cd skunkworks-collapse-json

python3 convertJsonToCollapsed.py explain.json

## Run the following commands to get the svg file under the name kernel.svg

cd ..

cd FlameGraph

./flamegraph.pl /Users/rithu.eswaramoorthy/jsonToCollapsed/explain.json.txt > kernel.svg

## Open the svg file on a web browser to display the FlameGraph

