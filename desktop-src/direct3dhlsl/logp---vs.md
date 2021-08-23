---
title: logp – vs
description: Logp(x) de precisão parcial.
ms.assetid: 8547ca8a-7bde-4e41-9e65-f7fcd65454c1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3c33242ec23070a78e8adee159d35c19121dcc7c3dfe2c013c3d00adceb16477
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043774"
---
# <a name="logp---vs"></a>logp – vs

Logp(x) de precisão parcial.

## <a name="syntax"></a>Syntax



| logp dst, src |
|---------------|



 

onde

-   dst é o registro de destino.
-   src é um registro de origem. O registro de origem requer o uso explícito do swizzle de replicação, ou seja, exatamente um dos componentes .x, .y, .z, .w swizzle (ou os equivalentes .r, .g, .b, .a).

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| logp                   | x    | x    | x    | x     | x    | x     |



 

O fragmento de código a seguir mostra as operações executadas.


```
float f = abs(src);
if (f != 0)
    dest.x = dest.y = dest.z = dest.w = (float)(log(f)/log(2));
else
    dest.x = dest.y = dest.z = dest.w = -FLT_MAX;   
```



Essa instrução fornece precisão parcial de logaritmo base 2, até 10 bits.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




