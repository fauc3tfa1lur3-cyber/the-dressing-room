# ✨ The Dressing Room

# Database Schema Documentation

Version: 1.0

---

# 1. Database Purpose

The Dressing Room requires a flexible database structure capable of supporting:

* personal wardrobes
* AI styling intelligence
* beauty profiles
* outfit planning
* shopping recommendations
* Divine Nine experiences
* analytics
* personalization

The database should allow the application to grow from a digital closet into a complete AI-powered personal image ecosystem.

---

# 2. Recommended Database Platform

Recommended options:

Primary:

* Supabase (PostgreSQL)

Alternative:

* Firebase

The database should support:

* user authentication
* image storage
* real-time updates
* secure user data
* scalable relationships

---

# 3. Database Design Principles

The database should prioritize:

## Personalization

Every user should have a unique styling experience.

---

## AI Memory

The system should store enough information for AI stylists to understand:

* preferences
* habits
* personality
* wardrobe patterns
* style evolution

---

## Privacy

Sensitive information should be:

* private by default
* user-controlled
* securely stored

---

# 4. Core Database Entities

Primary tables:

```
users
profiles
style_profiles
beauty_profiles
closet_items
outfits
outfit_items
events
calendar_entries
shopping_items
wishlist_items
ai_memory
stylist_preferences
ambiance_preferences
divine_nine_profiles
appointments
analytics
```

---

# 5. Users Table

Stores account information.

## users

Fields:

```
id
email
created_at
updated_at
authentication_provider
```

---

# 6. User Profile Table

Stores personal information.

## profiles

Fields:

```
id
user_id
first_name
last_name
profile_photo_url
location
timezone
preferred_language
created_at
updated_at
```

---

# 7. Style Profile Table

Stores the user's fashion identity.

## style_profiles

Fields:

```
id
user_id

favorite_colors
disliked_colors

favorite_brands

favorite_styles

favorite_silhouettes

style_goals

comfort_preferences

shopping_preferences

style_notes

created_at
updated_at
```

---

# 8. Style DNA Table

Stores evolving AI-generated style information.

## style_dna

Fields:

```
id
user_id

luxury_glam_percentage

executive_luxe_percentage

soft_girl_percentage

street_luxe_percentage

romantic_percentage

editorial_percentage

custom_styles

last_calculated

```

---

# 9. Style Mood Quiz Table

Stores quiz results.

## style_quizzes

Fields:

```
id
user_id

quiz_date

mood

occasion

energy_level

comfort_level

desired_aesthetic

recommended_style

ai_summary
```

---

# 10. Beauty Profile Table

Stores complete beauty information.

## beauty_profiles

Fields:

```
id
user_id

skin_tone
undertone

height
body_shape

hair_texture

natural_hair_preferences

current_hairstyle

hair_color

wig_collection

protective_styles

makeup_preferences

foundation_match

favorite_lipsticks

favorite_nail_styles

jewelry_preferences

favorite_metals

fragrance_preferences

created_at
updated_at
```

---

# 11. Hair Collection Table

Tracks hair looks.

## hair_profiles

Fields:

```
id
user_id

style_name

category

photo_url

notes

favorite

date_created

```

Examples:

* knotless braids
* wig installs
* silk press
* loc styles
* natural styles

---

# 12. Closet Items Table

The core wardrobe database.

## closet_items

Fields:

```
id
user_id

image_url

item_name

category

subcategory

brand

color

secondary_colors

pattern

material

season

occasion

style_tags

purchase_price

purchase_date

retailer

condition

status

times_worn

favorite

created_at
updated_at
```

---

# 13. Closet Item Categories

Supported categories:

## Clothing

* tops
* bottoms
* dresses
* jumpsuits
* sets
* jackets
* coats

## Shoes

* heels
* sneakers
* boots
* sandals
* flats

## Accessories

* handbags
* jewelry
* sunglasses
* scarves
* hats

---

# 14. Closet Availability Status

Each item can have:

```
available

in_laundry

at_dry_cleaners

stored

unavailable
```

Unavailable items should not appear in AI outfit recommendations.

---

# 15. Closet Location System

Digital luxury spaces:

```
couture_closet

shoe_gallery

handbag_gallery

jewelry_vault

beauty_vanity

coat_lounge

accessory_bar
```

