<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Thanks again! Now go create something AMAZING! :D
-->

<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->

<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://github.com/GiovanniBaccichet/bachelor-thesis">
    <img src="imgs/Light_bulb_perspective_matte_s.png" alt="Logo" width="170">
  </a>

  <h3 align="center">Bachelor Thesis</h3>

  <p align="center">
    Information and Communications Engineering @ University of Trento
    <br />
    <a href="https://github.com/GiovanniBaccichet/bachelor-thesis/releases/tag/1.0"><strong>Download PDF »</strong></a>
    <br />
    <br />
    <a href="https://baccichet.org">Giovanni Baccichet</a>
    |
    <a href="https://www.granelli-lab.org/">Prof. Fabrizio Granelli</a>
  </p>
</p>

<!-- ABSTRACT -->

## Abstract

Cyber security has become a matter of global interest and importance. In the last couple of
years, especially with the pandemic situation going on, several attacks were performed against
companies and critical structures. Since almost every intrusion is put in place through the network,
understanding how to identify and report malicious activity in a lightweight, reliable way is vital.
This dissertation aims to use Machine Learning (ML) techniques to detect and identify network
attacks. For this purpose an Intrusion Detection System (IDS) has been implemented and designed
to be able to classify particular behaviors of network traffic with a low false-positive rate, taking
also into cosideration user’s privacy, which lately has become a concern.
The approach used in this project differs from the traditional one because of the metrics employed
in the classification process: instead of inspecting the payload of each network packet, the IDS
observes its flow. In this context a flow is a tuple of 5 values (source IP, destination IP, source
port, destination port, protocol) from which a set of useful features can be extracted and passed to
the ML model for analysis.
The developed piece of software was thought to be deployed with ease in a realistic scenario. For this
reason it can be interfaced with Software Defined Network (SDN) for saving and then classifying
network traffic. To achieve this integration, a script for the open-source controller Ryu has been
developed: it creates a L3 switch that can generate a .pcap file containing the network packets
passing through it. This architecture is particularly flexible due to its modularity: the system itself
can work independent of the controller chosen, which represents the only component to adapt to.
Almost the entirety of the system has been built using Python, since it represents a good starting
point for prototyping. Random Forest (RF), the ML algorithm of choice, was trained using a
Jupyter Notebook, on the CICIDS2017 dataset resulting in an accuracy of 99.91% and an F1 score
of 99.86%.
