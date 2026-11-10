cd ~/cybersecurity
cat > README.md << 'EOF'
# Cybersecurity

I'm a computer science student at Texas A&M focusing on cybersecurity. This repo is where I document what I'm learning: the rooms I complete, the projects I build, and what went wrong along the way. Everything here is written in my own words.

## What's here

| Folder | What it is |
|--------|------------|
| [`tryhackme/`](tryhackme/) | Notes from TryHackMe rooms: what each room covered, what I did, and what I learned |
| [`homelab/`](homelab/) | My home lab build: hardware, setup, and what I run on it |

I also work through OverTheWire. Those notes are kept private, because the wargames ask players not to publish solutions.

## Skills I'm building

- Linux command line, including file searching, permissions, and text processing
- SSH, key-based login, and basic networking
- Git and GitHub workflows
- Vim
- Encoding and compression (Base64, ROT13, gzip, bzip2, tar)

## Where I'm headed

- Finish the TryHackMe Pre-Security path and move on to the next paths
- Keep building out the home lab and documenting it
- Learn Python for everyday tasks and small security scripts
- Compete in beginner-friendly CTFs

## How my notes are written

Each write-up covers the goal, the concept, what I did, what went wrong, what I learned, and how the same idea applies in the real world. The "what went wrong" part is the one I care about most, since that's where the learning happens.

## Contact

GitHub: [diego-garcia-dev](https://github.com/diego-garcia-dev)
EOF
grep -rIniE 'BEGIN .*PRIVATE KEY|password|passwd|secret|token' --exclude-dir=.git . | head -30
