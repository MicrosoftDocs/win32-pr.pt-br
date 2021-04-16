---
title: Elemento sourceFilter
description: O elemento sourceFilter contém elementos que selecionam itens de uma biblioteca.
ms.assetid: c961990f-8c57-448d-b4dc-dcfe70300e5a
keywords:
- Elemento sourceFilter do Windows Media Player
topic_type:
- apiref
api_name:
- sourceFilter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cb43a9577c5fe8857b63067db5be90d314037b84
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750186"
---
# <a name="sourcefilter-element"></a>Elemento sourceFilter

O elemento **sourceFilter** contém elementos que selecionam itens de uma biblioteca.

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

<span id="type"></span><span id="TYPE"></span>**Escreva**
</dt> <dd>

O tipo de objeto de filtro. Não há valores predefinidos para este atributo.

</dd> <dt>

<span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>**ID** (obrigatório) 
</dt> <dd>

O GUID que identifica exclusivamente o objeto de filtro de origem. Os métodos do objeto de filtro de origem são invocados para interpretar os elementos de **fragmento** contidos no elemento **sourceFilter** .



| Valor                                  | Descrição                                              |
|----------------------------------------|----------------------------------------------------------|
| {4202947A-A563-4B05-A754-A1B4B5989849} | O GUID do filtro de origem "música em minha biblioteca".    |
| {B2D9BDDC-8E49-444B-9BA4-193ABF9C7870} | O GUID do filtro de origem "vídeo em minha biblioteca".    |
| {CC823400-A8E4-4081-B073-D3B6D952FE69} | O GUID do filtro de origem "imagens em minha biblioteca". |
| {E5415A66-7763-4BDE-B97F-5557CA73C303} | O GUID do filtro de origem "programas de TV em minha biblioteca". |



 

</dd> <dt>

<span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**nome** (obrigatório) 
</dt> <dd>

O nome do objeto de filtro.



| Valor                  | Descrição                                                                                     |
|------------------------|-------------------------------------------------------------------------------------------------|
| Música na minha biblioteca    | Um objeto de filtro que seleciona itens especificados do conjunto de itens de música na biblioteca do usuário. |
| Vídeo na minha biblioteca    | Um objeto de filtro que seleciona itens especificados do conjunto de itens de vídeo na biblioteca do usuário. |
| Imagens na minha biblioteca | Um objeto de filtro que seleciona itens especificados do conjunto de itens de fotos na biblioteca do usuário. |
| Programas de TV em minha biblioteca | Um objeto de filtro que seleciona itens especificados do conjunto de itens de TV na biblioteca do usuário.    |



 

</dd> </dl>

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia | Elementos                         |
|-----------|----------------------------------|
| Pai    | [queryset](queryset-element.md) |
| Filho     | [fragmento](fragment-element.md) |



 

## <a name="remarks"></a>Comentários

O elemento **sourceFilter** seleciona itens da biblioteca sem considerar o tamanho do conjunto de resultados. O elemento **Filter** , por outro lado, limita o tamanho do conjunto de resultados.

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
| Versão<br/> | Windows Media Player 9 Series ou posterior.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento Filter**](filter-element.md)
</dt> <dt>

[**Elemento Fragment**](fragment-element.md)
</dt> <dt>

[**Elemento queryset**](queryset-element.md)
</dt> <dt>

[**Referência de elementos da playlist do Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





