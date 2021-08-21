---
title: drcp (SM5-ASM)
description: Computa um recíproco de precisão dupla por componente.
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
# <a name="drcp-sm5---asm"></a>drcp (SM5-ASM)

Computa um recíproco de precisão dupla por componente.



| RCP \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\] |
|------------------------------------------------------------|



 



| Item                                                            | Descrição                                                                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[no \] endereço dos resultados<br/> *dest*  =  **1,0**  /  *src0*. O valor do resultado deve ser preciso para o 1,0 ULP<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[no \] número para pegar o recíproco de.<br/>                                                                         |



 

## <a name="remarks"></a>Comentários

A instrução DRCP é emitida pelo compilador HLSL somente quando explicitamente chamado por meio de RCP () intrínseco, quando um Double é usado como o argumento. A precisão dessa instrução é necessária para ser 1,0 ULP.

Os sombreadores que usam essa instrução serão marcados com um sinalizador de sombreador que fará com que eles não sejam associados, a menos que todas as condições a seguir sejam atendidas.

-   O sistema dá suporte ao DirectX 11,1.
-   O sistema inclui um Driver WDDM 1,2.
-   O driver fornece suporte para essa instrução por meio de **Opções de D3D11 de dados de recursos do D3D11 \_ \_ \_ \_ . ExtendedDoublesShaderInstructions** definido como **true**.

A tabela a seguir mostra os resultados obtidos ao executar a instrução com várias classes de números, supondo que nenhum estouro ou Subfluxo ocorra.

Nesta tabela, F significa um número real finito.



| **orig**->  | **-INF** | **-F** | **-0** | **+0** | **+ F** | **+ INF** | **NaN** |
|---------------|----------|--------|--------|--------|--------|----------|---------|
| **dest**-> | -0       | -F     | -inf   | +inf   | + F     | +0       | NaN     |



 

Essa instrução se aplica aos seguintes estágios de sombreador:



| Vértice | Envoltória | Domínio | Geometry | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa instrução tem suporte nos seguintes modelos de sombreador:



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo do sombreador 4,1](dx-graphics-hlsl-sm4.md)              | não        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | não        |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do Shader Model 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





