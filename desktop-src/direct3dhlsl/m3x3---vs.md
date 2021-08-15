---
title: m3x3-vs
description: Multiplica um vetor de 3 componentes por uma matriz de 3x3. | m3x3-vs
ms.assetid: 6a749ed0-097d-4354-bc70-fbcd879eafab
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 11c1caa682751c3c4d112efd07643233e9cac91392c9e3bb9c575b1f89f5b53f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119562056"
---
# <a name="m3x3---vs"></a>m3x3-vs

Multiplica um vetor de 3 componentes por uma matriz de 3x3.

## <a name="syntax"></a>Syntax



| m3x3 DST, src0, src1 |
|----------------------|



 

onde

-   DST é o registro de destino. O resultado é um vetor de 3 componentes.
-   src0 é um registro de origem que representa um vetor de 3 componentes.
-   src1 é um registro de origem que representa uma matriz 3x3, que corresponde ao primeiro de três registros consecutivos.

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| m3x3                   | x    | x    | x    | x     | x    | x     |



 

A máscara XYZ é necessária para o registro de destino. Os modificadores de negação e swizzle são permitidos para src0, mas não para src1.

O fragmento de código a seguir mostra as operações executadas.


```
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z);
```



O vetor de entrada está no registro src0. A matriz de 3x3 de entrada está no registro src1 e nos próximos dois registros mais altos, conforme mostrado na expansão abaixo. Um resultado 3D é produzido, deixando o outro elemento do registro de destino (dest. w) não afetado.

Essa operação é normalmente usada para transformar vetores normais durante cálculos de iluminação. Essa instrução é implementada como um par de produtos de ponto, conforme mostrado abaixo.


```
m3x3 r0.xyz, r1, c0  which will be expanded to:

dp3   r0.x, r1, c0
dp3   r0.y, r1, c1
dp3   r0.z, r1, c2
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




