---
title: exp - ps
description: Fornece precisão total exponencial 2x. | exp - ps
ms.assetid: 09e4446f-4149-4ec8-b3e3-2045b55bd591
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5ba7c5d2462e2f07d09da0162322f9a04b8f347768c5ba4cfcc8eb30cca78fad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117907899"
---
# <a name="exp---ps"></a>exp - ps

Fornece precisão total exponencial de 2<sup>x</sup>.

## <a name="syntax"></a>Syntax



| exp dst, src |
|--------------|



 

onde

-   dst é o registro de destino.
-   src é um registro de origem. O registro de origem requer o uso explícito do swizzle de replicação; ou seja, exatamente um dos componentes .x, .y, .z, .w swizzle (ou .r, .g, .b, .a equivalentes) deve ser especificado. Consulte [Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| exp                   |      |      |      |      | x    | x    | x     | x    | x     |



 

O snippet de código a seguir mostra as operações executadas:


```
dest.x = dest.y = dest.z = dest.w = (float)pow(2, src.replicateSwizzleComponent);
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




