---
title: booliano (WMI)
description: É um \_ parâmetro VT bool que assume o valor de Variant \_ TRUE (&\# 8211; 1) ou Variant \_ false (0).
ms.assetid: 3928ff39-ed17-4a61-bb72-a3c9be16ae45
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 569f7ce633bfb70fdba5e7055a80ad73ebd0fb6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811573"
---
# <a name="boolean-wmi"></a>booliano (WMI)

O tipo de dados booliano é um \_ parâmetro VT bool que assume o valor de Variant \_ true (– 1) ou Variant \_ false (0). A tabela a seguir lista a diferença entre as representações programáticas de **true** lógico em C/C++ e o tipo de automação.

| Idioma   | Valor         | Valor numérico |
|------------|---------------|-----------------|
| C/C++      | **TRUE**      | 1               |
| Automação | VARIANTE \_ true | – 1              |

Os dois tipos são diferentes de zero e, portanto, não são **falsos**, mas têm representações diferentes para **verdadeiro**.
