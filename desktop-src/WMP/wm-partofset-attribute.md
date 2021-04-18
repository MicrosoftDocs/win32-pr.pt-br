---
title: Atributo WM/PartOfSet
description: O atributo WM/PartOfSet é o número da peça e o número total de partes do conjunto ao qual o item pertence.
ms.assetid: c6827c31-c625-4283-a50d-f08eccf87271
keywords:
- Atributo WM/PartOfSet do Windows Media Player
topic_type:
- apiref
api_name:
- WM/PartOfSet
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c27d6297931c503c95c8ef0462bf7b119a0ffb75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105791353"
---
# <a name="wmpartofset-attribute"></a>Atributo WM/PartOfSet

O atributo **WM/PartOfSet** é o número da peça e o número total de partes do conjunto ao qual o item pertence.

## <a name="applies-to"></a>Aplica-se A

-   [Arquivos de música](music-file-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado somente em um arquivo de música que não está na biblioteca do.

A constante do Windows Media Format SDK para esse atributo é g \_ wszWMPartOfSet.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





