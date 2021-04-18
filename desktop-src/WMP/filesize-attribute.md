---
title: Atributo FileSize
description: O atributo FileSize é o tamanho do arquivo em bytes.
ms.assetid: e845cc82-6975-4fd9-800f-a66f59a5fb39
keywords:
- Atributo FileSize Windows Media Player
topic_type:
- apiref
api_name:
- FileSize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cee243d85be59502acead3614dced49494c11104
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810549"
---
# <a name="filesize-attribute"></a>Atributo FileSize

O atributo **filesize** é o tamanho do arquivo em bytes.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Arquivos de mídia do Windows comumente usados](commonly-used-windows-media-file-attributes.md)
-   [Outros itens](other-item-attributes.md)
-   [Itens de foto](photo-item-attributes.md)
-   [Itens de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado tanto na biblioteca quanto no arquivo de mídia digital.

**Size** é um alias para este atributo.

A constante do Windows Media Format SDK para esse atributo é g \_ wszWMFileSize.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior (o item de foto tem suporte apenas no Windows Media Player 10 ou posterior)<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





