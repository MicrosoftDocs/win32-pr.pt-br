---
description: Se o bit de controle visível estiver definido, o controle ficará visível na caixa de diálogo. Se esse bit não estiver definido, o controle ficará oculto na caixa de diálogo. O estado visível ou oculto do atributo de controle visível pode ser alterado posteriormente por um evento de controle.
ms.assetid: 77d3164c-ea8a-4dcf-afd5-02bb2c2568c6
title: Atributo de controle visível
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550513f6bd0e40e58694c2c15a9986b5b02f289c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790029"
---
# <a name="visible-control-attribute"></a>Atributo de controle visível

Se o bit de controle visível estiver definido, o controle ficará visível na caixa de diálogo. Se esse bit não estiver definido, o controle ficará oculto na caixa de diálogo. O estado visível ou oculto do atributo de controle visível pode ser alterado posteriormente por um [evento de controle](control-events.md).

## <a name="valid-controls"></a>Controles válidos

Todos os controles.

## <a name="value"></a>Valor



| Decimal | Hexadecimal | Constante                          |
|---------|-------------|-----------------------------------|
| 1       | 0x00000001  | **msidbControlAttributesVisible** |



 

## <a name="remarks"></a>Comentários

Você pode usar a [tabela ControlCondition](controlcondition-table.md) para mostrar ou ocultar um controle de acordo com o valor de uma propriedade ou instrução condicional. Você também pode mostrar ou ocultar um controle assinando o controle em um [ControlEvent,](control-events.md). Insira o identificador do atributo na coluna atributo e o identificador do evento na coluna evento da [tabela EventMappings](eventmapping-table.md).

Consulte [controlar atributos](control-attributes.md) e [controles](controls.md).

 

 



