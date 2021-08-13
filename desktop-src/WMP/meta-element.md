---
title: Elemento meta
description: O elemento meta especifica os metadados que se aplicam à lista de reprodução inteira.
ms.assetid: 7248e1d9-ebd1-48cb-9019-89a35eac27ae
keywords:
- Windows Media Player meta de elemento
topic_type:
- apiref
api_name:
- meta Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b2e4120b3eceea6d2a664edec9b48a46d33ad19b788bb820458a8802dccd2d9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119415736"
---
# <a name="meta-element"></a>Elemento meta

O elemento **meta** especifica os metadados que se aplicam à lista de reprodução inteira.

``` syntax
<meta
    name = "string"
    content = "string"
/>
```

## <a name="attributes"></a>Atributos



| Termo                                                                       | Descrição                                                                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="name"></span><span id="NAME"></span>**nomes**<br/>          | O nome de um item de metadados.<br/>                                                                                       |
| <span id="content"></span><span id="CONTENT"></span>**disputa**<br/> | O valor de um item de metadados. Por exemplo, se o atributo name for "gênero", o atributo Content poderá ser "rock".<br/> |



 

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia | Elementos                 |
|-----------|--------------------------|
| Pai    | [principal](head-element.md) |
| Filho     | Nenhum                     |



 

## <a name="remarks"></a>Comentários

o criador de uma lista de reprodução de mídia Windows pode definir o atributo name de um elemento meta para qualquer cadeia de caracteres. a lista a seguir mostra alguns atributos de nome típicos que são encontrados em Windows listas de reprodução de mídia criadas pelo Windows Media Player e outros componentes da Microsoft.

-   Autor
-   Categoria
-   Gênero
-   UserName
-   UserRating
-   Gerador

## <a name="examples"></a>Exemplos


```
<head>
    <meta name = "Author" content = "Frank Lee"/>
    <meta name = "Category" content = "Classic"/>
    <meta name = "Genre" content = "Rock"/>
</head>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento head**](head-element.md)
</dt> <dt>

[**Windows Referência de elementos de playlist de mídia**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





