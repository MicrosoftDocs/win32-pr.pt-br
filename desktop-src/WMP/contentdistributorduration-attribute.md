---
title: Atributo ContentDistributorDuration
description: O atributo ContentDistributorDuration é a duração da reprodução do item, em segundos.
ms.assetid: c64cb4ca-b0bc-4beb-b2ae-ddd0c5fcd35c
keywords:
- Windows Media Player de atributo ContentDistributorDuration
topic_type:
- apiref
api_name:
- ContentDistributorDuration
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eefee789358f2d913d976432a485cf7726e3f7d6afa14e845ad9d7699d8ed4a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135749"
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

 

 





