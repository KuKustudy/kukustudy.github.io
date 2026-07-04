---
layout: post
title:  "How to create backup dump file for supabase database"
date:   2026-07-04 15:28:00 +1000
categories: update blog
---

### How to create backup dump file for supabase database

1. download supabase CLI and docker (docker is needed for creating the database dump)

    download supabase CLI by entering this command in command prompt:
    `brew install supabase/tap/supabase`

    download docker from https://www.docker.com/products/docker-desktop/


2. enter following in command prompt, it will pop up a window ask you to login:

    `supabase login`


3. link supabase database using database id, I make this up, please don't copy and paste the database id directly:

    `supabase link --project-ref [database id]`

    e.g. `supabase link --project-ref deabcdhbbmcmabcddcsa`


4. store the database dump to desired path
   
    `db dump -f [path to desired storage directory]/backup.sql`

    e.g. `db dump -f ~/Downloads/backup.sql`

