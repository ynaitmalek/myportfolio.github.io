---
title: "Gloveraille"
meta_title: ""
description: "An other braille keyboard."
date: 2023-05-29T14:00:00Z
image: "/images/projects/gloveraille_schema.png"
categories: ["IoT"]
author: "Youssef Nait Malek"
tags: ["Python", "AI"]
draft: false
---
## Introduction

Glovraille is a glove that functions as a Braille keyboard, powered by an Arduino board.

{{< button label="GitHub Page" link="https://github.com/NaitMalekYoussef/Gloveraille" style="solid" >}}

## Concept

The concept is very simple, as shown in the figure bellow, the user will type a character using the selector and the character zone, when the user finish typing the character, he can confirm whether it is a number or character using one of the options in the fourth finger, the character is then sent to the connected device (computer, phone or other compatible device) after confirmation. The user can also send space, delete, enter or correct.
The Glovraille consists of 10 pads, 6 for character input, 3 for different options and one pad as a selector. The role of each pad is as follow:
* Pad GND : the selector ( connected to GND pin of the Arduino)
* Pads from 0 to 5 : character zone, this pads will construct the character (Arduino pins; 2,3,4,5,6 and 7).
* pad 6: When this pad is selected using the selector, if the user already taped a character, it will confirm the **character** and sent it to the connected device. Otherwise, if the user did not enter any character, this will send a **space** to the device. (Pin 11 in the Arduino).
* pad 7: When this pad is selected using the selector, if the user already taped a character, it will confirm the **number** and sent it to the connected device. (Pin 12 in the Arduino).
* pad 8: When this pad is selected using the selector, if the user already taped a character, it will correct the character, in other words, this action will clear the character buffer and does not send anything to the connected device.  Otherwise, if the user did not enter any character, this will send a **return character**   to the device. (Pin 13 of the Arduino).
