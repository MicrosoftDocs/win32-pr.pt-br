---
title: Elemento querySet
description: O elemento querySet contém elementos que definem quais itens de mídia serão selecionados na biblioteca.
ms.assetid: 18b5a509-a56b-4fd1-812f-60b8efd5136b
keywords:
- Elemento querySet Windows Media Player
topic_type:
- apiref
api_name:
- querySet Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cb157bb30c2e728b7840fe7021a2a4fcacc317b10eb6778b5702d7d2277c4a92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118570609"
---
# <a name="queryset-element"></a>Elemento querySet

O **elemento querySet** contém elementos que definem quais itens de mídia serão selecionados na biblioteca.

``` syntax
<querySet>
</querySet>
```

## <a name="attributes"></a>Atributos

Esse elemento não tem atributos.

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia | Elementos                                   |
|-----------|--------------------------------------------|
| Pai    | [smartPlaylist](smartplaylist-element.md) |
| Filho     | [Sourcefilter](sourcefilter-element.md)   |



 

## <a name="remarks"></a>Comentários

O **elemento querySet** especifica quais itens de mídia devem ser selecionados na biblioteca, sem considerar o tamanho do conjunto de resultados. O **elemento** de filtro, por outro lado, limita o tamanho do conjunto de resultados.

## <a name="examples"></a>Exemplos


```
<querySet>
    <sourceFilter 
        type = "smartFilterObject" 
        id = "{4202947A-A563-4B05-A754-A1B4B5989849}"
        name = "Windows Media Local Music Library Filter">
            <fragment name = "Genre">
                <argument name = "Condition">Equals</argument>
                <argument name = "Value">Rock</argument>
            </fragment>
            <fragment name = "Artist">
                <argument name = "Condition">Does Not Equal</argument>
                <argument name = "Value">Brenda Diaz</argument>
            </fragment>
    </sourceFilter>
</querySet>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------|
| Versão<br/> | Windows Media Player série 9 ou posterior.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento argument**](argument-element.md)
</dt> <dt>

[**Elemento filter**](filter-element.md)
</dt> <dt>

[**Elemento fragment**](fragment-element.md)
</dt> <dt>

[**Elemento smartPlaylist**](smartplaylist-element.md)
</dt> <dt>

[**Elemento sourceFilter**](sourcefilter-element.md)
</dt> <dt>

[**Windows Referência de elementos da playlist de mídia**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





