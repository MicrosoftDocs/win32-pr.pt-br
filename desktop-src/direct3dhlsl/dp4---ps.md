---
title: DP4-PS
description: Computa o produto de quatro componentes do ponto dos registros de origem. | DP4-PS
ms.assetid: 83ef6097-cacf-4498-842b-3eb03e57bd6f
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2562259af164b8680d54e9a120abaa405fd781c5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104012012"
---
# <a name="dp4---ps"></a>DP4-PS

Computa o produto de quatro componentes do ponto dos registros de origem.

## <a name="syntax"></a>Syntax



| DP4 DST, src0, src1 |
|---------------------|



 

onde

-   DST é o registro de destino.
-   src0 é um registro de origem.
-   src1 é um registro de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| dp4                   |      | x    | x    | x    | x    | x    | x     | x    | x     |



 

O trecho de código a seguir mostra as operações executadas:


```
dest.x = dest.y = dest.z = dest.w = 
    (src0.x * src1.x) + (src0.y * src1.y) + 
    (src0.z * src1.z) + (src0.w * src1.w);
```



Limitações para PS \_ 1 \_ 2 e PS \_ 1 \_ 3:

-   Cada sombreador pode usar até quatro instruções DP4.
-   Cada instrução DP4 conta como duas instruções aritméticas.

Limitações para \_ as versões 1 X:

-   Essa instrução não pode ser emitida em conjunto porque DP4 é executado no pipeline de vetor e alfa.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




