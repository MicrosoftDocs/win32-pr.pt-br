---
title: Atributo SyncOnly
description: o atributo SyncOnly é uma representação de cadeia de caracteres de um valor booliano que Windows Media Player usa para determinar se uma lista de reprodução está disponível somente para sincronização.
ms.assetid: 36149bb9-3a0b-4f6d-8be3-97d2a87faa83
keywords:
- Windows Media Player de atributo SyncOnly
topic_type:
- apiref
api_name:
- SyncOnly
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e77fe67fe3cb943ad210f4d9beb58cfea8f32da87e6ee15955b578f07a608f39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134729"
---
# <a name="synconly-attribute"></a>Atributo SyncOnly

o atributo **SyncOnly** é uma representação de cadeia de caracteres de um valor **booliano** que Windows Media Player usa para determinar se uma lista de reprodução está disponível somente para sincronização.

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

 

 





