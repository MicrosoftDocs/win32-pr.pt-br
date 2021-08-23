---
title: Atributo MediaContentTypes
description: O atributo MediaContentTypes especifica o tipo de conteúdo no item.
ms.assetid: b91bab65-d6d2-4e05-9338-c24f28b7c71e
keywords:
- Atributo MediaContentTypes Windows Media Player
topic_type:
- apiref
api_name:
- MediaContentTypes
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eca3c422083954554db76657a0bb9cc10062fd878a9ebf4b31f4dc88734ac1d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996236"
---
# <a name="mediacontenttypes-attribute"></a>Atributo MediaContentTypes

O **atributo MediaContentTypes** especifica o tipo de conteúdo no item.

## <a name="applies-to"></a>Aplica-se A

-   [Playlists](playlist-attributes-ref.md)

## <a name="remarks"></a>Comentários

Esse atributo pode ser um dos seguintes valores:



| Valor | Significado                                |
|-------|----------------------------------------|
| 1     | A playlist contém conteúdo de áudio.   |
| 2     | A ser fornecido.                        |
| 3     | A playlist contém conteúdo de áudio.   |
| 4     | A playlist contém conteúdo de vídeo.   |
| 5     | A playlist contém conteúdo de imagem. |
| 6     | A playlist contém conteúdo de TV.      |



 

Para determinar se você pode alterar o valor desse atributo, use o [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player série 9 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





