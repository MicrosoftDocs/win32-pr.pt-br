---
title: Atributo de picovalue
description: O atributo de Picovalue é um valor de amplitude de 16 bits que indica o nível de volume de pico.
ms.assetid: 5d80a1f3-015c-4740-bd1c-f3bbf88a9df2
keywords:
- Atributo de picovalue Windows Media Player
topic_type:
- apiref
api_name:
- PeakValue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74fde522e043adb8b11c25bede763bed6b252f2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763833"
---
# <a name="peakvalue-attribute"></a>Atributo de picovalue

O atributo de **picovalue** é um valor de amplitude de 16 bits que indica o nível de volume de pico.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Arquivos de mídia do Windows comumente usados](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado tanto na biblioteca quanto no arquivo de mídia digital.

O Windows Media Player define esse valor em uma das seguintes instâncias:

-   Depois de copiar um arquivo.
-   Depois de reproduzir um arquivo (quando o aprimoramento do nivelamento de volume automático estiver habilitado).

A constante do Windows Media Format SDK para esse atributo é g \_ wszPeakValue.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





