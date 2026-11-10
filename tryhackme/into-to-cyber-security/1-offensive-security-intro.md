**"To outsmart a hacker, you need to think like one."**

# Offensive Security Intro

This room introduces the basics of offensive security and shows how attackers may look for weaknesses in a website.

## Gobuster

Gobuster is a command-line tool used to find hidden pages or directories on a website by testing names from a wordlist.

## Virtual Machine

The virtual machine contains a fake banking website. In this room, Gobuster is used to discover hidden pages that may expose important functionality.

## Steps

1. Open the terminal.
2. Run `gobuster -u http://fakebank.thm -w wordlist.txt dir`
3. Review the results.

<img width="770" height="531" alt="image" src="https://github.com/user-attachments/assets/8802ecfa-ee50-482c-9ca3-5b02b9356003" />

The results show that `/bank-transfer` returns `Status: 200`, meaning the page is accessible.

4. Visit the discovered page.

<img width="859" height="814" alt="image" src="https://github.com/user-attachments/assets/1a229d6d-d745-4638-bdcb-c35089e73142" />

This shows how exposed pages can reveal sensitive functionality that an attacker could abuse.

## Takeaway

This room showed how simple enumeration can uncover hidden pages on a website and why sensitive functionality should not be left easily accessible.
