---
description: Se esse bit for definido, o texto no controle será exibido em uma única linha. Se o texto se estender além das margens do controle, ele será truncado e uma reellipse (&\# 0034;...&\# 0034;) é inserido no final para indicar o truncamento. Se esse bit não estiver definido, o texto será wraps.
ms.assetid: 0dec3d25-0da7-4054-8d5c-55e81be16489
title: Atributo de controle NoWrap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1ef67a58dd0898b4c1e6d1577d35d67e8810649d49425087fecc3e0b3518cbb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519636"
---
# <a name="nowrap-control-attribute"></a>Atributo de controle NoWrap

Se esse bit for definido, o texto no controle será exibido em uma única linha. Se o texto se estender além das margens do controle, ele será truncado e uma reellipse ("...") será inserida no final para indicar o truncamento. Se esse bit não estiver definido, o texto será wraps.

## <a name="valid-controls"></a>Controles válidos

[Text](text-control.md)

## <a name="value"></a>Valor



| Decimal | Hexadecimal | Constante                         |
|---------|-------------|----------------------------------|
| 262144  | 0x00040000  | **msidbControlAttributesNoWrap** |



 

## <a name="remarks"></a>Comentários

Para definir esse atributo em um controle, inclua o bit NoWrap na coluna Atributos do registro do controle na [tabela Controle](control-table.md).

Consulte [Controlar atributos](control-attributes.md) e [controles](controls.md).

 

 



