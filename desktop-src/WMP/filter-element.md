---
title: Elemento Filter
description: O elemento Filter contém elementos que limitam o tamanho de uma lista de reprodução, a duração de uma lista de reprodução ou o número de itens de mídia em uma lista de reprodução.
ms.assetid: 880885f6-493f-466b-b5ad-ab9b569f4cc5
keywords:
- Elemento Filter do Windows Media Player
topic_type:
- apiref
api_name:
- filter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 32d2d306faebef813996b59575220efeba99dfb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796414"
---
# <a name="filter-element"></a>Elemento Filter

O elemento **Filter** contém elementos que limitam o tamanho de uma lista de reprodução, a duração de uma lista de reprodução ou o número de itens de mídia em uma lista de reprodução.

``` syntax
<filter
    type = "string"
    id = "WPL_GUID"
    name = "string"
>
</filter>
            
```

## <a name="attributes"></a>Atributos

<dl> <dt>

<span id="type"></span><span id="TYPE"></span>**Escreva**
</dt> <dd>

O tipo de objeto de filtro. Não há valores predefinidos para este atributo.

</dd> <dt>

<span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>**ID** (obrigatório) 
</dt> <dd>

O GUID que identifica exclusivamente um objeto de filtro. Os métodos do objeto de filtro são invocados para interpretar os elementos de **fragmento** contidos no elemento de **filtro** .



| Valor                                  | Descrição                                                                                                 |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------|
| {BC5E21B0-504C-46F6-82BF-FB975C911AD6} | A ID do filtro "filtro de playlist automática da Microsoft--limita as listas de reprodução automática por contagem, tamanho ou duração". |



 

</dd> <dt>

<span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**nome** (obrigatório) 
</dt> <dd>

O nome do objeto de filtro.



| Valor                                                                              | Descrição                                        |
|------------------------------------------------------------------------------------|----------------------------------------------------|
| Filtro de playlist automática da Microsoft--limita as listas de reprodução automática por contagem, tamanho ou duração | Limita listas de reprodução automáticas por contagem, tamanho ou duração. |



 

</dd> </dl>

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia | Elementos                                   |
|-----------|--------------------------------------------|
| Pai    | [smartPlaylist](smartplaylist-element.md) |
| Filho     | [fragmento](fragment-element.md)           |



 

## <a name="remarks"></a>Comentários

O elemento **Filter** não adiciona nenhum elemento de mídia a uma lista de reprodução; Ele simplesmente remove ou filtra o conteúdo que foi selecionado pelo elemento **sourceFilter** .

## <a name="examples"></a>Exemplos


```XML
<filter 
    type = "smartFilterObject" 
    id = "{BC5E21B0-504C-46F6-82BF-FB975C911AD6}" 
    name = "Microsoft Auto Playlist Filter -- Limits auto playlists by count,size or duration">
        <fragment name = "Limit Number of Items">
            <argument name = "number">25</argument>
        </fragment>
</filter>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento Argument**](argument-element.md)
</dt> <dt>

[**Elemento Fragment**](fragment-element.md)
</dt> <dt>

[**Elemento smartPlaylist**](smartplaylist-element.md)
</dt> <dt>

[**Elemento sourceFilter**](sourcefilter-element.md)
</dt> <dt>

[**Referência de elementos da playlist do Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





