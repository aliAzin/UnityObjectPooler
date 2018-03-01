# UnityObjectPooler
## Simple object pool for Unity

Lightweight solution that you can just immediately throw objects at to be pooled. There is no need to pre-define pools (although you can if you want).

###### Instantiating objects 
(taking them from the pool):
```
var obj = ObjectPooler.Instance.Spawn(prefab, position, rotation);
```

###### Destroying objects 
(adding them back into the pool):
```
ObjectPooler.Instance.Despawn(gameObject);   
```

###### Preparing objects for re-use. 
```
public class Enemy : MonoBehaviour, IPoolable
{
    public void Spawn()
    {
        // do stuff...
    }

    public void Despawn()
    {
        // do stuff...
    }
}
```