---
title: booliana (WMI)
description: É um parâmetro BOOL de VT que assume o valor \_ de VARIANT \_ TRUE (&\# 8211;1) ou VARIANT \_ FALSE (0).
ms.assetid: 3928ff39-ed17-4a61-bb72-a3c9be16ae45
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50422990a45dd59c2bedc3ac90bddcf06f7796cd3308daf03a11db0dca38f0b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051054"
---
# <a name="boolean-wmi"></a>booliana (WMI)

O tipo de dados booliana é um parâmetro BOOL de VT que assume o valor \_ de VARIANT \_ TRUE (–1) ou VARIANT \_ FALSE (0). A tabela a seguir lista a diferença entre as representações programáticas de **TRUE** lógico em C/C++ e o tipo de Automação.

| Idioma   | Valor         | Valor numérico |
|------------|---------------|-----------------|
| C/C++      | **TRUE**      | 1               |
| Automação | VARIANT \_ TRUE | –1              |

Ambos os tipos são diferentes de zero e, portanto, **não false,** mas têm representações diferentes para **TRUE.**
