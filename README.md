# NetworkingFinalProject
In this project, we studied attacks on secure messaging apps. We first read the article "Practical Traffic Analysis Attacks on Secure Messaging Applications" by Alireza Bahramali, Amir Houmansadr, Ramin Soltani, Dennis Goeckel, and Don Towsley. This article discusses how traffic analysis attacks can be used to identify users and activities in secure messaging apps and gives numerous examples of this technique might be used, even if the messages themselves are encrypted. After carefully reading the article and highlighting important points we’ve summarized it in Hebrew in the Dry Part of the project.

We then conducted our own experiments to see how traffic analysis attacks could be applied to WhatsApp. We created four different groups and sent different types of messages in each group (text messages, voice recording, images etc..). We used Wireshark to record the network traffic for each group and convert the recordings into a csv file which was later used with Python to analyze the recordings by graphing our recording as shown in the article.

Our results showed that traffic analysis attacks can be used to identify users and activities in WhatsApp, even if the messages themselves are encrypted. For example, given the fact that the attacker is already in those messaging groups (either the group was open/public in which case he could just add himself or else someone who was already an admin in that specific group added them) we were able to identify which users were sending images, voice recordings, and text messages and exactly in what time. 
Our results suggest that traffic analysis attacks are a serious threat to the security of secure messaging apps. App developers need to take steps to decrease the risk of traffic analysis attacks, such as using strong encryption, another important thing we learnt from the article is that adding background web-browsing traffic may reduce the accuracy of the attacks from 93% down to as low as 70% which is significant.

In addition to the technical findings, we also learned a few important lessons from this project. First, it is important to read the research literature before conducting your own experiments. The article we read provided us with valuable insights into the traffic analysis problem and helped us to design our experiments more effectively.
Second, it is important to use real-world data in your experiments. The data we collected from WhatsApp was much more realistic than the synthetic data that is often used in research papers. We can confidently say that WhatsApp is one of the most commonly used app therefore we had to adjust our experiments according to that fact and sent messages that are a bit larger than usual in order to spot exactly when the message we meant to track was sent and when the attacker just received messages from other group they didn’t mean to track.  This made our results more credible and helped us to draw more accurate conclusions.

Overall, we believe that this project was a success. We learnt a great amount about traffic analysis attacks and we were able to demonstrate that these attacks are a serious threat to the security of secure messaging apps. 

## Use our code

In order to use the code, clone the repository, or download it to your own computer. open the ipynb file using jupyter notebook. Paste the csv saved recordings into the file's directory, change the path inside the code to your updated csv file names, and run the code.

## Navigate through our project
src directory: graphing code

resources directory: contains both our CSV and PCAP files

## References
Practical Traffic Analysis Attacks on Secure Messaging Applications:  https://www.ndss-symposium.org/wp-content/uploads/2020/02/24347-paper.pdf
