# staep-1
from json import dumps, loads
from urllib2 import urlopen, Request

 
info = {'token':'haTzzCr65h'}

 
token = dumps(info)

 
req = Request('http://challenge.code2040.org/api/getstring', token)

 

string = loads(urlopen(req).read())['result']

 

gnirts = string[::-1]

 
print "This is the reversed string: " + gnirts

 

send = {'token':'haTzzCr65h', 'string':gnirts}

 

res = Request('http://challenge.code2040.org/api/validatestring', data=dumps(send)) 

 
final = loads(urlopen(res).read())['result']


print final
