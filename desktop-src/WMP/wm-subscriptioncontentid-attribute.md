---
title: Atributo WM/SubscriptionContentID
description: O atributo WM/SubscriptionContentID é o identificador de conteúdo da assinatura.
ms.assetid: ef0fe575-3cea-4442-950b-40c60378364b
keywords:
- Atributo WM/SubscriptionContentID do Windows Media Player
topic_type:
- apiref
api_name:
- WM/SubscriptionContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f10448686e299c20fc1cd44f716b805910e8f5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785164"
---
# <a name="wmsubscriptioncontentid-attribute"></a>Atributo WM/SubscriptionContentID

O atributo **WM/SubscriptionContentID** é o identificador de conteúdo da assinatura.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Atributos de arquivo de mídia do Windows comumente usados](commonly-used-windows-media-file-attributes.md)
-   [Itens de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado tanto na biblioteca quanto no arquivo de mídia digital.

**SubscriptionContentID** é um alias para este atributo.

A constante do Windows Media Format SDK para esse atributo é g \_ wszWMSubscriptionContentID.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





