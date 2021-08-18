---
title: m3x2 – vs
description: Multiplica um vetor de 3 componentes por uma matriz 3x2. | m3x2 – vs
ms.assetid: 4ef3bd47-3e38-4d9d-a8f5-6ee9c08de69c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ad05ef52970e30d2a130279c6109409205acb9615816e3fa0c7e185998f62254
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854136"
---
# <a name="m3x2---vs"></a>m3x2 – vs

Multiplica um vetor de 3 componentes por uma matriz 3x2.

## <a name="syntax"></a>Syntax



| m3x2 dst, src0, src1 |
|----------------------|



 

onde

-   dst é o registro de destino. O resultado é um vetor de dois componentes.
-   src0 é um registro de origem que representa um vetor de três componentes.
-   src1 é um registro de origem que representa uma matriz 3x2, que corresponde ao primeiro de dois registros consecutivos.

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| m3x2                   | x    | x    | x    | x     | x    | x     |



 

A máscara xy é necessária para o registro de destino. Modificadores negate e swizzle são permitidos para src0, mas não para src1.

As equações a seguir mostram como a instrução opera:


```
dest.x = (src0.x * src1.x) + (src0.x * src1.y) + (src0.x * src1.z);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z);
```



O vetor de entrada está no registro src0. A matriz de entrada 3x2 está no registro src1 e o próximo registro superior no mesmo arquivo de registro, conforme mostrado na expansão a seguir. Um resultado 2D é produzido, deixando os outros elementos do registro de destino (dest.z e dest.w) não afetados.

Essa operação é normalmente usada para as transformação 2D. Essa instrução é implementada como um par de produtos de ponto, conforme mostrado aqui.


```
m3x2   r0.xy, r1, c0   which will be expanded to:

dp3   r0.x, r1, c0
dp3   r0.y, r1, c1
```



Modificadores swizzle e negate são inválidos para o registro src1. O registro dest e src0 ou qualquer um dos registros src1+i não pode ser o mesmo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




