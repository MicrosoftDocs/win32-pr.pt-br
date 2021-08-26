---
title: m3x4 – ps
description: Multiplica um vetor de 3 componentes por uma matriz 3x4. | m3x4 – ps
ms.assetid: b749d3cd-2acf-450c-94f2-fea5e1c8f4d2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 21c7f5ed65531e4022f503acf1b2ca994c860894824b2614220e16d36743d52b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067926"
---
# <a name="m3x4---ps"></a>m3x4 – ps

Multiplica um vetor de 3 componentes por uma matriz 3x4.

## <a name="syntax"></a>Syntax



| m3x4 dst, src0, src1 |
|----------------------|



 

onde

-   dst é o registro de destino. O resultado é um vetor de quatro componentes.
-   src0 é um registro de origem que representa um vetor de três componentes.
-   src1 é um registro de origem que representa uma matriz 3x4, que corresponde ao primeiro de quatro registros consecutivos.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| m3x4                  |      |      |      |      | x    | x    | x     | x    | x     |



 

A máscara xyzw (padrão) é necessária para o registro de destino. Modificadores negate e swizzle são permitidos para src0, mas não para src1.

O snippet de código a seguir mostra as operações executadas.


```
 
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z);
dest.z = (src0.x*src3.x) + (src0.y*src3.y) + (src0.z*src3.z);
dest.w = (src0.x*src4.x) + (src0.y*src4.y) + (src0.z*src4.z);
```



O vetor de entrada está no registro src0. A matriz de entrada 3x4 está no registro src1 e os próximos dois registros superiores, conforme mostrado na expansão abaixo.

Essa operação geralmente é usada para transformar um vetor de posição por uma matriz que tem um efeito projetivo, mas não aplica nenhuma tradução. Essa instrução é implementada como um par de produtos de ponto, conforme mostrado aqui.


```
m3x4   r0.xyzw, r1, c0   will be expanded to: 

dp3 r0.x, r1, c0
dp3 r0.y, r1, c1
dp3 r0.z, r1, c2
dp3 r0.w, r1, c3
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




