---
description: O atributo de controle Indireto especifica se o valor exibido ou alterado por esse controle é referenciado indiretamente.
ms.assetid: dc9c0dd6-7e19-44ec-b1a5-3d51a1855adf
title: Atributo de controle indireto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c679938a818fb8393958c35694f3c2b7f782c91fc2dfcf1ac04777553ec629c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996682"
---
# <a name="indirect-control-attribute"></a>Atributo de controle indireto

O atributo de controle Indireto especifica se o valor exibido ou alterado por esse controle é referenciado indiretamente. Se esse bit for definido, o controle exibirá ou altera o valor da propriedade que tem o identificador listado na coluna Propriedade da [tabela Controle](control-table.md). Se esse bit não estiver definido, o controle exibirá ou altera o valor da propriedade na coluna Propriedade da tabela Controle.

## <a name="valid-controls"></a>Controles válidos

Todos os controles ativos.

## <a name="value"></a>Valor



| Decimal | Hexadecimal | Constante                           |
|---------|-------------|------------------------------------|
| 8       | 0x00000008  | **msidbControlAttributesIndirect** |



 

## <a name="remarks"></a>Comentários

Consulte [Atributos de controle](control-attributes.md) e o controle que você precisa criar em [Controles](controls.md).

 

 



