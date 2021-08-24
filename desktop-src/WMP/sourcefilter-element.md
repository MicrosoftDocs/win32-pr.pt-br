---
title: Elemento sourceFilter
description: O elemento sourceFilter contém elementos que selecionam itens de uma biblioteca.
ms.assetid: c961990f-8c57-448d-b4dc-dcfe70300e5a
keywords:
- Elemento sourceFilter Windows Media Player
topic_type:
- apiref
api_name:
- sourceFilter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 14294f227e5ebe29e422d60a95734f7b93207880ea82ef9fb70ed3f7cf6dac4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763266"
---
# <a name="sourcefilter-element"></a>Elemento sourceFilter

O **elemento sourceFilter** contém elementos que selecionam itens de uma biblioteca.

``` syntax
<sourceFilter
    type = "string"
    id = "WPL_GUID"
    name = "string"
>
</sourceFilter>
```

## <a name="attributes"></a>Atributos

<dl> <dt>

<span id="type"></span><span id="TYPE"></span>**Tipo**
</dt> <dd>

O tipo de objeto de filtro. Não há valores predefinidos para esse atributo.

</dd> <dt>

<span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>**id** (obrigatório) 
</dt> <dd>

O GUID que identifica exclusivamente o objeto de filtro de origem. Os métodos do objeto de filtro de origem são invocados para interpretar os elementos **de fragmento** contidos no **elemento sourceFilter.**



| Valor                                  | Descrição                                              |
|----------------------------------------|----------------------------------------------------------|
| {4202947A-A563-4B05-A754-A1B4B5989849} | O GUID do filtro de origem "Música na minha biblioteca".    |
| {B2D9BDDC-8E49-444B-9BA4-193ABF9C7870} | O GUID do filtro de origem "Vídeo na minha biblioteca".    |
| {CC823400-A8E4-4081-B073-D3B6D952FE69} | O GUID do filtro de origem "Imagens na minha biblioteca". |
| {E5415A66-7763-4BDE-B97F-5557CA73C303} | O GUID do filtro de origem "TV mostra em minha biblioteca". |



 

</dd> <dt>

<span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**name** (obrigatório) 
</dt> <dd>

O nome do objeto de filtro.



| Valor                  | Descrição                                                                                     |
|------------------------|-------------------------------------------------------------------------------------------------|
| Música em minha biblioteca    | Um objeto de filtro que seleciona itens especificados do conjunto de itens de música na biblioteca do usuário. |
| Vídeo em minha biblioteca    | Um objeto de filtro que seleciona itens especificados do conjunto de itens de vídeo na biblioteca do usuário. |
| Imagens em minha biblioteca | Um objeto de filtro que seleciona itens especificados do conjunto de itens de foto na biblioteca do usuário. |
| Programas de TV na minha biblioteca | Um objeto de filtro que seleciona itens especificados do conjunto de itens de TV na biblioteca do usuário.    |



 

</dd> </dl>

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia | Elementos                         |
|-----------|----------------------------------|
| Pai    | [querySet](queryset-element.md) |
| Filho     | [Fragmento](fragment-element.md) |



 

## <a name="remarks"></a>Comentários

O **elemento sourceFilter** seleciona itens da biblioteca sem considerar o tamanho do conjunto de resultados. O **elemento** de filtro, por outro lado, limita o tamanho do conjunto de resultados.

## <a name="examples"></a>Exemplos


```
<sourceFilter 
    type = "smartFilterObject" 
    id = "{4202947A-A563-4B05-A754-A1B4B5989849}" 
    name = "Music in my library">
        <fragment name = "Genre">
            <argument name = "condition">Is</argument>
            <argument name = "value">Rock</argument>
        </fragment>
        <fragment name = "Album Artist">
            <argument name = "condition">Is Not</argument>
            <argument name = "value">Brenda Diaz</argument>
        </fragment>
</sourceFilter>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------|
| Versão<br/> | Windows Media Player Série 9 ou posterior.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento filter**](filter-element.md)
</dt> <dt>

[**Elemento fragment**](fragment-element.md)
</dt> <dt>

[**Elemento querySet**](queryset-element.md)
</dt> <dt>

[**Windows Referência de elementos da playlist de mídia**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





