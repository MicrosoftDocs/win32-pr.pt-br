---
title: Elemento queryset
description: O elemento queryset contém elementos que definem quais itens de mídia serão selecionados da biblioteca.
ms.assetid: 18b5a509-a56b-4fd1-812f-60b8efd5136b
keywords:
- Elemento queryset Windows Media Player
topic_type:
- apiref
api_name:
- querySet Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4971c2a7f601132640d7654a95dd288f1740a467
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765721"
---
# <a name="queryset-element"></a>Elemento queryset

O elemento **queryset** contém elementos que definem quais itens de mídia serão selecionados da biblioteca.

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
| Filho     | [sourceFilter](sourcefilter-element.md)   |



 

## <a name="remarks"></a>Comentários

O elemento **queryset** especifica quais itens de mídia devem ser selecionados da biblioteca, sem considerar o tamanho do conjunto de resultados. O elemento **Filter** , por outro lado, limita o tamanho do conjunto de resultados.

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
| Versão<br/> | Windows Media Player 9 Series ou posterior.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento Argument**](argument-element.md)
</dt> <dt>

[**Elemento Filter**](filter-element.md)
</dt> <dt>

[**Elemento Fragment**](fragment-element.md)
</dt> <dt>

[**Elemento smartPlaylist**](smartplaylist-element.md)
</dt> <dt>

[**Elemento sourceFilter**](sourcefilter-element.md)
</dt> <dt>

[**Referência de elementos da playlist do Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





