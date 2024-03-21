# myomnia-theme
======================================

This theme is created to override the django side pages of openedx.


Installation
------------

Clone this repository into the themes directory of your Open edX instance:
```
cd $(tutor config printroot)/env/build/openedx/themes/  
git clone https://github.com/PrevidenceUT/myomnia-theme.git
``` 


Customization
-------------

Create an html file with similar directory as it's in edx-platform.  
For example to customise the footer in LMS, create 'footer.html' inside lms/templates/
Now make your customisation here


Activate Theme
-------------

First You should re-build the openedx docker image, as per the [Tutor documentation on theming](https://docs.tutor.edly.io/configuration.html#adding-custom-themes):
```
tutor images build openedx
```

Then, restart your platform:  
```
tutor local stop && tutor local start
```

To activate your themes, head over to the administration panel at http://{lms_host}/admin/theming/sitetheme/

    If there are no existing themes then 
    1. Click the “Add site theme” button to create a theme.
    2. Here select site for which you want to set the theme.
    3. Enter name of the theme in "Theme dir name". Here the name of the theme is "myomnia-theme".

    Complete steps 1, 2 & 3 for lms and studio both.
