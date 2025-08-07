# Content Starter Pack README

If you are reading this in a repository that you have cloned from the content-starter-pack template, then you can delete this README file after you've read it and no longer need it.

The content-starter-pack repository is a starting point for new content created it LeGIT. It has sample material and the basic structure of a set of skills that would make up a course or e-learning module.

There are several directories at the root of this repository that are explained below.

## The Front-Back-Matter directory

__DO NOT DELETE THE FRONT-BACK-MATTER DIRECTORY, OR ANY FILES IN IT.__

The ``front-back-matter`` directory has several standard files that are used for generating print lab manuals (or PDFs). These documents are usually included at the beginning or the end of a printed document and have legal information, contact info or user information for all lab documents. If you are building a full lab manual, make sure that you include the front and back matter in the same was as shown in [build.yaml](build.yaml).

These documents refer to images in the style-rau-base CSS theme, so make sure that you have [cloned the latest theme submodule](https://github.com/RAU-EIT/rau-start-here/blob/main/docs/user-guide/update-style.md).

## The Samples directory

The samples directory provides resources for SMEs developing new content in LeGIT. Use them as a reference; feel free to copy content from these folders into your course / skill specific folders at the root of your repository.

Later on, when you have built some of your own material, you can remove the ``samples`` directory from your repository. It is not intended to be part of your work. If you do use images or markdown sample files, make sure to copy those into your own course directory (and change any references to images, etc).

In the ``samples`` directory, you can find three main directories:

- _template-files
- skills
- courses

These directories all have different reference material, but are all useful to demonstrate how to write markdown and configure document builds within LeGIT.

### The samples/_template-files directory

The ___template-files__ directory contains reference markdown files for the formats that LeGIT can publish.

- __general-setup.md__, an accessory document to a lab manual that tells instructors how to set up a lab, or what students need to work with the lab equipment
- __lab-lesson.md__, a single section of a full lab manual
- __presentation-basic.md__, a sample presentation markdown file with minimal style on the slides
- __presentation-customer.md__, a presentation markdown file with a cover made specifically for Rockwell Automation customer training
- __presentation-distributor.md__, a presentation markdown file with a cover made specifically for distributor events like Distributor Technical Training (DTT)
- __scorm-quiz.md__, a markdown file that provides an interactive quiz for e-learning content
- __scorm-section.md__, a markdown file that demonstrates interactive objects like flip cards and image hotspots for e-learning content

Each of these markdown files may refer to images that are in the ``media`` folder in the same directory. If you copy any files from here and want to use the images that were referenced in the markdown, you'll need to copy the images out of the media folder as well.

### The samples/skills directory

The __skills__ directory contains all of the markdown and media files that teach a single skill.

In the new (circa 2023) RAU content development model, we develop content at the skill level. From a hierarchy standpoint, skills are the smallest unit of training; a skill is essentially a single, standalone piece of knowledge. A skill should be able to exist on its own, i.e. be presented by itself (for example as a single E-Learning module) and convey a meaningful outcome for the learner.

When developing skills, it's important to develop all of the pieces of content that you need for that skill. At a minimum there should be a presentation, e-learning section and lab procedure for each skill.

Here's an example of the learning content hierarchy for instructor led training courses:

__Skill(s) > Lesson(s) > Course__

For E-Learning, this might be a little different:

__Skill(s) > Module(s)__

### The samples/courses directory

The __courses__ directory contains course specific content outside of the individual skills that make up a course. This usually is something like a cover page for a lab manual, or specific material that is exclusive to a single course like a setup guide or boardwork that spans multiple skills.

## The style-rau-base directory

This directory contains the standard styles that RAU uses to make the content we create look presentable. 

Assuming you've [cloned the latest style submodule](https://github.com/RAU-EIT/rau-start-here/blob/main/docs/user-guide/dry-run.md#clone-the-current-document-styles), this directory and all files inside should not be deleted or modified.

## The output directory

This directory will not be created until you do a build based on the configuration within build.yaml. Files that are created go to the output directory. The output directory is ignored for git commits in order to save space.
