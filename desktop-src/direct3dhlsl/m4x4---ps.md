---
title: m4x4-PS
description: Multiplica um vetor de 4 componentes por uma matriz 4x4. | m4x4-PS
ms.assetid: 2a9915a3-f396-4108-97f7-d70c5262ff59
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 93f2da73c45151f5287f3acf773efb4bd57d21e1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968394"
---
# <a name="m4x4---ps"></a>m4x4-PS

Multiplica um vetor de 4 componentes por uma matriz 4x4.

## <a name="syntax"></a>Syntax



| m4x4 DST, src0, src1 |
|----------------------|



 

onde

-   DST é o registro de destino. O resultado é um vetor de 4 componentes.
-   src0 é um registro de origem que representa um vetor de 4 componentes.
-   src1 é um registro de origem que representa uma matriz 4x4, que corresponde ao primeiro de quatro registradores consecutivos.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| m4x4                  |      |      |      |      | x    | x    | x     | x    | x     |



 

A máscara xyzw (padrão) é necessária para o registro de destino. Os modificadores de negação e swizzle são permitidos para src0, mas não para src1.

Os modificadores swizzle e negação são inválidos para o registro src0. Os registros de horário de verão e src0 não podem ser iguais.

O trecho de código a seguir mostra as operações executadas.


```
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z) + (src0.w*src1.w);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z) + (src0.w*src2.w);
dest.z = (src0.x*src3.x) + (src0.y*src3.y) + (src0.z*src3.z) + (src0.w*src3.w);
dest.w = (src0.x*src4.x) + (src0.y*src4.y) + (src0.z*src4.z) + (src0.w*src4.w);
```



O vetor de entrada está no registro src0. A matriz 4x4 de entrada está no registro src1 e nos próximos três registros mais altos, conforme mostrado na expansão abaixo.

Essa operação é normalmente usada para transformar uma posição por uma matriz de projeção. Essa instrução é implementada como um conjunto de produtos dot, conforme mostrado aqui.


```
m4x4   r0.xyzw, r1, c0    will be expanded to:

dp4   r0.x, r1, c0
dp4   r0.y, r1, c1
dp4   r0.z, r1, c2
dp4   r0.w, r1, c3
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




