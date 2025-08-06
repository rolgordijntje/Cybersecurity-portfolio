## August 6, 2025 TryHackMe Userstring-Analysis

Today was a productive and educational day. I'm currently working in SOC Level 1 > Cyber Defence > Frameworks > Pyramid of Pain.
Task 6 focuses on Network Artifacts.

We're using **TShark** to filter out User-Agent strings with the following command:

**tshark -Y http.request -T fields -e http.host -e http.user_agent -r analysis_file.pcap**

The User-Agent string we're seeing is:

```Mozilla/4.0 (compatible; MSIE 7.0; Windows NT 6.1; Trident/7.0; SLCC2; .NET CLR 2.0.50727; .NET CLR 3.5.30729; .NET CLR 3...)```

So, what is a User-Agent string?
You could call it your browser's identity card — it tells the server what software and version you're using.

In this example:

- Mozilla/4.0 is mostly there for compatibility with older websites.
- compatible; MSIE 7.0 refers to Microsoft Internet Explorer 7.
- But, the precense of Tridant/7.0 reveals that this is actually Internet Explorer 11 (Trident 7 is the rendering engine for IE11)
 

    


