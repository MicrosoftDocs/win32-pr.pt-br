---
title: Elemento meta
description: O elemento meta especifica os metadados que se aplicam à lista de reprodução inteira.
ms.assetid: 7248e1d9-ebd1-48cb-9019-89a35eac27ae
keywords:
- Elemento meta do Windows Media Player
topic_type:
- apiref
api_name:
- meta Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9f3c41c25a0df0895c645c34f97495712b113ffc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749555"
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

O criador de uma playlist do Windows Media pode definir o atributo Name de um elemento meta para qualquer cadeia de caracteres. A lista a seguir mostra alguns atributos de nome típicos que são encontrados nas listas de reprodução do Windows Media criadas pelo Windows Media Player e outros componentes da Microsoft.

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

[**Referência de elementos da playlist do Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





