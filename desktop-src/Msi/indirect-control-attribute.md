---
description: O atributo de controle indireto especifica se o valor exibido ou alterado por esse controle é referenciado indiretamente.
ms.assetid: dc9c0dd6-7e19-44ec-b1a5-3d51a1855adf
title: Atributo de controle indireto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6d0c183f586c197b14810e7176bce607ac3adaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827941"
---
# <a name="indirect-control-attribute"></a>Atributo de controle indireto

O atributo de controle indireto especifica se o valor exibido ou alterado por esse controle é referenciado indiretamente. Se esse bit for definido, o controle exibirá ou alterará o valor da propriedade que tem o identificador listado na coluna propriedade da [tabela de controle](control-table.md). Se esse bit não estiver definido, o controle exibirá ou alterará o valor da propriedade na coluna propriedade da tabela de controle.

## <a name="valid-controls"></a>Controles válidos

Todos os controles ativos.

## <a name="value"></a>Valor



| Decimal | Hexadecimal | Constante                           |
|---------|-------------|------------------------------------|
| 8       | 0x00000008  | **msidbControlAttributesIndirect** |



 

## <a name="remarks"></a>Comentários

Consulte [atributos de controle](control-attributes.md) e o controle que você precisa criar sob [controles](controls.md).

 

 



