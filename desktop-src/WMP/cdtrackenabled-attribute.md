---
title: Atributo CDTrackEnabled
description: O atributo CDTrackEnabled indica se a faixa está habilitada para reprodução.
ms.assetid: ebbc42bd-2d6c-47ae-9a3f-c6256b120d35
keywords:
- Atributo CDTrackEnabled Windows Media Player
topic_type:
- apiref
api_name:
- CDTrackEnabled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c81c231dbdfc432ea7aa510a19b1f85e0826c836
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813373"
---
# <a name="cdtrackenabled-attribute"></a>Atributo CDTrackEnabled

O atributo **CDTrackEnabled** indica se a faixa está habilitada para reprodução.

## <a name="applies-to"></a>Aplica-se A

-   [Faixas de CD](cd-track-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado somente no cache da biblioteca.

Ao reproduzir um CD no Windows Media Player, o usuário pode selecionar uma faixa e especificar que ela não deve ser reproduzida. Esse valor desse atributo será true se a faixa puder ser reproduzida, ou false se o usuário especificou que a faixa não deve ser reproduzida.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





