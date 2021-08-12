---
title: Atributo AverageLevel
description: O atributo AverageLevel é um valor de amplitude de 16 bits que indica o nível médio de volume.
ms.assetid: 04ff19f1-a9a5-4e47-86a6-50c6f08b0d7d
keywords:
- Windows Media Player de atributo AverageLevel
topic_type:
- apiref
api_name:
- AverageLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e169b1e2d63e6f8215515acc852d431ff13ccd513924e4c2a237b16c17dacfc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118582741"
---
# <a name="averagelevel-attribute"></a>Atributo AverageLevel

O atributo **AverageLevel** é um valor de amplitude de 16 bits que indica o nível médio de volume.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [arquivos de mídia Windows usados com frequência](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado tanto na biblioteca quanto no arquivo de mídia digital.

Windows Media Player define esse valor em uma das seguintes instâncias:

-   Depois de copiar um arquivo.
-   Depois de reproduzir um arquivo (quando o aprimoramento do nivelamento de volume automático estiver habilitado).

a constante do SDK do formato de mídia Windows para esse atributo é g \_ wszAverageLevel.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





