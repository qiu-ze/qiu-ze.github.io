Hello World
使用ITEMs注册表注册一个新物品**stonecoin**
<code>
public class ModItems {
    public static final DeferredRegister<Item> ITEMS = DeferredRegister.create(Registries.ITEM, BarrenWilderness.MODID);

    public static final Supplier<Item> STONECOIN = ITEMS.register("stonecoin",()-> new StoneCoinItem(new Item.Properties()));

    public static void register(IEventBus eventBus) {
        ITEMS.register(eventBus);
    }
}
</code>
后用Properties写了**stonecoin**的一个新方法
<code>
public class StoneCoinItem extends Item {
    public StoneCoinItem(Properties pProperties) {
        super(pProperties);
    }
}
</code>
