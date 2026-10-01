# EatNext sign-in and access page

Static Supabase Auth page for the GitHub Pages route `/eatnext-auth/`. The parent `config.js` contains only the public Supabase project URL and publishable key.

Users request a passwordless email sign-in link explicitly. The callback is fixed to `https://mchenla.github.io/eatnext-auth/`; a valid `authorization_id` is preserved so the user can return to the pending consent. The page never accepts a caller-provided redirect destination. After Supabase processes the callback, it verifies the signed-in user and loads OAuth authorization details. Access is granted or denied only after an explicit click.

Run `python3 self_check.py` for local static checks. Do not put service-role keys or user tokens in this directory.
