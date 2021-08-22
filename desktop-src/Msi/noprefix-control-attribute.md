---
description: Se esse bit for definido em um controle de texto, a ocorrência do caractere &\# 0034; &&\# 0034; em uma cadeia de caracteres de texto será exibida como ela mesma. Se esse bit não estiver definido, o caractere seguinte &\# 0034; &&\# 0034; na cadeia de caracteres de texto será exibido como um caractere sublinhado.
ms.assetid: b958eecb-2f44-420f-8c93-7a4bd8b589da
title: Atributo de controle NoPrefix
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15345bb56ad85ec654cffe7a0bf2173973e032ac33aca633105d3a220647cf93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065876"
---
# <a name="noprefix-control-attribute"></a>Atributo de controle NoPrefix

Se esse bit for definido em um controle de texto, a ocorrência do caractere "&" em uma cadeia de texto será exibida como a si mesma. Se esse bit não estiver definido, o caractere após "&" na cadeia de texto será exibido como um caractere sublinhado.

## <a name="valid-controls"></a>Controles válidos

[Text](text-control.md)

## <a name="value"></a>Valor



| Decimal | Hexadecimal | Constante                           |
|---------|-------------|------------------------------------|
| 131072  | 0x20000     | **msidbControlAttributesNoPrefix** |



 

## <a name="remarks"></a>Comentários

Para definir esse atributo em um controle, inclua o bit NoPrefix na coluna atributos do registro do controle na [tabela de controle](control-table.md).

Consulte [controlar atributos](control-attributes.md) e [controles](controls.md).

 

 



