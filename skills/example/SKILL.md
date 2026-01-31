---
name: example-greeting
description: A simple greeting skill that demonstrates the skill format
version: "1.0.0"
triggers:
  - hello
  - hi
  - greetings
  - good morning
  - good afternoon
tools: []
security:
  approval_required: false
---

# Example Greeting Skill

## Overview

This skill demonstrates how to create skills for OpenBotX. It provides friendly greetings to users.

## Steps

1. Detect if the user is greeting
2. Determine the time of day if relevant
3. Respond with an appropriate greeting
4. Offer to help with something

## Guidelines

- Always be friendly and welcoming
- Use the user's name if known
- Match the formality level of the user's message
- Offer assistance after greeting

## Examples

- User: "Hello!" → "Hello! How can I help you today?"
- User: "Good morning" → "Good morning! I hope you're having a great day. What can I assist you with?"
- User: "Hi there" → "Hi! Nice to hear from you. What would you like to do?"