---

# 16. Outfit Table

Stores complete looks.

## outfits

Fields:

```
id
user_id

outfit_name

occasion

aesthetic

season

weather_type

stylist_created_by

image_url

notes

favorite

created_at
```

---

# 17. Outfit Items Relationship

Connects clothing items to outfits.

## outfit_items

Fields:

```
id

outfit_id

closet_item_id

item_role
```

Examples:

```
top

bottom

shoe

bag

jewelry

outerwear
```

---

# 18. Outfit History

Tracks what users actually wear.

## outfit_history

Fields:

```
id

user_id

outfit_id

date_worn

occasion

rating

received_compliments

notes
```

This helps AI learn successful outfits.

---

# 19. AI Memory Table

Stores personalized AI knowledge.

## ai_memory

Fields:

```
id

user_id

memory_type

memory_content

importance_level

created_at

updated_at
```

Examples:

"The user loves gold jewelry."

"The user prefers comfortable heels."

"The user receives compliments wearing jewel tones."

---

# 20. AI Stylist Preferences

Stores stylist customization.

## stylist_preferences

Fields:

```
id

user_id

favorite_stylist

stylist_personality

communication_style

advice_frequency
```

---

# 21. Closet Ambiance Preferences

Stores visual customization.

## ambiance_preferences

Fields:

```
id

user_id

selected_theme

custom_colors

dark_mode

animation_preference

sound_preference

icon_style
```

Examples:

* Black Luxury
* Lavender Luxe
* Sigma Gamma Rho
* Custom Theme

---

# 22. Events Table

Stores styling occasions.

## events

Fields:

```
id

user_id

event_name

event_type

date

location

dress_code

weather

notes
```

Examples:

* wedding
* conference
* date night
* Divine Nine event

---

# 23. Planned Outfits Table

Connects outfits to events.

## planned_outfits

Fields:

```
id

user_id

event_id

outfit_id

status

notes
```

---

# 24. Shopping Intelligence Table

Tracks potential purchases.

## shopping_items

Fields:

```
id

user_id

image_url

product_url

brand

item_name

price

category

ai_analysis

compatibility_score

recommendation

created_at
```

---

# 25. Wishlist Table

Stores future purchases.

## wishlist_items

Fields:

```
id

user_id

item_name

brand

price

image_url

priority

status

notes
```

---

# 26. Cost-per-Slay Tracking

Calculated from closet data.

Formula:

```
purchase_price / times_worn
```

Example:

A $200 jacket worn 20 times:

Cost-per-Slay = $10 per wear

---

# 27. Packing Assistant Tables

## trips

Fields:

```
id

user_id

destination

start_date

end_date

weather

activities
```

---

## packing_lists

Fields:

```
id

trip_id

closet_item_id

category

packed
```

---

# 28. Glam Calendar

## appointments

Fields:

```
id

user_id

appointment_type

provider

date

notes
```

Examples:

* hair
* nails
* facial
* tailoring
* dry cleaning

---

# 29. Divine Nine Profile

## divine_nine_profiles

Fields:

```
id

user_id

organization

chapter

privacy_setting

selected_theme
```

---

# 30. Divine Nine Events

## d9_events

Fields:

```
id

user_id

event_type

organization

date

dress_code

recommended_colors
```

---

# 31. Analytics Tables

## wardrobe_analytics

Tracks:

```
total_items

wardrobe_value

most_worn_items

least_worn_items

favorite_colors

favorite_categories

style_distribution
```

---

# 32. Image Storage Structure

Recommended storage organization:

```
users/

    user_id/

        closet/

        outfits/

        beauty/

        profile/

        inspiration/
```

---

# 33. Security Requirements

All user wardrobe data should be:

* private
* user-owned
* encrypted where appropriate

Users control:

* sharing
* visibility
* social features

---

# 34. Future Database Expansion

Possible future tables:

```
social_connections

friend_votes

mood_boards

fashion_trends

voice_preferences

ar_measurements

shopping_alerts

resale_tracking
```

---

# Final Database Goal

The database should allow The Dressing Room to become a true AI personal image platform.

The system should remember:

what users own,

what they love,

what makes them feel confident,

what they wear,

and how their style evolves over time.

The database is not just storing clothing.

It is storing a person's relationship with their image.
