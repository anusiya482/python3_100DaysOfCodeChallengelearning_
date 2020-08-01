# python3_100DaysOfCodeChallengelearning_
#sys module

import sys 
sys.stderr.write("this is stderr text\n")
sys.stderr.flush()
sys.stdout.write('this is stdout text\n')
print(sys.argv)
if len(sys.argv)>1:
    print(sys.argv[1])

#urllib module

    
import urllib.request
import urllib.parse
#x=urllib.request.urlopen('https://www.google.com')
#print(x.read())
url='http://pythonproramming.net'
values={'s':'basics'
        'submit':'search'}
data=urllib.parse.urlencode(values)
data=data.encode('utf-8')
req=urllib.request.Request(url,data)
resp=urllib.request.urlopen(req)
respData=resp.read()
print(respData)
import urllib.request
try:
    x=urllib.request.urlopen('https://www.google.com/search?q=test')
    print(x.read())

except Exception as e:
    print(e)

