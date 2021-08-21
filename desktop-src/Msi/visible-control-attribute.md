---
description: Se o bit de controle visível estiver definido, o controle ficará visível na caixa de diálogo. Se esse bit não estiver definido, o controle ficará oculto na caixa de diálogo. O estado visível ou oculto do atributo de controle visível pode ser alterado posteriormente por um evento de controle.
ms.assetid: 77d3164c-ea8a-4dcf-afd5-02bb2c2568c6
title: Atributo de controle visível
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78abdecdc46f179b7639a6ecaa627d92b643ed781ade242a152262d38c46f7eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498796"
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

 

 



