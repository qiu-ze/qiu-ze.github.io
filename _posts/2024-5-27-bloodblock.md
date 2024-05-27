---
layout: post
title: BloodBlock
date: 2024-5-27 16:00:00 +0800
last_modified_at: 2024-5-27 19:00:00 +0800
tags: [Minecraft]
toc:  true
---
**新版NeoForge同up^(￣(oo)￣)^的改动**

**把没用的use换成新的有用的方法useItemOn,并把返回值类型从InteractionResult改成ItemInteractionResult**

**多了一个ItemStack pStack**

```java
public @NotNull ItemInteractionResult useItemOn(@NotNull ItemStack pStack, @NotNull BlockState pState, Level pLevel, @NotNull BlockPos pPos, @NotNull Player pPlayer, @NotNull InteractionHand pHand, @NotNull BlockHitResult pHit) {

    if (!pLevel.isClientSide() && pHand == InteractionHand.MAIN_HAND) {
        pLevel.setBlock(pPos, pState.cycle(FIRE), 3);
    }

    return super.useItemOn(pStack,pState,pLevel,pPos,pPlayer,pHand,pHit);

    }
```
