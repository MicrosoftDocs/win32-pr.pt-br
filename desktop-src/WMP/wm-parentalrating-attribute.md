---
title: Atributo WM/ParentalRating
description: O atributo WM/ParentalRating é a classificação pai do conteúdo.
ms.assetid: 9cbe5ae7-96b9-41f2-bdfd-8043f4cbd82d
keywords:
- Windows Media Player do atributo WM/ParentalRating
topic_type:
- apiref
api_name:
- WM/ParentalRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5808156e73620f775c2aa91feceaed4e06961f8e974c53a1595cdc739185062
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000876"
---
# <a name="wmparentalrating-attribute"></a>Atributo WM/ParentalRating

O atributo **WM/ParentalRating** é a classificação pai do conteúdo.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [atributos de arquivo de mídia Windows usados com frequência](commonly-used-windows-media-file-attributes.md)
-   [DVDs](dvd-attributes.md)
-   [Itens de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado tanto na biblioteca (ou no cache) quanto no arquivo de mídia digital.

a constante do SDK do formato de mídia Windows para esse atributo é g \_ wszWMParentalRating.

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

 

 





