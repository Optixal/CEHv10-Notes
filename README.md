# CEHv9-Notes

![ifis_ceh1-1](https://user-images.githubusercontent.com/19287477/35230991-93a6f604-ffd2-11e7-9436-f45556c484e8.png)

## Personal and Public Notes

All notes listed below are very useful, but to save time, you should read the most useful and important ones first. Here is the read order, starting from the most useful, to the least (but still somewhat useful).

1. Personal Reddit Comments Below
2. CEH v9 Notes - Dads Man Cave.pdf
3. CEH Cheatsheet.pdf
4. CEH Cheatsheet 2.pdf
5. CEH Read Topics.pdf
6. CEH Impt Cmd Line Programs.txt
7. CEH Tools.pdf

## Personal Reddit Comments

Here are a bunch of personal responses I made on reddit to CEH takers. I believe they will come in handy.

*Source: I'm 14 and dad wants me to give CEHv9 in a week, NEED DESPERATE HELP! - https://www.reddit.com/r/CEH/comments/5l4xi2/im_14_and_dad_wants_me_to_give_cehv9_in_a_week/*

```
just passed a week ago, was pretty doable, you should be fine. the questions are random for each session, so getting easy/hard questions will be based mostly on chance.

important topics:

* common port numbers and their purposes
* semi-recent vulnerabilities: shellshock (appeared in 3+ questions), heartbleed and poodle
* popular cmd line tools (nmap (tcp, syn, ack [for firewalls], fin [xmas, null], idle scans), netcat, hping3, firewalk, nslookup, dig, john, ssh, tcpdump, metasploit)
* popular GUI programs (roughly know how they work) (wireshark (+ filters), zenmap (nmap gui), maltego, burpsuite, ettercap, cain & abel, nessus, kismet wireless, colasoft packet builder)
* white/gray/blackbox pentesting (all three came out, free marks) (corresponds to: full/partial/no knowledge of internal organization respectively)
* cross site scripting and cross site request forgery
* firewall/ids evasion techniques
* snort ids rule format (came out in a question)
* icmp codes
* regional whois registries (Arin (america), LAcnic (latin america), ripEncc (europe), AFRnic (africa), APnic (asia pacific))
* offline human based attacks (~3+ questions) - social engineering, dumpster diving, tailgating
* wireless - wep (24 bit IV, RC4), wpa (48 bit IV, TKIP), wpa2 (48 bit IV, AES CCMP)
* crypto - symmetric ([3]des, aes), asymmetric (public key) (rsa, diffie hellman), hash (md5 - 128bit, sha1 - 160 bit, sha256 - 256 bit, etc)

i've also compiled a bunch of notes which u may find useful, they are on github over here: https://github.com/Optixal/CEHv9-Notes

last notes: after taking the exam, i realized that you do not need to memorize every tool out there in the wild, just study the popular ones that aren't outdated, as they'll throw u questions like "Which reconnaisance tool would you use for mapping out relational data of a target? Options: netcat, hping3, whois, maltego - ans: maltego", where the options usually consist of popular tools, and half of the options are definitely out. most of them can be found on kali linux. i also did some practice on http://www.aiotestking.com/ec-council/category/exam-312-50v8-certified-ethical-hacker-v8/ to prep for my exams.

all the best for yours!

---

ur welcome!

nope i did not get those questions, i believe they'll ask more about the generalized standards (eg. pci-dss (payment cards), iso/iec 27001:2013 (infosec in a company), hipaa (healthcare), sarbanes oxley act (protect investors), dmca (protect content), fisma (federal operations)).

there weren't many of these questions though, in fact there were more questions on ethics (5+ questions) compared to laws/standards (1/2 questions?). those ethics questions are pretty straightforward, one was "You found the password to your manager's bitcoin wallet in a text file on his machine while conducting a pentest. What do you do next?" Options:

A - ignore it and continue
B - steal it and sell the password
C - steal it and transfer the bitcoins
D - pause the pentest and inform him immediately

ans: D.. so they shouldn't be much of a problem.

your grade will be calculated and displayed immediately after ur exam (not pass / pass). if you do fail, you'll have to arrange another retest and pay the full price of it.. don't worry so much on failing though, study the important topics, do a few more practice questions, and do your best during the exam. and the fact that ur taking the exam at 14 is quite surprising, i'm sure ur dad understands that

---

yes, not sure whether you can get a discount tho. but for my school, those who needed to retake had to pay the full cost.

for the scans, understand how a tcp handshake work (syn, syn/ack, ack), and also understand how each type of scan work by:

knowing the purpose of each scan (map out firewall's rules - ack scan, sneak pass a firewall to scan a system behind it - fin/null/xmas scans, "stealth" scan - syn scan, "default" scan - tcp scan, udp port scan - udp scan)
knowing how each of those scan determines the state of a port (open, open|filtered, closed, etc.) by analyzing the response packets (syn/ack - open, no response - open|filtered, rst - closed (or in ack scan - unfiltered), udp - open udp port, icmp type 3 code 3 - closed udp port)
for the nmap scans, this is definitely the best reference: https://nmap.org/book/man-port-scanning-techniques.html

and of course, do try each of the scans using command line nmap, bcos reading is one thing, doing it hands-on is another. a tip is to use the -vvv (level 3 verbose mode) while conducting each scan to see the packet responses, it will be in the "REASON" column, this will help you understand how the state of a port is determined.

---

nmap:

http://www.aiotestking.com/ec-council/which-nmap-switch-would-the-hacker-use-6/
http://www.aiotestking.com/ec-council/which-type-of-packet-inspection-is-the-firewall-conducting-3/
for nmap, also study the other flags that can be used along with scans. e.g: -T4 (scan speed, T4 is lvl 4 aggressive speed), -O (operating system detection), -Pn/-P0 (no ping, skip discovery stage and assume system being scanned is online), -A (aggressive scan), -F (fast scan), --script=[script]/-sC (nmap scripting engine). and to add on to the other scans: -sP (ping sweep), -sO (protocol scan, used for determining whether the system being scanned uses tcp, icmp, etc.)

for the rest of the tools, i did not encounter many questions that involved their syntaxes (probably only 1 question), so just know what they are used for and if you have time, learn their basic syntaxes. questions regarding those tools (other than nmap) will usually include them in a list of tools and ask which of them best suits the question's description. eg: http://www.aiotestking.com/ec-council/what-would-be-the-name-of-this-tool-5/

```

---

## Thanks For Reading

*If you find these useful, make sure to star:star: the repo to let me know you appreciate it :) All the best for your certification!*
