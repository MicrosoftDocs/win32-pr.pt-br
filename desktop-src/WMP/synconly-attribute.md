---
title: Atributo SyncOnly
description: O atributo SyncOnly é uma representação de cadeia de caracteres de um valor booliano que o Windows Media Player usa para determinar se uma lista de reprodução está disponível apenas para sincronização.
ms.assetid: 36149bb9-3a0b-4f6d-8be3-97d2a87faa83
keywords:
- Atributo SyncOnly Windows Media Player
topic_type:
- apiref
api_name:
- SyncOnly
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0245ffac2c4c64717adf669fcc6ff8fd0768382
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780334"
---
# <a name="synconly-attribute"></a>Atributo SyncOnly

O atributo **SyncOnly** é uma representação de cadeia de caracteres de um valor **booliano** que o Windows Media Player usa para determinar se uma lista de reprodução está disponível apenas para sincronização.

## <a name="applies-to"></a>Aplica-se A

-   [Playlists](playlist-attributes-ref.md)

## <a name="remarks"></a>Comentários

Um valor de 1 indica que a playlist está disponível somente para sincronização e não pode aparecer no nó de **playlist automática** . Um valor de zero indica que a lista de reprodução pode aparecer no nó de **playlist automática** .

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------|
| Versão<br/> | Windows Media Player 10 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





