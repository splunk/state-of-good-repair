
# State of Good Repair Splunk App
This app accompanies the 2019 .conf ["IoT1318 - Maintaining a state of good repair with predictive analytics"](https://conf.splunk.com/learn/session-catalog.html?search=nesavich) presentation and provides:
* Examples of all SPL covered in presentation.
* Takeaways for follow up / implementation of similar use cases at your company.
* Education / training 

# Prerequisites
Before you install the State of Good Repair Splunk App, make sure your system meets the following minimum prerequisites:

* Splunk Enterprise, Splunk Light, or Splunk Cloud version 6 or later. 
* [Maps+](https://splunkbase.splunk.com/app/3124/) - Fully configured 
* [Splunk Machine Learning Toolkit](https://splunkbase.splunk.com/app/2890/) - Fully configured 
* Optional - [Google Maps API key](https://developers.google.com/maps/documentation/javascript/get-api-key) 

This is to enable the street view pop ups demonstrated in the presentation.  Customers electing to enable this will need to populate their key in the description field in ... ```sogr/default/data/ui/views/Dispensary_Map.xml``` found at the end of line 37.

---

### Caveats / Tips
A couple tips for sharing knowledge objects created in MLTK with other apps in Splunk.

##### Knowledge Objects
Set permissions in MLTK app with ```All Apps (system) ``` and permissions with ```Everyone Read and admin & power write```.  This will allow for reference to ML knowledge objects you create in other apps.

##### Referencing ML Models - __mlspl* files
ML models are fit to special lookups that begin with ```__mlspl_<name of model>``` under the account they are created.  

IE ```$SPLUNK_HOME/etc/users/<user>/Splunk_ML_Toolkit/lookups/__mlspl_<name of model>```  

These __mlspl file needs to reside in the lookups directory of the app(s) referencing it.

IE ```$SPLUNK_HOME/etc/apps/<app>/lookups/__mlspl_<name of model>```

---

### References
Links to helpful blogs, articles, how to videos and more are listed below.

##### [Anomaly Detection Video](https://www.youtube.com/watch?v=lyPN6q6z9Es&feature=youtu.be) - How To Video
Abbreviated How To video showing the water leak detection use case demonstrated in this session.

##### [Shining a Light on Industrial Data](https://www.splunk.com/blog/2014/10/22/shining-a-light-on-industrial-data.html) - Blog
Collecting, Connecting, and Enriching Industrial Data data with the [Kepware IDF to Metrics Index Add-on for Splunk](https://splunkbase.splunk.com/app/3963/).

##### Getting IoT Data In
While the use cases covered in this presentation all relied on [Splunk DB connect](https://splunkbase.splunk.com/app/2686/), there are many other ways of collecting IoT data that are beyond the scope of this presentation which are listed below for your reference:
* [Splunk Stream](https://splunkbase.splunk.com/app/1809/)
* [REST API Modular Input](https://splunkbase.splunk.com/app/1546/)
* [Splunk Add-on for OPC](https://splunkbase.splunk.com/app/4246/)
* [Kepware IDF to Metrics Index Add-on for Splunk](https://splunkbase.splunk.com/app/3963/)
* [WeavingThings IOT edge connectivity platform](https://splunkbase.splunk.com/app/3922/)

##### Best of .conf 2019 IoT sessions - TBD
Check back after .conf for list of some of best IoT sessions of 2019 .conf.
