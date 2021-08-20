---
title: lrp – ps
description: Interpola linearmente entre os registros de segunda e terceira fonte por uma proporção especificada no primeiro registro de origem. | lrp – ps
ms.assetid: b360f28e-cb2a-4403-a020-180524df6549
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 716cbdd5492f768885b8dd91dca5a17f72c4ba50897274c2d6e11f340f563394
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117906866"
---
# <a name="lrp---ps"></a>lrp – ps

Interpola linearmente entre os registros de segunda e terceira fonte por uma proporção especificada no primeiro registro de origem.

## <a name="syntax"></a>Syntax



| lrp dst, src0, src1, src2 |
|---------------------------|



 

onde

-   dst é o registro de destino.
-   src0 é um registro de origem.
-   src1 é um registro de origem.
-   src2 é um registro de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Lrp                   | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

Essa instrução executa a interpolação linear com base na fórmula a seguir.


```
 
dest = src0 * src1 + (1-src0) * src2
// which is the same as
dest = src2 + src0 * (src1 - src2)
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




