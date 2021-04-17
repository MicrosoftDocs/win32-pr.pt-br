---
title: Atributo WM/MCDI
description: O atributo WM/MCDI é o identificador do CD de música do CD do qual o arquivo ou o controle foi copiado.
ms.assetid: f0bec14d-416c-477f-98df-dece0bf85ea4
keywords:
- Atributo WM/MCDI do Windows Media Player
topic_type:
- apiref
api_name:
- WM/MCDI
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aec51c306f94e25acb94155c4d87f1f1a8b95866
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105773079"
---
# <a name="wmmcdi-attribute"></a>Atributo WM/MCDI

O atributo **WM/MCDI** é o identificador do CD de música do CD do qual o arquivo ou o controle foi copiado.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Faixas de CD](cd-track-attributes.md)
-   [Atributos de arquivo de mídia do Windows comumente usados](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado tanto na biblioteca (ou no cache) quanto no arquivo de mídia digital.

**TOC** é um alias para este atributo.

A constante do Windows Media Format SDK para esse atributo é g \_ wszWMMCDI.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





