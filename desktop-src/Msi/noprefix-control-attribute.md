---
description: Se esse bit for definido em um controle de texto, a ocorrência do caractere &\# 0034; &&\# 0034; em uma cadeia de caracteres de texto será exibida como ela mesma. Se esse bit não estiver definido, o caractere seguinte &\# 0034; &&\# 0034; na cadeia de caracteres de texto será exibido como um caractere sublinhado.
ms.assetid: b958eecb-2f44-420f-8c93-7a4bd8b589da
title: Atributo de controle NoPrefix
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1e1a0c6da65605efca1aacc4582b34a8f673d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164995"
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

 

 



