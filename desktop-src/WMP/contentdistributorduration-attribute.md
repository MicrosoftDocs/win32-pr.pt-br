---
title: Atributo ContentDistributorDuration
description: O atributo ContentDistributorDuration é a duração da reprodução do item, em segundos.
ms.assetid: c64cb4ca-b0bc-4beb-b2ae-ddd0c5fcd35c
keywords:
- Atributo ContentDistributorDuration Windows Media Player
topic_type:
- apiref
api_name:
- ContentDistributorDuration
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9f17bad8ef5dd1ab4b0a3d1c7b5becec6fd34a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783620"
---
# <a name="contentdistributorduration-attribute"></a>Atributo ContentDistributorDuration

O atributo **ContentDistributorDuration** é a duração da reprodução do item, em segundos.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Outros itens](other-item-attributes.md)

## <a name="remarks"></a>Comentários

Se o atributo **Duration** regular não for definido (NULL) ou 0, o valor desse atributo será retornado em vez disso.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------|
| Versão<br/> | Windows Media Player 11<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> <dt>

[**Atributo Duration**](duration-attribute.md)
</dt> </dl>

 

 





