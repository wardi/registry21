## Quick start

1. Clone this repository and submodules

   ```bash
   git clone --recursive https://github.com/open-data/registry23.git
   ```

2. Download the wet-boew intranet theme, and extract into `public/static/gcweb`

   ```bash
   cd registry21/ckanext-wet-boew/ckanext/wet_boew/public/dist/

   wget https://github.com/wet-boew/wet-boew-dist/archive/v3.1.7.zip
   unzip v3.1.7.zip wet-boew-dist-3.1.7/dist/*
   mv wet-boew-dist-3.1.7/dist/* .
   rm -r v3.1.7.zip wet-boew-dist-3.1.7/

   mkdir -p js/jquerymobile/
   wget http://code.jquery.com/mobile/1.3.0/jquery.mobile-1.3.0.js \
       -O js/jquerymobile/jquery.mobile-1.3.0.js
   ```

3. Install with [datacats](https://github.com/boxkite/datacats)
   and `datacats init`

   Use the latest master release from github instead of the one on pypi
   if you need HTTP proxy support

   **or**
   
   Install each python package and its dependencies into your python virtualenv
   
   Use `development.ini` as a template configuration file and fill in the missing solr
   and postgres configuration.
