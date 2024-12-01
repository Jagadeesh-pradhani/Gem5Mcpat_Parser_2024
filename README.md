# Gem5Mcpat_Parser_2024
Updated version of parser <br>
This script converts Gem5 simulation statistics to McPAT compatible input files. It supports multiple cores as well as multiple private or one shared L2 cache. <br>
Tested with ruby memory only



### Usage



```sh
 usage: parser.py [-h] --config PATH --stats PATH --template PATH
                                    [--output PATH]

        Gem5 to McPAT parser

        optional arguments:
        -h, --help            show this help message and exit
        --config PATH, -c PATH
                                Input config.json from Gem5 output.
        --stats PATH, -s PATH
                                Input stats.txt from Gem5 output.
        --template PATH, -t PATH
                                Template XML file
        --output PATH, -o PATH
                                Output file for McPAT input in XML format (default:
                                mcpat-in.xml)
```

### Example

```sh
git clone https://github.com/Jagadeesh-pradhani/Gem5Mcpat_Parser_2024.git
cd Gem5Mcpat_Parser_2024/
```
run
```sh
python3 parser.py --config m5out/config.json --stats m5out/stats.txt --template templates/template_latest.xml
```

### McPat
```sh
./mcpat -infile mcpat-in.xml
```





