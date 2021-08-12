---
title: Elemento filter
description: O elemento filter contém elementos que limitam o tamanho de uma playlist, a duração de uma playlist ou o número de itens de mídia em uma playlist.
ms.assetid: 880885f6-493f-466b-b5ad-ab9b569f4cc5
keywords:
- Elemento filter Windows Media Player
topic_type:
- apiref
api_name:
- filter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8a059a6a2820d99541076775ac869de0767ffd739743f5b145a155efd0a25abc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118576773"
---
# <a name="filter-element"></a>Elemento filter

O **elemento filter** contém elementos que limitam o tamanho de uma playlist, a duração de uma playlist ou o número de itens de mídia em uma playlist.

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

<span id="type"></span><span id="TYPE"></span>**Tipo**
</dt> <dd>

O tipo de objeto de filtro. Não há valores predefinidos para esse atributo.

</dd> <dt>

<span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>**id** (obrigatório) 
</dt> <dd>

O GUID que identifica exclusivamente um objeto de filtro. Os métodos do objeto de filtro são invocados para interpretar os **elementos de fragmento** contidos no elemento **de** filtro.



| Valor                                  | Descrição                                                                                                 |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------|
| {BC5E21B0-504C-46F6-82BF-FB975C911AD6} | A ID do filtro "Filtro de Playlist Automática da Microsoft – Limita as listas de reprodução automáticas por contagem, tamanho ou duração". |



 

</dd> <dt>

<span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**name** (obrigatório) 
</dt> <dd>

O nome do objeto de filtro.



| Valor                                                                              | Descrição                                        |
|------------------------------------------------------------------------------------|----------------------------------------------------|
| Filtro de Playlist Automática da Microsoft – limita listas de reprodução automáticas por contagem, tamanho ou duração | Limita as listas de reprodução automáticas por contagem, tamanho ou duração. |



 

</dd> </dl>

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia | Elementos                                   |
|-----------|--------------------------------------------|
| Pai    | [smartPlaylist](smartplaylist-element.md) |
| Filho     | [Fragmento](fragment-element.md)           |



 

## <a name="remarks"></a>Comentários

O **elemento filter** não adiciona nenhum elemento de mídia a uma playlist; ele simplesmente remove ou filtra o conteúdo selecionado pelo **elemento sourceFilter.**

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
| Versão<br/> | Windows Media Player série 9 ou posterior.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento argument**](argument-element.md)
</dt> <dt>

[**Elemento fragment**](fragment-element.md)
</dt> <dt>

[**Elemento smartPlaylist**](smartplaylist-element.md)
</dt> <dt>

[**Elemento sourceFilter**](sourcefilter-element.md)
</dt> <dt>

[**Windows Referência de elementos da playlist de mídia**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





