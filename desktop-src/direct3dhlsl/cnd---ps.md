---
title: CND-PS
description: Escolhe condicionalmente entre src1 e src2, com base na comparação src0 0,5.
ms.assetid: 7a3b49e9-d146-47dc-99a8-4f336db7d0d5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cb31c873bf3a4e38048f57d75a30cec70021716d2aab43b683cb29aef25f7f23
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726956"
---
# <a name="cnd---ps"></a>CND-PS

Escolhe condicionalmente entre src1 e src2, com base na comparação src0 > 0,5.

## <a name="syntax"></a>Syntax



| CND DST, src0, src1, src2 |
|---------------------------|



 

onde

-   DST é o registro de destino.
-   src0 é um registro de origem.
-   src1 é um registro de origem.
-   src2 é um registro de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| cnd                   | x    | x    | x    | x    |      |      |       |      |       |



 

Para as versões 1 \_ 1 a 1 \_ 3, src0 deve ser r0. a.


```
// Version 1_1 to 1_3
if (r0.a > 0.5)
  dest = src1
else
  dest = src2
```



A versão 1 \_ 4 compara cada canal separadamente.


```
for each component in src0
{
   if (src0.component > 0.5)
     dest.component = src1.component
   else
     dest.component = src2.component
}
```



Esses exemplos mostram uma comparação de quatro canais feita em um sombreador da versão 1 \_ 4, bem como uma comparação de canal único possível em um sombreador da versão 1 \_ 1.


```
ps_1_4
def c0, -0.5, 0.5, 0, 0.6
def c1,  0,0,0,0
def c2,  1,1,1,1

cnd r1, c0, c1, c2   // r0 contains 1,1,1,0 because
// r1.x = c2.x because c0.x <= 0.5
// r1.y = c2.y because c0.y <= 0.5
// r1.z = c2.z because c0.z <= 0.5
// r1.w = c1.w because c0.w >  0.5
```



A versão 1 \_ 1 a 1 \_ 3 compara-se com o canal alfa replicado somente de r0.


```
ps_1_1
def c0, -0.5, 0.5, 0, 0.6
def c1,  0,0,0,0
def c2,  1,1,1,1
mov r0, c0
cnd r1, r0.a, c1, c2   // r1 gets assigned 0,0,0,0 because 
                       // r0.a > 0.5, therefore r1.xyzw = c1.xyzw
```



Este exemplo compara dois valores, A e B. O exemplo supõe que um é carregado em V0 e B é carregado em v1. Tanto a quanto B devem estar no intervalo de-1 a + 1 e, como os registros de cor (vn) são definidos como estando entre 0 e 1, a restrição é satisfeita neste exemplo.


```
ps_1_1                // Version instruction
sub r0, v0, v1_bias   // r0 = A - (B - 0.5)
cnd r0, r0.a, c0, c1  // r0 = ( A > B ? c0 : c1 )

// r0 = c0 if A > B, otherwise, r0 = c1
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




