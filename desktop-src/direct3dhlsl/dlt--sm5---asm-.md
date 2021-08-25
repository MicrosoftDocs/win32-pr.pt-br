---
title: dlt (sm5 – asm)
description: Comparação de precisão dupla de componentes menor que.
ms.assetid: A9DE5007-4ADD-403D-A2B7-EAE475E9DCCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 957037c5168299959e580cbc2ffda100bdac96bdb4fbd9f90242ffa53c416367
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024666"
---
# <a name="dlt-sm5---asm"></a>dlt (sm5 – asm)

Comparação de precisão dupla de componentes menor que.



| dlt \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle, \] \[ - \] src1 \[ \_ abs \] \[ .swizzle\] |
|--------------------------------------------------------------------------------------------|



 



| Item                                                            | Descrição                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[em \] O endereço dos resultados da operação.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[em \] Os componentes a comparar com *src1*.<br/>         |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[em \] Os componentes a comparar com *src0*.<br/>         |



 

## <a name="remarks"></a>Comentários

Essa instrução executa a comparação de ponto flutuante de precisão dupla (*src0*  <  *src1*) para cada componente e grava o resultado *para dest*.

Se a comparação for verdadeira, o 0xFFFFFFFF de 32 bits será retornado para esse componente. Caso contrário, os 0x00000000 de 32 bits são retornados.

A comparação com NaN retorna false.

As *máscaras de dest* válidas são qualquer um ou dois componentes. Ou seja: .x, .y, .z, .w, .xy, .xz, .xw, .yz, .yw, .zw O primeiro componente *dest* na máscara recebe o resultado de 32 bits para a primeira comparação dupla. O segundo componente na máscara (se presente) recebe o resultado de 32 bits para a segunda comparação dupla.

Os swizzles válidos para os parâmetros de origem são .xyzw, .xyxy, .zwxy, .zwzw. Os seguintes *mapeamentos de src* são pós-swizzle:

-   *src0* é um vec2 duplo em (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).
-   *src1* é um vec2 duplo em (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).

Essa instrução se aplica aos seguintes estágios do sombreador:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa instrução tem suporte nos seguintes modelos de sombreador:



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | não        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | não        |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do modelo de sombreador 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





