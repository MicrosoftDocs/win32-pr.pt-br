---
title: M3x4-vs
description: Multiplica um vetor de 3 componentes por uma matriz 3x4. | M3x4-vs
ms.assetid: 8bec1ac5-376b-4eae-ba82-b42a6c0e7c4e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a4018698dbe6ab986945a84c1fcf9ce0431bd0fc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968339"
---
# <a name="m3x4---vs"></a>M3x4-vs

Multiplica um vetor de 3 componentes por uma matriz 3x4.

## <a name="syntax"></a>Syntax



| M3x4 DST, src0, src1 |
|----------------------|



 

onde

-   DST é o registro de destino. O resultado é um vetor de 4 componentes.
-   src0 é um registro de origem que representa um vetor de 3 componentes.
-   src1 é um registro de origem que representa uma matriz 3x4, que corresponde ao primeiro de quatro registradores consecutivos.

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| m3x4                   | x    | x    | x    | x     | x    | x     |



 

A máscara xyzw (padrão) é necessária para o registro de destino. Os modificadores de negação e swizzle são permitidos para src0, mas não para src1.

O fragmento de código a seguir mostra as operações executadas.


```
 
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z);
dest.w = (src0.x * src4.x) + (src0.y * src4.y) + (src0.z * src4.z);
```



O vetor de entrada está no registro src0. A matriz 3x4 de entrada está no registro src1 e nos próximos três registros superiores, conforme mostrado na expansão abaixo.

Essa operação é normalmente usada para transformar um vetor de posição por uma matriz que tem um efeito projetado, mas não aplica nenhuma tradução. Essa instrução é implementada como um par de produtos de ponto, conforme mostrado aqui.


```
m3x4   r0.xyzw, r1, c0   will be expanded to: 

dp3 r0.x, r1, c0
dp3 r0.y, r1, c1
dp3 r0.z, r1, c2
dp3 r0.w, r1, c3
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




