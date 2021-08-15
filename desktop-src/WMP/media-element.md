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
ms.openlocfilehash: c67f4321d85ec52babbc6f24c2cd9e3512f7c970eb3360ba2ddfd7ba53f82152
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996316"
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

o atributo **cid** (a ID de conteúdo) é preenchido pelo Windows Media Player como uma maneira de identificar exclusivamente um conteúdo de mídia, mesmo que seus atributos de metadados tenham sido alterados. isso permite o compartilhamento de listas de reprodução entre computadores, pois o conteúdo pode ser identificado em outro computador, e o caminho para ele pode ser "reparado automaticamente" pela lista de reprodução de mídia Windows. o atributo **tid** (a ID de rastreamento) usa o sistema de arquivos Windows para reparar automaticamente o caminho para a mídia se o nome ou o local do arquivo for alterado.

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

[**Windows Referência de elementos de playlist de mídia**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





