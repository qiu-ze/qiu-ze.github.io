---
layout: post
title: Testblog
date: 2024-5-21 23:00:00 +0800
last_modified_at: 2024-5-22 16:00:00 +0800
tags: [Minecraft]
toc:  true
---
使用ITEMS注册表注册一个新物品

**stonecoin**
<div class="highlight-tools">
  <i class="fas fa-angle-down expand">
  </i><div class="code-lang">JAVA</div>
  <div class="copy-notice"></div><i class="fas fa-paste copy-button">
  </i>
<em>
  
    public class ModItems {
        public static final DeferredRegister<Item> ITEMS = DeferredRegister.create(Registries.ITEM, BarrenWilderness.MODID);
        public static final Supplier<Item> STONECOIN = ITEMS.register("stonecoin",()-> new StoneCoinItem(new Item.Properties()));
        public static void register(IEventBus eventBus) {
            ITEMS.register(eventBus);
        }
    }
</em>
</div>
后用Properties写了**stonecoin**的一个新方法

<div class="highlight-tools">
  <i class="fas fa-angle-down expand">
  </i><div class="code-lang">JAVA</div>
  <div class="copy-notice"></div><i class="fas fa-paste copy-button">
  </i>
<em>
  
    public class StoneCoinItem extends Item {
        public StoneCoinItem(Properties pProperties) {
            super(pProperties);
        }
    }
</em>
</div>
