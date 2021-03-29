---
title: m4x3-vs
description: Multiplica um vetor de 4 componentes por uma matriz 4x3. | m4x3-vs
ms.assetid: 12dd31bd-2078-44a1-912e-72c8f377bc4c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7608b1187cc90cf4914bdd42a197cc6044d53734
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968338"
---
# <a name="m4x3---vs"></a>m4x3-vs

Multiplica um vetor de 4 componentes por uma matriz 4x3.

## <a name="syntax"></a>Syntax



| m4x3 DST, src0, src1 |
|----------------------|



 

onde

-   DST é o registro de destino. O resultado é um vetor de 3 componentes.
-   src0 é um registro de origem que representa um vetor de 4 componentes.
-   src1 é um registro de origem que representa uma matriz 4x3, que corresponde ao primeiro de três registros consecutivos.

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| m4x3                   | x    | x    | x    | x     | x    | x     |



 

A máscara XYZ é necessária para o registro de destino. Os modificadores de negação e swizzle são permitidos para src0, mas não para src1.

O fragmento de código a seguir mostra as operações executadas.


```
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z) + (src0.w * src1.w);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z) + (src0.w * src2.w);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z) + (src0.w * src3.w);
```



O vetor de entrada está no registro src0. A matriz 4x3 de entrada está no registro src1 e nos próximos dois registros mais altos, conforme mostrado na expansão abaixo. Um resultado 3D é produzido, deixando o outro elemento do registro de destino (dest. w) não afetado.

Essa operação é normalmente usada para transformar um vetor de posição por uma matriz que não tem efeito projetado, como ocorre em transformações de espaço de modelo. Essa instrução é implementada como um par de produtos de ponto, conforme mostrado abaixo.


```
m4x3   r0.xyz, r1, c0    will be expanded to:

dp4   r0.x, r1, c0
dp4   r0.y, r1, c1
dp4   r0.z, r1, c2
```



Os modificadores swizzle e negação são inválidos para o registro src1. O registro de hora de verão e src0 não pode ser o mesmo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




