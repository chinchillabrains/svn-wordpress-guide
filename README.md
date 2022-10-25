# svn-wordpress-guide
This is a guide on using SVN (Subversion) for uploading/updating wordpress.org plugins

#### 1. Download repository (Check out)

```
svn co http://svn.wp-plugins.org/my-plugin-slug
```

#### 2. Create/update readme.txt
- Use the sample readme.txt from this repository.
- You can find readme.txt specs on [wordpress.org](https://developer.wordpress.org/plugins/wordpress-org/how-your-readme-txt-works/)

#### 3. Add your plugin code to trunk directory
#### 4. Add new files & new directories
```
svn add dirname
```
```
svn add filename
```
Or add everything
```
svn add *
```
#### 5. Push changes (Check in)
```
svn --username=myWordpressUsername ci -m "Commit message here"
```
#### 6. Tag plugin version
Run this command to create a new tag from the contents of the trunk directory.
```
svn --username=myWordpressUsername copy http://plugins.svn.wordpress.org/my-plugin-slug/trunk http://plugins.svn.wordpress.org/my-plugin-slug/tags/1.0.0 -m "version 1.0.0 tag"
```
