---
title: Atributo de descrição (SDK do WMP)
description: O atributo de descrição é uma descrição do conteúdo.
ms.assetid: 8bf76bf5-2bba-4ceb-bc98-f8b8ab2c8b6f
keywords:
- Atributo de descrição Windows Media Player
topic_type:
- apiref
api_name:
- Description
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78c4bc3562e7b807dc0e333c887aad1550d05b0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762086"
---
# <a name="description-attribute"></a>Atributo de descrição

O atributo de **Descrição** é uma descrição do conteúdo.

## <a name="applies-to"></a>Aplica-se A

-   [Arquivos de música](music-file-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado em arquivos de música, não na biblioteca do.

Esse atributo pode ter vários valores. Para recuperar todos os valores de um atributo com valores múltiplos, você deve usar a *mídia*. método **getItemInfoByType** , não o método *Media*. getItemInfo.

A constante do Windows Media Format SDK para esse atributo é g \_ wszWMDescription.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





