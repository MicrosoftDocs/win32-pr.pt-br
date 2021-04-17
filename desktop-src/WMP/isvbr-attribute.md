---
title: Atributo IsVBR
description: O atributo IsVBR indica se o conteúdo foi codificado usando a codificação de taxa de bits variável (VBR).
ms.assetid: faec0940-ef53-40a1-be54-a990884e907d
keywords:
- Atributo IsVBR Windows Media Player
topic_type:
- apiref
api_name:
- IsVBR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaec9f740e7b251c73ed12f5897ff9d95b023886
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811097"
---
# <a name="isvbr-attribute"></a>Atributo IsVBR

O atributo **IsVBR** indica se o conteúdo foi codificado usando a codificação de taxa de bits variável (VBR).

## <a name="applies-to"></a>Aplica-se A

-   [Arquivos de mídia do Windows comumente usados](commonly-used-windows-media-file-attributes.md)
-   [Itens de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado somente no arquivo de mídia digital.

A constante do Windows Media Format SDK para esse atributo é g \_ wszWMIsVBR.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





