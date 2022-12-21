directdial
==========

Direct Dial application.

Ready to be used with Heroku.

## Usage Examples
###Default usage => bridge call to the 'To' parameter

* ####Direct Dial <br/>
http://13.127.140.35:5001/direct-dial/?DialMusic=real&CLID=919624705678

* ####Inbound trunk <br/>
http://13.127.140.35:5001/response/sip/inbound_trunk/?DESTINATION=13.235.91.239

* ####Outbound trunk <br/>
https://www.plivo.com/docs/enterprise/outbound-easytrunk#forward-calls-from-your-soft-switch

* ####Set call forwarding <br/>
  http://server/response/sip/route/?ForwardTo=15555559999<br/>

* ####Set dial music for call ring <br/>
**Play music from an URL while the call is getting connected**<br/>
  http://server/response/sip/route/?ForwardTo=15555559999&DialMusic=http://myserver/playsound/
  <br/>or<br/>
**Ring back tone from the actual device**<br/>
  http://server/response/sip/route/?ForwardTo=15555559999&DialMusic=real

* ####Disable outbound calls<br/>
**to phone numbers**<br/>
  http://server/response/sip/route/?DisableCall=number <br/>
  so, when 'To' is a number the XML response is a simple hangup. e.g. <br/>
  http://server/response/sip/route/?To=15555559999&DisableCall=number
<br/> 
**to SIP endpoints**<br/>
  http://server/response/sip/route/?DisableCall=sip <br/>
  So, when 'To' is a SIP uri the XML response is a simple hangup.
<br/> 
**to all destinations**<br/>
  http://server/response/sip/route/?DisableCall=all
