---
title: Atributo WM/ContentGroupDescription
description: O atributo WM/ContentGroupDescription é a descrição do grupo de conteúdo, que é uma coleção de itens de mídia, como um conjunto de CD na caixa.
ms.assetid: b2615f78-2d45-45f0-89f7-f1e8e083be9b
keywords:
- Windows Media Player do atributo WM/ContentGroupDescription
topic_type:
- apiref
api_name:
- WM/ContentGroupDescription
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49af85d5064da7950c3208e0307f027accb5e31b4e474eb743e629ecdf05aa0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118332445"
---
# <a name="wmcontentgroupdescription-attribute"></a>Atributo WM/ContentGroupDescription

O atributo **WM/ContentGroupDescription** é a descrição do grupo de conteúdo, que é uma coleção de itens de mídia, como um conjunto de CD na caixa.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [atributos de arquivo de mídia Windows usados com frequência](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado tanto na biblioteca quanto no arquivo de mídia digital.

**ContentGroupDescription** é um alias para este atributo.

a constante do SDK do formato de mídia Windows para esse atributo é g \_ wszWMContentGroupDistribution.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





