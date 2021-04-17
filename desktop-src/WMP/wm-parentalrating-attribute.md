---
title: Atributo WM/ParentalRating
description: O atributo WM/ParentalRating é a classificação pai do conteúdo.
ms.assetid: 9cbe5ae7-96b9-41f2-bdfd-8043f4cbd82d
keywords:
- Atributo WM/ParentalRating do Windows Media Player
topic_type:
- apiref
api_name:
- WM/ParentalRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d4da78c6c8af5dbff3e283a784f0c1f583e093c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787444"
---
# <a name="wmparentalrating-attribute"></a>Atributo WM/ParentalRating

O atributo **WM/ParentalRating** é a classificação pai do conteúdo.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Atributos de arquivo de mídia do Windows comumente usados](commonly-used-windows-media-file-attributes.md)
-   [DVDs](dvd-attributes.md)
-   [Itens de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado tanto na biblioteca (ou no cache) quanto no arquivo de mídia digital.

A constante do Windows Media Format SDK para esse atributo é g \_ wszWMParentalRating.

**MPAARating** é um alias para este atributo.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





