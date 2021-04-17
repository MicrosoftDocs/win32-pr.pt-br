---
title: Atributo Duration
description: O atributo Duration é a duração da reprodução do item, em segundos.
ms.assetid: 0a59a7b6-4536-4197-9f4a-1877ef42f828
keywords:
- Atributo Duration Windows Media Player
topic_type:
- apiref
api_name:
- Duration
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb50e57a58eb1a2343230fd91757de1aa09901ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780239"
---
# <a name="duration-attribute"></a>Atributo Duration

O atributo **Duration** é a duração da reprodução do item, em segundos.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Arquivos de mídia do Windows comumente usados](commonly-used-windows-media-file-attributes.md)
-   [Outros itens](other-item-attributes.md)
-   [Itens de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado tanto na biblioteca quanto no arquivo de mídia digital.

A constante do Windows Media Format SDK para esse atributo é g \_ wszWMDuration.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





