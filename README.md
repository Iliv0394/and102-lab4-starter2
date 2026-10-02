# Campground Explorer

Submitted by: Isaac Livingston

Campground Explorer is an Android app that displays campground information from the National Park Service API. The app shows a scrollable list of campgrounds with each campground's name, location, description, and image. Users can tap on a campground to open a detail screen with more information about that campground.

Time spent: about 6.5  hours spent in total

## Required Features

The following **required** functionality is completed:

- [x] Campgrounds are displayed using a RecyclerView
- [x] Each campground displays its name
- [x] Each campground displays its description
- [x] Each campground displays its latitude and longitude
- [x] Campground images are downloaded and displayed using Glide
- [x] User can tap on a campground
- [x] User can navigate to a Campground Details screen
- [x] The selected campground information is passed to the DetailActivity
- [x] Detail screen displays the campground name
- [x] Detail screen displays the campground latitude and longitude
- [x] Detail screen displays the campground description
- [x] Detail screen displays the campground image

## Optional Features

The following **optional/stretch** features are implemented:

- [ ] Additional XML styling

## Additional Features

The following **additional** features are implemented:

- [x] Campground information is loaded from the National Park Service API
- [x] API response is parsed using Kotlin Serialization
- [x] Nested JSON image information is handled using a CampgroundImage data class
- [x] RecyclerView is organized using a LinearLayoutManager
- [x] The first available campground image is displayed
- [x] Campground objects are passed between activities using an Intent
- [x] Campground and CampgroundImage objects are serializable
- [x] API key is stored in an apikey.properties file instead of being hard-coded
- [x] API key is kept out of the GitHub repository
- [x] Project was successfully committed and pushed to GitHub

## Video Walkthrough

Here's a walkthrough of the implemented features:

[ https://drive.google.com/file/d/1ohKQgmmgb5VpniXSZbOi60IZrtlsDbOk/view?usp=sharing ]

## Notes

One challenge was setting up the starter project correctly. At first, the GitHub repository was empty because it was created as a new repository instead of being forked from the CodePath starter repository. This was fixed by creating a proper fork and cloning the new fork into Android Studio.

Another challenge was setting up the National Park Service API key. The project would not build until the `apikey.properties` file was created and the API key was added.

There was also an issue with the RecyclerView ID. The activity layout used the ID `campgrounds`, so the MainActivity code had to use `binding.campgrounds`.

The app also crashed when opening the campground detail screen because the CampgroundImage objects were not serializable. This was fixed by making CampgroundImage implement `java.io.Serializable`.

After fixing these issues, the app successfully displayed campground data from the API and opened the correct detail screen when a campground was selected.

## License

Copyright 2026 Isaac Livingston

Licensed under the Apache License, Version 2.0.
