# c3ev3e Theme for Grav
based on ceevee theme, but strongly modified.

![Ceevee](assets/readme_1.png)

dagobit ported the Template to Bootstrap Grid and enhanced the skills section to a two column view.
For the Work Section we added the support of unsorted lists embedded as infos tree node in the yaml.
We also added a "blank" Layout for serving additional pages due law reasons like data privacy or imprint.
We hope you enjoy the work and refer in the rest to the original README content.

Based on the original [Ceevee](http://www.styleshout.com/free-templates/ceevee/) which is a clean, modern, fully responsive site template for your resume and portfolio. With this template, you can easily introduce yourself and showcase your works to future clients and employers. Also, it is flexible and easy to customize so you even use this template as a creative, business or portfolio site for your company.

# Features:

* HTML5 and CSS3
* Fully Responsive
* Clean and modern design
* Various templates for presenting your content
* Fontawesome icon font
* @font-face custom web fonts
* jQuery enhanced
* Flexslider
* Magnific popup lightbox
* Smooth scrolling effect
* Cross browser compatible
* Twitter integration

# Features New:
* Boostrap CSS 4 Grid
* Blank layout for privacy or imprint pages
* Two Column Skills Section with bootsrap progress bar
* Added infos tree node for past work
* Fixed some vars in the template only writing surrounding tag if var is really given

# Installation

Installing the c3ev3e theme can be done in one of two ways. Our GPM (Grav Package Manager) installation method enables you to quickly and easily install the theme with a simple terminal command, while the manual method enables you to do so via a zip file.

The theme by itself is useful, but you may have an easier time getting up and running by installing a skeleton. The [Ceevee Site Skeleton](https://github.com/getgrav/grav-skeleton-ceevee-site) is a self-contained repository for a complete sites which includes: sample content, configuration, theme, and plugins.

## GPM Installation (Preferred)

The simplest way to install this theme is via the [Grav Package Manager (GPM)](http://learn.getgrav.org/advanced/grav-gpm) through your system's Terminal (also called the command line).  From the root of your Grav install type:

    bin/gpm install c3ev3e # just working if we get listed with it soon

This will install the c3ev3e theme into your `/user/themes` directory within Grav. Its files can be found under `/your/site/grav/user/themes/c3ev3e`.

## Manual Installation

To install this theme, just download the zip version of this repository and unzip it under `/your/site/grav/user/themes`. Then, rename the folder to `c3ev3e`. You can find these files either on [GitHub](https://github.com/dagobit/grav-theme-c3ev3e) 

You should now have all the theme files under

    /your/site/grav/user/themes/c3ev3e

>> NOTE: This theme is a modular component for Grav which requires the [Grav](http://github.com/getgrav/grav), [Error](https://github.com/getgrav/grav-theme-error) and [Problems](https://github.com/getgrav/grav-plugin-problems) plugins.

# Updating

As development for the c3ev3e theme continues, new versions may become available that add additional features and functionality, improve compatibility with newer Grav releases, and generally provide a better user experience. Updating c3ev3e is easy, and can be done through Grav's GPM system, as well as manually.

## GPM Update (Preferred)

The simplest way to update this theme is via the [Grav Package Manager (GPM)](http://learn.getgrav.org/advanced/grav-gpm). You can do this with this by navigating to the root directory of your Grav install using your system's Terminal (also called command line) and typing the following:

    bin/gpm update c3ev3e # only if we get listed

This command will check your Grav install to see if your c3ev3e theme is due for an update. If a newer release is found, you will be asked whether or not you wish to update. To continue, type `y` and hit enter. The theme will automatically update and clear Grav's cache.

## Manual Update

Manually updating Ceevee is pretty simple. Here is what you will need to do to get this done:

* Delete the `your/site/user/themes/c3ev3e` directory.
* Download the new version of the Ceevee theme from either [GitHub](https://github.com/dagobit/grav-theme-c3ev3e)
* Unzip the zip file in `your/site/user/themes` and rename the resulting folder to `c3ev3e`.
* Clear the Grav cache. The simplest way to do this is by going to the root Grav directory in terminal and typing `bin/grav clear-cache`.

> Note: Any changes you have made to any of the files listed under this directory will also be removed and replaced by the new set. Any files located elsewhere (for example a YAML settings file placed in `user/config/themes`) will remain intact.

# Setup

If you want to set c3ev3e as the default theme, you can do so by following these steps:

* Navigate to `/your/site/grav/user/config`.
* Open the **system.yaml** file.
* Change the `theme:` setting to `theme: c3ev3e`.
* Save your changes.
* Clear the Grav cache. The simplest way to do this is by going to the root Grav directory in Terminal and typing `bin/grav clear-cache`.

Once this is done, you should be able to see the new theme on the frontend. Keep in mind any customizations made to the previous theme will not be reflected as all of the theme and templating information is now being pulled from the **c3ev3e** folder.


# Configuration
Configuration of c3ev3e theme consist of two parts:
* configuration file (from [skeleton](https://github.com/getgrav/grav-skeleton-ceevee-site/commits?author=hexplor)): "user/config/site.yaml"
* header variables (inside markdown files)

In configuration file you can set basic values for header, footer and general.
In markdown files, you can manage page content and overall look of the separate section. For example, below is a portfolio.md header section:

```markdown
portfolio:
  - title: "Creative Minds"
    img: portfolio-01.jpg
    img_text: View More
    img_url: "#"
    content: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc ultricies nulla non metus pulvinar imperdiet. Praesent non adipiscing libero."
```

In above example you can specify title, image, roll over text, url and content for each separate portfolio element.

Rest of the sections is made in similar approach. Remember to preserve original indentation to avoid issues.

## Configuration Example for resumee enhancements made by dagobit
Here we add the subtitle, the infos List and the skills were extended with a details variable.
### resume
```markdown

title: Resume
sections:
- title: Freelancer
- subtitle: Small approach of my Journe as rentable Guy
  css_class: work
  items:
    - title: Master of Disaster and beyond
      info: could be the location or Company I worked
      date: Year or detailed infos
      description: Some long text, complete sentences or just a small teaser for my work could belong here.
      infos: 
        - Further Bullet Points
        - Of things I did
        - or I did not


....


- title: Skills
  subtitle: Some skills I learned the Hardway
  css_class: skill
  items:
    - title: Development and DevOps
      info:
      date:
      description: Let's talk about what I can do or not.
      skills:
        - name: AWS
          details: (S3, EC2, RDS etc.)
          level: 85
        - name: DevOps
          details: (like DevSecOps, CI / CD etc.)
          level: 80
```

