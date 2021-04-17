---
title: Atributo WM/ContentGroupDescription
description: O atributo WM/ContentGroupDescription é a descrição do grupo de conteúdo, que é uma coleção de itens de mídia, como um conjunto de CD na caixa.
ms.assetid: b2615f78-2d45-45f0-89f7-f1e8e083be9b
keywords:
- Atributo WM/ContentGroupDescription do Windows Media Player
topic_type:
- apiref
api_name:
- WM/ContentGroupDescription
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4690e52f2745fa2761252fdba4ad4df31b18619
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780283"
---
# <a name="wmcontentgroupdescription-attribute"></a>Atributo WM/ContentGroupDescription

O atributo **WM/ContentGroupDescription** é a descrição do grupo de conteúdo, que é uma coleção de itens de mídia, como um conjunto de CD na caixa.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Atributos de arquivo de mídia do Windows comumente usados](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado tanto na biblioteca quanto no arquivo de mídia digital.

**ContentGroupDescription** é um alias para este atributo.

A constante do Windows Media Format SDK para esse atributo é g \_ wszWMContentGroupDistribution.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





