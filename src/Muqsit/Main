<?php
namespace Muqsit;

use pocketmine\utils\Config;
use pocketmine\plugin\PluginBase;
use pocketmine\event\Listener;

class Main extends PluginBase implements Listener{

  public function onEnable(){
    $this->saveDefaultConfig();
    $this->reloadConfig();
    $this->getServer()->getPluginManager()->registerEvents($this, $this);
  }
  
  public function onJoin(PlayerJoinEvent $e){
    $p = $e->getPlayer();
    $cfg = $this->getConfig();
    $x = $cfg->getAll();
    if($cfg->get($x) > 1500000){
      $cfg->setNested($x, 1500000)
    }
  }
}
