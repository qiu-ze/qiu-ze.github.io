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

**文件名: ModItems.java**
```java
public class ModItems {
    public static final DeferredRegister<Item> ITEMS = DeferredRegister.create(Registries.ITEM, BarrenWilderness.MODID);
    public static final Supplier<Item> STONECOIN = ITEMS.register("stonecoin",()-> new StoneCoinItem(new Item.Properties()));
    public static void register(IEventBus eventBus) {
        ITEMS.register(eventBus);
    }
}
```
后用Properties写了stonecoin的一个新方法  
```java
public class StoneCoinItem extends Item {
    public StoneCoinItem(Properties pProperties) {
        super(pProperties);
    }
}
```
