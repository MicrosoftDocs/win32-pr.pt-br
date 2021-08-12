---
title: Atributo PeakValue
description: O atributo PeakValue é um valor de amplitude de 16 bits que indica o nível de volume de pico.
ms.assetid: 5d80a1f3-015c-4740-bd1c-f3bbf88a9df2
keywords:
- Atributo PeakValue Windows Media Player
topic_type:
- apiref
api_name:
- PeakValue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5aa2a661342b305155717f4f11336f540e1ae53524ff2d303a2ab790e2c73af7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118573580"
---
# <a name="peakvalue-attribute"></a>Atributo PeakValue

O **atributo PeakValue** é um valor de amplitude de 16 bits que indica o nível de volume de pico.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Arquivos de mídia Windows comumente usados](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado na biblioteca e no arquivo de mídia digital.

Windows Media Player define esse valor em qualquer uma das seguintes instâncias:

-   Depois que ele tiver roubado um arquivo.
-   Depois que ele tiver tocado um arquivo (quando a melhoria de nivelamento automático de volume estiver habilitada).

A Windows constante do SDK de Formato de Mídia para esse atributo é g \_ wszPeakValue.

Para determinar se você pode alterar o valor desse atributo, use o [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player série 9 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





