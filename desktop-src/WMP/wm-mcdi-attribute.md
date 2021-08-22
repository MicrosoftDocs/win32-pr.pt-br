---
title: Atributo WM/MCDI
description: O atributo WM/MCDI é o identificador do CD de música do CD do qual o arquivo ou o controle foi copiado.
ms.assetid: f0bec14d-416c-477f-98df-dece0bf85ea4
keywords:
- Windows Media Player do atributo WM/MCDI
topic_type:
- apiref
api_name:
- WM/MCDI
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 738ce8d5af7351b30fd986323db01d4dd335fa7307d2da88e48f4b2456eba1f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053844"
---
# <a name="wmmcdi-attribute"></a>Atributo WM/MCDI

O atributo **WM/MCDI** é o identificador do CD de música do CD do qual o arquivo ou o controle foi copiado.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Faixas de CD](cd-track-attributes.md)
-   [atributos de arquivo de mídia Windows usados com frequência](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado tanto na biblioteca (ou no cache) quanto no arquivo de mídia digital.

**TOC** é um alias para este atributo.

a constante do SDK do formato de mídia Windows para esse atributo é g \_ wszWMMCDI.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





