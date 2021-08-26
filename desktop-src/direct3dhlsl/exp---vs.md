---
title: exp - vs
description: Fornece precisão total exponencial 2x. | exp - vs
ms.assetid: 3644046b-3257-4257-9880-146ca50f6b0b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2b5b27067e83cbfd7604165ec1191d3371634aac15781a719377c92c69e29e6f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067946"
---
# <a name="exp---vs"></a>exp - vs

Fornece precisão total exponencial de 2<sup>x</sup>.

## <a name="syntax"></a>Syntax



| exp dst, src |
|--------------|



 

onde

-   dst é o registro de destino.
-   src é um registro de origem. O registro de origem requer o uso explícito do swizzle de replicação, ou seja, exatamente um dos componentes .x, .y, .z, .w swizzle (ou os equivalentes .r, .g, .b, .a). Consulte [Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md).

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| exp                    | x    | x    | x    | x     | x    | x     |



 

Essa instrução fornece pelo menos 21 bits de precisão.

O fragmento de código a seguir mostra as operações executadas:


```
dest.x = dest.y = dest.z = dest.w = (float)pow(2, src.replicateSwizzleComponent);
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




