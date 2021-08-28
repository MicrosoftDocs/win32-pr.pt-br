---
title: m4x3 – ps
description: Multiplica um vetor de 4 componentes por uma matriz 4x3. | m4x3 – ps
ms.assetid: cf9ae4c3-6cdf-4c6f-b34c-0ebd3c8a4123
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4e291c268aae4173cb3ace4fc00beb5f1a3aa9f0b3d335f80891a851bcab41b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982026"
---
# <a name="m4x3---ps"></a>m4x3 – ps

Multiplica um vetor de 4 componentes por uma matriz 4x3.

## <a name="syntax"></a>Syntax



| m4x3 dst, src0, src1 |
|----------------------|



 

onde

-   dst é o registro de destino. O resultado é um vetor de três componentes.
-   src0 é um registro de origem que representa um vetor de quatro componentes.
-   src1 é um registro de origem que representa uma matriz 4x3, que corresponde ao primeiro de três registros consecutivos.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| m4x3                  |      |      |      |      | x    | x    | x     | x    | x     |



 

A máscara xyz é necessária para o registro de destino. Modificadores negate e swizzle são permitidos para src0, mas não para src1.

O snippet de código a seguir mostra as operações executadas.


```
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z) + (src0.w*src1.w);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z) + (src0.w*src2.w);
dest.z = (src0.x*src3.x) + (src0.y*src3.y) + (src0.z*src3.z) + (src0.w*src3.w);
```



O vetor de entrada está no registro src0. A matriz de entrada 4x3 está no registro src1 e os próximos dois registros superiores, conforme mostrado na expansão abaixo. Um resultado 3D é produzido, deixando o outro elemento do registro de destino (dest.w) não afetado.

Essa operação geralmente é usada para transformar um vetor de posição por uma matriz que não tem nenhum efeito projetivo, como ocorre em transformações de espaço de modelo. Essa instrução é implementada como um conjunto de produtos de ponto, conforme mostrado abaixo.


```
m4x3   r0.xyz, r1, c0    will be expanded to:

dp4   r0.x, r1, c0
dp4   r0.y, r1, c1
dp4   r0.z, r1, c2
```



Modificadores swizzle e negate são inválidos para o registro src1. O registro dst e src0 não pode ser o mesmo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




