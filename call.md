## Call for Contesters

Following on the success of the Microsoft Indoor Localization Competition, and before it, the 2007 IPSN Extreme Sensing Competition, we call for participants in the Bosch Device-Free Localization Competition at [CPS-IoT Week 2019](http://cpslab.cs.mcgill.ca/cpsiotweek2019/).  Although there are hundreds of research papers which use RF measurements from commercial wireless communications devices to perform localization, gesture and activity recognition, vital sign monitoring, and other applications, there is little public information directly comparing the performance of different systems against each other. A competition offers an opportunity to make this direct comparison.  The results can help the research community come to conclusions and discover important new directions for research that will have critical impact.

### Categories of Competition

Participating teams will enter in one of these two categories:
1. **Signal Strength Software-only**
2. **Team-deployed Hardware**

#### Signal Strength Software-only

The organizers will deploy a set of 10 sensors that collect received signal strength (RSS) only.  The devices will be Zigbee transceivers at 2.4 GHz measuring on 8 frequency channels.  Each 0.5 seconds, these sensors output the RSS on each pairwise channel (10*9 device pairs) on each of 8 frequency channels, quantized to 1 dB.  These devices will provide real-time RSS to any team in this category.  A team must access the RSS measurements, which will be available on the network, run their DFL software on the data, and post a position estimate (or decide that no person is in the area) at given time instants.

For the Signal Strength Software-Only teams, we will post a [public github RTI project](https://github.com/npatwari/dflcompetition).  We will [adapt the RTI code](https://github.com/npatwari/rti) to make it work for the Signal Strength Software-only category.  In that category, a team modify our software so that they have a system that works out of the box.  Of course, our software could be improved in multiple ways, and modifications and adaptations to the algorithm and its parameters will make its performance improve.

#### Team-deployed Hardware

The team will provide and deploy their own network of RF sensors.  These might include WiFi CSI measurement devices; UWB-IR measurement devices, or some other RF measurement system.  The team will be given time to set up their hardware, and to test their system.  In this case, the team's system must post a position estimate (or again, that no person is in the area) at given time instants.

For the Team-deployed Hardware category, each participating team will discuss their spectral needs in their application, and we will assign channels beforehand when possible to avoid interference.  A team may deploy a maximum of 10 devices.

### Evaluation and Criteria

Teams will primarily be judged by penalized tracking error.  There will be either zero or one person in the area at a time. A team’s system must decide if there is a person in the area, and if so, what the person’s coordinate is.  If, at a time instant, there is a person present and the team estimates their coordinate, their error is the Euclidean distance between actual and estimated coordinate.  If instead, a team’s determination of presence is incorrect, then their error is a constant penalty to be specified later.  If the team correctly determines that no person is present, the error is zero.  The penalized tracking error is the RMS value of the error over all time instants.

### Prizes

The team with lowest penalized tracking error in each category wins first place.  The second-place team in each category will also be awarded.  There will be monetary prizes awarded by our sponsor, [Bosch](https://www.bosch.com/).

### Eligibility

Any industry, university, or government team may compete, with the exception that the organizers will not compete.  At least one member of the team must attend and have a CPSWeek registration.

### Submission

Contesters must submit an 2-page abstract to be considered for participation as a team.  The abstract must explicitely indicate the intended category of compeition and briefly describe the approach and the deployment requirements. 

Submissions are treated as confidential until the competition. Submissions must be at most two (2) pages, including figures, tables, and references. Submission should follow the exact same format as regular, full IPSN 2019 papers. Abstracts should include the names and affiliations of all authors. 

Abstracts should be sent as pdf over email to: npatwari at wustl.edu on or before March 7th 2019 with the following subject line: 2019 Device-free Localization Competition Submission.

### Important Dates
* Abstract Submission Deadline: **March 7, 2019**
* Final Notification: March 15, 2019

Note that Abstracts may be submited **before** the deadline, and early submissions will have early notifications.  If you need to be accepted as a team earlier than March 15 for visa reasons, please apply as early as possible.  The committee will make rolling decisions on applying teams.
