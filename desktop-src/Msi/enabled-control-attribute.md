---
description: Esse atributo especifica se o controle fornecido está habilitado ou desabilitado. A maioria dos controles aparece cinza quando desabilitada.
ms.assetid: d84b1b55-34e1-4173-b945-39a809014d55
title: Atributo de controle habilitado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb7c5cbbbc12353fc07cf50404a1feae1d98f1b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751204"
---
# <a name="enabled-control-attribute"></a>Atributo de controle habilitado

Esse atributo especifica se o controle fornecido está habilitado ou desabilitado. A maioria dos controles aparece cinza quando desabilitada.

Se esse bit for definido, o controle será criado como habilitado.

Se esse bit não estiver definido, o controle será criado como desabilitado.

## <a name="valid-controls"></a>Controles válidos

Todos os controles. A aparência de alguns controles que não estão associados a uma propriedade, como bitmaps e ícones, não é afetada pela definição deste atributo.

## <a name="value"></a>Valor



| Decimal | Hexadecimal | Constante                          |
|---------|-------------|-----------------------------------|
| 2       | 0x00000002  | **msidbControlAttributesEnabled** |



 

## <a name="remarks"></a>Comentários

Você também pode usar a [tabela ControlCondition](controlcondition-table.md) para desabilitar ou habilitar um controle de acordo com o valor de uma propriedade ou instrução condicional.

Você também pode habilitar ou desabilitar um controle inscrevendo o controle em um [ControlEvent,](control-events.md). Insira o identificador do atributo na coluna atributo e o identificador do evento na coluna evento da [tabela EventMappings](eventmapping-table.md).

Consulte [atributos de controle](control-attributes.md) e o controle que você precisa criar sob [controles](controls.md).

 

 



