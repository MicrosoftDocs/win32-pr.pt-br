---
title: Elemento de mídia
description: O elemento Media especifica um dos itens de mídia em uma lista de reprodução.
ms.assetid: 7329bf48-3b23-4bc6-8488-506efca284bb
keywords:
- Elemento de mídia Windows Media Player
topic_type:
- apiref
api_name:
- media Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e693c8b17345d3ba7875d48b83b5e3e90d682dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751396"
---
# <a name="media-element"></a>Elemento de mídia

O elemento **Media** especifica um dos itens de mídia em uma lista de reprodução.

``` syntax
<media
    src = "URL"
    cid = "WPL_GUID"
    tid = "WPL_GUID"
>
</media>
```

## <a name="attributes"></a>Atributos



| Termo                                                                                                                       | Descrição                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span id="src__required______________"></span><span id="SRC__REQUIRED______________"></span>**src** (obrigatório) <br/> | A URL de um item de mídia.<br/>                                                              |
| <span id="cid"></span><span id="CID"></span>**CID**<br/>                                                             | A ID de conteúdo que é exclusiva para este item de mídia.<br/>                                     |
| <span id="tid"></span><span id="TID"></span>**tid**<br/>                                                             | A ID de rastreamento que pode ser usada para rastrear o objeto do sistema de arquivos para este item de mídia.<br/> |



 

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia | Elementos               |
|-----------|------------------------|
| Pai    | [Seq](seq-element.md) |
| Filho     | Nenhum                   |



 

## <a name="remarks"></a>Comentários

O atributo **CID** (a ID de conteúdo) é preenchido pelo Windows Media Player como uma maneira de identificar exclusivamente um conteúdo de mídia, mesmo que seus atributos de metadados tenham sido alterados. Isso permite o compartilhamento de listas de reprodução entre computadores, pois o conteúdo pode ser identificado em outro computador e o caminho para ele pode ser "reparado automaticamente" pela lista de reprodução do Windows Media. O atributo **tid** (a ID de rastreamento) usa o sistema de arquivos do Windows para reparar automaticamente o caminho para a mídia se o nome ou o local do arquivo for alterado.

## <a name="examples"></a>Exemplos


```
<media
    src = "laure.wma"
    cid = "ABCDEFGH-abcd-1234-WXYZ-ABCDEF000000"
    tid = "12345678-1234-abcd-ABCD-123456abcDEF"
>
</media>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento seq**](seq-element.md)
</dt> <dt>

[**Referência de elementos da playlist do Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





