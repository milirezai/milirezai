```php
class milirezai
{

    private static $name ;
    private static $lastName;
    private static $aboutMe ;
    private static $role ;
    private static $currentFocus ;
    private static $languages = []; 
    private static $backEnd = [];
    private static $frontEnd = []; 
    private static $database = []; 
    private static $versionControlSystems = [];


    public static function setPersonalInformation($name, $lastName, $aboutMe, $role, $currentFocus)
    {
        self::$name = $name;
        self::$lastName = $lastName;
        self::$aboutMe = $aboutMe;
        self::$role = $role;
        self::$currentFocus = $currentFocus;
    }

    public static function backEnd(array $languages, array $levelOfExpertise, array $frameworks, array $architecture)
    {
        self::$languages['backEnd'] = $languages;
        self::$backEnd= ["languages" => $languages,"levelOfExpertise" => $levelOfExpertise, "frameworks" =>$frameworks , "architecture" => $architecture];
    }
    public static function frontEnd(array $languages, array $levelOfExpertise, array $frameworks, array $architecture)
    {
        self::$languages['frontEnd'] = $languages;
        self::$frontEnd= ["languages" => $languages,"levelOfExpertise" => $levelOfExpertise, "frameworks" =>$frameworks , "architecture" => $architecture];
    }
    public static function database($database, $languages, $levelOfExpertise, array $architecture)
    {
        self::$languages['database'] = $languages;
        self::$database= ["database" => $database ,"languages" => $languages,"levelOfExpertise" => $levelOfExpertise,"architecture" => $architecture];
    }
    public static function versionControlSystems(array $versionControlSystems)
    {
        self::$versionControlSystems = $versionControlSystems;
    }

    public static function get()
    {
        return
        [
            "personalInformation" =>
                [
                    "name" => self::$name,
                    "lastName" => self::$lastName,
                    "aboutMe" => self::$aboutMe,
                    "role" => self::$role,
                    "currentFocus" => self::$currentFocus,
                ],
                "languages" => self::$languages,
             "technologies" =>
               [
                   "backend" => self::$backEnd,
                   "frontEnd" => self::$frontEnd,
                   "database" => self::$database,
               ],
            "versionControlSystems" => self::$versionControlSystems,
        ];
    }

}

$personalInformation=milirezai::setPersonalInformation("milad", "rezai", "junyore php developer", "php developer", "lerning");
$backend=milirezai::backEnd(["php"],["php" => "75%"],["laravel","damavand"],["mvc"]);
$frontEnd=milirezai::frontEnd(["html","css","js"],["html" => "70%","css" => "60%","js" => "45%"],[],[]);
$database=milirezai::database(["mysql"],["sql"],["sql" => "60%"],["Relational"]);
$versionControlSystems=milirezai::versionControlSystems(["git"]);
$get=milirezai::get();
print_r($get);
```
<div align="center">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/laravel/laravel-original.svg" width="52" height="40" alt="gmail logo" />
  <img/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" width="52" height="40" alt="gmail logo"/>
  <img/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg" width="52" height="40" alt="gmail logo"/>
  <img />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg" width="52" height="40" alt="gmail logo"/>
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" width="52" height="40" alt="gmail logo"/>
  <img/>
    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/99/Unofficial_JavaScript_logo_2.svg/800px-Unofficial_JavaScript_logo_2.svg.png" width="52" height="40" alt="gmail logo" />
  <img/>
   <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/php/php-original.svg" width="50" height="50" alt="gmail logo"/>
 </div>
 <div align="center">
