---
description: Se esse bit for definido, o texto no controle será exibido em uma única linha. Se o texto ultrapassar as margens do controle, ele será truncado e uma reticências (&\# 0034;... &\# 0034;) é inserido no final para indicar o truncamento. Se esse bit não estiver definido, o texto será quebrado.
ms.assetid: 0dec3d25-0da7-4054-8d5c-55e81be16489
title: Atributo de controle NoWrap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51ee40b52fbec1c8add841f7055a7f42667eca94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789769"
---
# <a name="nowrap-control-attribute"></a>Atributo de controle NoWrap

Se esse bit for definido, o texto no controle será exibido em uma única linha. Se o texto ultrapassar as margens do controle, ele será truncado e uma reticências ("...") será inserida no final para indicar o truncamento. Se esse bit não estiver definido, o texto será quebrado.

## <a name="valid-controls"></a>Controles válidos

[Text](text-control.md)

## <a name="value"></a>Valor



| Decimal | Hexadecimal | Constante                         |
|---------|-------------|----------------------------------|
| 262144  | 0x00040000  | **msidbControlAttributesNoWrap** |



 

## <a name="remarks"></a>Comentários

Para definir esse atributo em um controle, inclua o bit nowrap na coluna atributos do registro do controle na [tabela de controle](control-table.md).

Consulte [controlar atributos](control-attributes.md) e [controles](controls.md).

 

 



