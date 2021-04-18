---
description: Se esse bit for definido, o botão de opção terá texto e uma borda exibida ao seu respeito.
ms.assetid: 25f88e07-a17d-4a5a-bf4f-5615e371cf6b
title: Atributo de controle HasBorder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dfce5e1938ea4896678eb192665babd3632549e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764656"
---
# <a name="hasborder-control-attribute"></a>Atributo de controle HasBorder

Se esse bit for definido, o [botão de opção](radiobuttongroup-control.md) terá texto e uma borda exibida ao seu respeito.

Se o bit de estilo não estiver definido, a borda não será exibida e nenhum texto será exibido no grupo.

## <a name="valid-controls"></a>Controles válidos

[Botão de opção](radiobuttongroup-control.md)

## <a name="valid"></a>Válido



| Decimal  | Hexadecimal | Constante                            |
|----------|-------------|-------------------------------------|
| 16777216 | 0x01000000  | **msidbControlAttributesHasBorder** |



 

## <a name="remarks"></a>Comentários

Para definir esse atributo em um controle, inclua os bits HasBorder na coluna atributos do registro do controle na [tabela de controle](control-table.md).

Consulte [atributos de controle](control-attributes.md) e o controle que você precisa criar sob [controles](controls.md).

 

 



