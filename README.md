# How-to-create-a-basic-router---php

What do you need


<php
class Route{
  private $uri = array();
  private $views = array();

  public function add($uri, $view=null) {
    $this->uri[] = trim($uri,"/");
    
    if($view != null) {
      $this->views[] = $view;
    }
  }

  public function on() {
    $got_uri = isset($_GET['uri']) ? $_GET['uri'] : '/';
    
  }
}


<?





## .htaccess file
RewriteEngine On
RewriteBase /mymainfolder/

RewriteCond %{REQUEST_FILENAME} !-f
RewriteCond %{REQUEST_FILENAME} !-d

RewriteRule ^(.+)$ index.php?uri=$1 [QSA,L]


