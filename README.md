# ZHA supported devices
This repository holds a list of all devices which are supported by the [ZHA][link-zha] component of [Home Assistant][link-ha].

## Contributing
Please create a yaml file in the format specified below, and create a pull request on this repository.

## Format
The device files should be placed in a yaml file `/devices/VENDOR/MODEL.yaml`.

Here is an example of how a file could look like:

```yaml
model: LED1545G12
domains:
  - light
description: white spectrum, dimmable light
picture_url: ikea_LED1545G12.png
link: https://www.ikea.com/us/en/catalog/products/70353343/
```

Explanation:

| key         | optional | description                                                                                                                                                                                                      |
|-------------|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| model       | no       | Model number of the device. You can find that in the datasheet. This is not "60W opal white", but a specific model number. Only use "60W opal white" model descriptors if you really can't find any model number |
| domains     | no       | Array of home assistant domains this device creates                                                                                                                                                              |
| sensors     | yes      | If this device has sensors, specify them in a list. E. g.: motion, contact, water                                                                                                                                |
| description | no       | A short description about what this devices does                                                                                                                                                                 |
| notes       | yes      | Additional information about this device. If you had to reset the device in a specific way, write it here                                                                                                        |
| picture_url | yes      | Pictures should be placed in `devices/pictures/DEVICE_PICTURE.png`. This has to be a 300x300px PNG file. Only add `DEVICE_PICTURE.png` here, do not add the full path.                                                                                                          |
| source      | yes      | If this information is from someone else, e. g. from a thread in the forum or on discord, please add a link to the conversation here                                                                             |
| link        | yes      | A link to the *vendors* product page. Do not put Amazon or AliExpress links here     

## How to view this data

Currently, we only collect the raw data about device support here. In the future, we can write a generator program that builds a markdown/html/... files to add them somewhere.


[link-zha]: https://www.home-assistant.io/components/zha/
[link-ha]: https://www.home-assistant.io/
