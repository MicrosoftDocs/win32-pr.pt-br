---
title: Atributo temporário
description: O atributo temporário especifica se uma playlist é temporária.
ms.assetid: 0d967a70-97d1-4918-8068-fe2868ab41d2
keywords:
- Atributo temporário Windows Media Player
topic_type:
- apiref
api_name:
- Temporary
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a70ae8f3ae06ae44077cce3d8fa3fdf67dc853eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811948"
---
# <a name="temporary-attribute"></a>Atributo temporário

O atributo **temporário** especifica se uma playlist é temporária.

**Comentários**

Se você tiver recuperado uma lista de reprodução da biblioteca, as alterações feitas na playlist serão refletidas na biblioteca do usuário. Para evitar isso, chame [IWMPPlaylist:: setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-setiteminfo) passando o nome do atributo "Temporary" e o valor "true". Isso converte a instância de playlist em uma playlist temporária, que é segura para ser editada sem alterar a playlist original.

**Aplica-se a**

-   [Playlists](playlist-attributes-ref.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------|
| Versão<br/> | Windows Media Player 11<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





