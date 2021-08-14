---
title: drcp (sm5 – asm)
description: Calcula um recíproco de precisão dupla de componentes.
ms.assetid: 499A14D6-36DB-4860-94D1-887D931E60D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9539a53b27840b51d0a1d2e9904c744aa3f5c3e60bd9dc21a6bf72ba9291efa4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118515338"
---
# <a name="drcp-sm5---asm"></a>drcp (sm5 – asm)

Calcula um recíproco de precisão dupla de componentes.



| rcp \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle\] |
|------------------------------------------------------------|



 



| Item                                                            | Descrição                                                                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[em \] O endereço dos resultados<br/> *dest*  =  **1.0**  /  *src0*. O valor do resultado deve ser preciso para 1,0 ULP<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[em \] O número de o recíproco.<br/>                                                                         |



 

## <a name="remarks"></a>Comentários

A instrução DRCP é emitida pelo compilador HLSL somente quando explicitamente chamada por meio do intrínseco rcp(), quando um double é usado como o argumento . A precisão dessa instrução é necessária para ser 1,0 ULP.

Sombreadores que usam essa instrução serão marcados com um sinalizador de sombreador que fará com que eles falhem na vinculação, a menos que todas as condições a seguir sejam atendidas.

-   O sistema dá suporte ao DirectX 11.1.
-   O sistema inclui um driver WDDM 1.2.
-   O driver relata suporte para essa instrução por meio **de D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS. ExtendedDoublesShaderInstructions** definido como **TRUE.**

A tabela a seguir mostra os resultados obtidos ao executar a instrução com várias classes de números, supondo que nenhum estouro ou estouro ocorra.

Nesta tabela F significa número finito-real.



| **Src**->  | **-inf** | **-F** | **-0** | **+0** | **+F** | **+inf** | **NaN** |
|---------------|----------|--------|--------|--------|--------|----------|---------|
| **Dest**-> | -0       | -F     | -inf   | +inf   | +F     | +0       | NaN     |



 

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

 

 





