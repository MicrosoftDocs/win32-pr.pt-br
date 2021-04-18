---
title: Atributo WM/TrackNumber
description: O atributo WM/TrackNumber é o número de faixa do item no álbum no qual ele foi originalmente lançado.
ms.assetid: d1fc5bac-c440-470f-be5c-5aca74aee99e
keywords:
- Atributo WM/TrackNumber do Windows Media Player
topic_type:
- apiref
api_name:
- WM/TrackNumber
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecd9adf3a939a5087ee270e8bef4d4d510b678ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788149"
---
# <a name="wmtracknumber-attribute"></a>Atributo WM/TrackNumber

O atributo **WM/TrackNumber** é o número de faixa do item no álbum no qual ele foi originalmente lançado.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Atributos de arquivo de mídia do Windows comumente usados](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado tanto na biblioteca quanto no arquivo de mídia digital.

Faixas de números para um álbum começam em 1.

**OriginalIndex** e **OriginalIndexLeft** são aliases para este atributo.

A constante do Windows Media Format SDK para esse atributo é g \_ wszWMTrackNumber.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





