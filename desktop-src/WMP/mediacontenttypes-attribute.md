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
ms.openlocfilehash: 8979864151e029abf2731f6f0b4663e078a2c061
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748545"
---
# <a name="mediacontenttypes-attribute"></a>Atributo MediaContentTypes

O atributo **MediaContentTypes** especifica o tipo de conteúdo no item.

## <a name="applies-to"></a>Aplica-se A

-   [Playlists](playlist-attributes-ref.md)

## <a name="remarks"></a>Comentários

Esse atributo pode ser um dos seguintes valores:



| Valor | Significado                                |
|-------|----------------------------------------|
| 1     | A lista de reprodução contém o conteúdo de áudio.   |
| 2     | A ser fornecido.                        |
| 3     | A lista de reprodução contém o conteúdo de áudio.   |
| 4     | A lista de reprodução contém conteúdo de vídeo.   |
| 5     | A lista de reprodução contém conteúdo de imagem. |
| 6     | A lista de reprodução contém conteúdo de TV.      |



 

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





