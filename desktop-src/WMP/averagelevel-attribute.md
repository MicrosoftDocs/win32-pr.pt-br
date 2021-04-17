---
title: Atributo AverageLevel
description: O atributo AverageLevel é um valor de amplitude de 16 bits que indica o nível médio de volume.
ms.assetid: 04ff19f1-a9a5-4e47-86a6-50c6f08b0d7d
keywords:
- Atributo AverageLevel Windows Media Player
topic_type:
- apiref
api_name:
- AverageLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 594612f3675d818f94270b1952d2a9ca7bed15d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760897"
---
# <a name="averagelevel-attribute"></a>Atributo AverageLevel

O atributo **AverageLevel** é um valor de amplitude de 16 bits que indica o nível médio de volume.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Arquivos de mídia do Windows comumente usados](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado tanto na biblioteca quanto no arquivo de mídia digital.

O Windows Media Player define esse valor em uma das seguintes instâncias:

-   Depois de copiar um arquivo.
-   Depois de reproduzir um arquivo (quando o aprimoramento do nivelamento de volume automático estiver habilitado).

A constante do Windows Media Format SDK para esse atributo é g \_ wszAverageLevel.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





