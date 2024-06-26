# fuff-tool-cookbook
Description: fuff is a powerful and flexible tool designed for fuzzing HTTP endpoints, particularly useful for web application security testing. It allows security professionals to discover hidden files, directories, parameters, and other vulnerabilities by sending numerous HTTP requests with various inputs. With its highly customizable and performant nature, fuff stands out as an essential tool in a security analyst's toolkit. Installation To install fuff, use the following command: go install github.com/ffuf/ffuf/v2@latest Ensure that Go is installed and properly configured on your system. (Or) We can simply use command : "apt-get install fuff". Commmand: sudo apt-get install fuff
 ![Screenshot 2024-06-26 112121](https://github.com/prasannatulasiA/fuff-tool-cookbook/assets/85549966/2f23eaf7-981f-4bec-8b98-c7e22db7876e)

Or by using the another method to install fuff by using the url With its highly customizable and performant nature, fuff stands out as an essential tool in a security analyst's toolkit. Installation To install fuff, use the following command: go install github.com/ffuf/ffuf/v2@latest Ensure that Go is installed and properly configured on your system. (Or) We can simply use command : "apt-get install fuff

![Screenshot 2024-06-26 112200](https://github.com/prasannatulasiA/fuff-tool-cookbook/assets/85549966/8209ebf0-c869-425c-8e1b-7be4a31d3c10)

![Screenshot 2024-06-26 112311](https://github.com/prasannatulasiA/fuff-tool-cookbook/assets/85549966/dda10d18-c7f7-4112-8a89-a13825d80ee8)

![Screenshot 2024-06-26 124026](https://github.com/prasannatulasiA/fuff-tool-cookbook/assets/85549966/19c894d6-3f1d-435d-8320-8184bd271997)

Usage of fuff: 1.Fuzzing Directories To fuzz directories on a website: "fuff -u https://example.com/FUZZ -w wordlist.txt" • -u: URL with the placeholder FUZZ where the payload will be inserted. • -w: Path to the wordlist file containing potential directory names.

![Screenshot 2024-06-26 124242](https://github.com/prasannatulasiA/fuff-tool-cookbook/assets/85549966/3ebabfe0-585d-448c-a8ed-d1531c7b0f47)


2.Fuzzing GET Parameters To fuzz GET parameters: "fuff -u https://example.com/page?FUZZ=value -w wordlist.txt"

![Screenshot 2024-06-26 124941](https://github.com/prasannatulasiA/fuff-tool-cookbook/assets/85549966/bce055d8-fe9d-4d29-b92c-0685633b0ef4)


3.Fuzzing POST Data To fuzz POST data: "fuff -u https://example.com/login -w wordlist.txt -X POST -d 'username=admin&password=FUZZ' " • -X POST: Specifies the HTTP method to use (POST in this case). • -d: Data to be sent in the body of the POST request.

![Screenshot 2024-06-26 125146](https://github.com/prasannatulasiA/fuff-tool-cookbook/assets/85549966/1e8dcba3-7319-4bf5-8163-1c7da8ac53ea)

4.Multi-Wordlist Fuzzing To use multiple wordlists simultaneously: "fuff -u https://example.com/FUZZ/FIZZ -w wordlist1.txt -w wordlist2.txt"

5.Using Filters To filter out results based on response status codes, sizes, or words: • Filter by status code: fuff -u https://example.com/FUZZ -w wordlist.txt -fc 404

• Filter by response size: fuff -u https://example.com/FUZZ -w wordlist.txt -fs 1234

• Filter by number of words in the response: fuff -u https://example.com/FUZZ -w wordlist.txt -fw 100

![Screenshot 2024-06-26 125414](https://github.com/prasannatulasiA/fuff-tool-cookbook/assets/85549966/13e92f2f-9649-4c1e-b6f8-f38dc63d46ef)


6.Recursion To recursively fuzz discovered directories: fuff -u https://example.com/FUZZ -w wordlist.txt -recursion

![Screenshot 2024-06-26 125523](https://github.com/prasannatulasiA/fuff-tool-cookbook/assets/85549966/ba16adc1-69b9-453d-b07d-440414c5a630)


7.Specifying Headers To specify custom headers: fuff -u https://example.com/FUZZ -w wordlist.txt -H 'Authorization: Bearer token' -H 'Custom-Header: value'

8.Output Options To save the output in various formats: • JSON: fuff -u https://example.com/FUZZ -w wordlist.txt -o output.json -of json

• CSV: fuff -u https://example.com/FUZZ -w wordlist.txt -o output.csv -of csv

9.Speed and Timing To control the speed and timing of requests: • Number of concurrent requests: fuff -u https://example.com/FUZZ -w wordlist.txt -t 50

• Rate limiting (requests per second): fuff -u https://example.com/FUZZ -w wordlist.txt -rate 100
