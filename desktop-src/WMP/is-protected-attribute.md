---
title: Is_Protected atributo
description: O \_ atributo is Protected indica se o conteúdo é protegido usando o DRM (gerenciamento de direitos digitais).
ms.assetid: 049d4116-7ba6-49f5-ad54-82a98b79d6bc
keywords:
- Atributo Is_Protected Windows Media Player
topic_type:
- apiref
api_name:
- Is_Protected
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ba626e72e139a5373973edea581f0f8462eee32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788156"
---
# <a name="is_protected-attribute"></a>É \_ atributo protegido

O atributo **is \_ Protected** indica se o conteúdo é protegido usando o DRM (gerenciamento de direitos digitais).

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Arquivos de mídia do Windows comumente usados](commonly-used-windows-media-file-attributes.md)
-   [Itens de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado tanto na biblioteca quanto no arquivo de mídia digital.

**DigitallySecure** é um alias para este atributo.

A constante do Windows Media Format SDK para esse atributo é g \_ wszWMProtected.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





