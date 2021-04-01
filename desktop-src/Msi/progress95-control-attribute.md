---
description: Se esse bit for definido em um controle ProgressBar, a barra será desenhada como uma série de retângulos pequenos. Se esse bit não estiver definido, a barra de indicadores de progresso será desenhada como um retângulo contínuo único.
ms.assetid: b2c43763-799c-4f09-b9f8-47a4a5f4faf3
title: Atributo de controle Progress95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2242dde671484274be946802ba4fd4c1cfd687
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829349"
---
# <a name="progress95-control-attribute"></a>Atributo de controle Progress95

Se esse bit for definido em um [controle ProgressBar](progressbar-control.md), a barra será desenhada como uma série de retângulos pequenos. Se esse bit não estiver definido, a barra de indicadores de progresso será desenhada como um retângulo contínuo único.

## <a name="valid-controls"></a>Controles válidos

[ProgressBar](progressbar-control.md)

## <a name="value"></a>Valor



| Decimal | Hexadecimal | Constante                             |
|---------|-------------|--------------------------------------|
| 65536   | 0x00010000  | **msidbControlAttributesProgress95** |



 

## <a name="remarks"></a>Comentários

Para definir esse atributo em um controle, inclua o bit Progress95 na coluna atributos do registro do controle na [tabela de controle](control-table.md).

Consulte [atributos de controle](control-attributes.md) e o controle que você precisa criar sob [controles](controls.md).

 

 



