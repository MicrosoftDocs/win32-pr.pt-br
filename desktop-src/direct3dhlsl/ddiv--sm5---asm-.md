---
title: ddiv (sm5 – asm)
description: Calcula uma divisão de precisão dupla de componentes.
ms.assetid: 0A67FC35-7F2F-4258-83CE-1CA398E57952
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4730849b8ccc9070f538a58709bcd99fb9bfa552973c365fb3225806caf7aca0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986656"
---
# <a name="ddiv-sm5---asm"></a>ddiv (sm5 – asm)

Calcula uma divisão de precisão dupla de componentes.



| ddiv \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle \] \[ - \] src1 \[ \_ abs \] \[ .swizzle\] |
|--------------------------------------------------------------------------------------------|



 



| Item                                                            | Descrição                                                                                   |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[em \] O resultado da operação. O valor do resultado deve ser preciso para 0,5 ULP. <br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[em \] O dividendo.<br/>                                                               |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[em \] O divisor.<br/>                                                                |



 

## <a name="remarks"></a>Comentários

A instrução DDIV será emitida pelo compilador HLSL sempre que o operador de divisão for usado com doubles. A precisão dessa instrução será necessária para ser 0,5 ULP.

Sombreadores que usam essa instrução serão marcados com um sinalizador de sombreador que fará com que eles falhem na vinculação, a menos que todas as condições a seguir sejam atendidas.

-   O sistema dá suporte ao DirectX 11.1.
-   O sistema inclui um driver WDDM 1.2.
-   O driver relata suporte para essa instrução por meio **de D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS. ExtendedDoublesShaderInstructions** definido como **TRUE.**

A tabela a seguir mostra os resultados btained ao executar a instrução com várias classes de números, supondo que nenhum estouro ou estouro ocorra.

Nesta tabela F significa número finito-real.



| **src0 src1 ->** | **-inf** | **-F** | **-1.0** | **-0** | **+0** | **+1.0** | **+F** | **+inf** | **NaN** |
|---------------------|----------|--------|----------|--------|--------|----------|--------|----------|---------|
| **-inf**            | NaN      | +inf   | +inf     | +inf   | -inf   | -inf     | -inf   | NaN      | NaN     |
| **-F**              | +0       | +F     | -src0    | +inf   | -inf   | src0     | -F     | -0       | NaN     |
| **-0**              | +0       | +0     | +0       | NaN    | NaN    | -0       | -0     | -0       | NaN     |
| **+0**              | -0       | -0     | -0       | NaN    | NaN    | +0       | +0     | +0       | NaN     |
| **+F**              | -0       | -F     | -src0    | -inf   | +inf   | src0     | +F     | +0       | NaN     |
| **+inf**            | NaN      | -inf   | -inf     | -inf   | +inf   | +inf     | +inf   | NaN      | NaN     |
| **NaN**             | NaN      | NaN    | NaN      | NaN    | NaN    | NaN      | NaN    | NaN      | NaN     |



 

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

 

 





