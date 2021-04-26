---
title: DDIV (SM5-ASM)
description: Computa uma divisão de precisão dupla de um componente.
ms.assetid: 0A67FC35-7F2F-4258-83CE-1CA398E57952
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81fc039b222b28a5fb1217d23c78470aff1739f7
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999153"
---
# <a name="ddiv-sm5---asm"></a>DDIV (SM5-ASM)

Computa uma divisão de precisão dupla de um componente.



| DDIV \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] \[ - \] src1 \[ \_ ABS \] \[ . swizzle\] |
|--------------------------------------------------------------------------------------------|



 



| Item                                                            | Descrição                                                                                   |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[no \] resultado da operação. O valor do resultado deve ser preciso para o 0,5 ULP. <br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[no \] dividendo.<br/>                                                               |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[no \] divisor.<br/>                                                                |



 

## <a name="remarks"></a>Comentários

A instrução DDIV será emitida pelo compilador do HLSL sempre que o operador de divisão for usado com duplos. A precisão dessa instrução será necessária para ser 0,5 ULP.

Os sombreadores que usam essa instrução serão marcados com um sinalizador de sombreador que fará com que eles não sejam associados, a menos que todas as condições a seguir sejam atendidas.

-   O sistema dá suporte ao DirectX 11,1.
-   O sistema inclui um Driver WDDM 1,2.
-   O driver fornece suporte para essa instrução por meio de **Opções de D3D11 de dados de recursos do D3D11 \_ \_ \_ \_ . ExtendedDoublesShaderInstructions** definido como **true**.

A tabela a seguir mostra os resultados btained ao executar a instrução com várias classes de números, supondo que nenhum estouro ou Subfluxo ocorra.

Nesta tabela, F significa um número real finito.



| **src0 src1->** | **-INF** | **-F** | **-1,0** | **-0** | **+0** | **+ 1,0** | **+ F** | **+ INF** | **NaN** |
|---------------------|----------|--------|----------|--------|--------|----------|--------|----------|---------|
| **-INF**            | NaN      | +inf   | +inf     | +inf   | -inf   | -inf     | -inf   | NaN      | NaN     |
| **-F**              | +0       | + F     | -src0    | +inf   | -inf   | src0     | -F     | -0       | NaN     |
| **-0**              | +0       | +0     | +0       | NaN    | NaN    | -0       | -0     | -0       | NaN     |
| **+0**              | -0       | -0     | -0       | NaN    | NaN    | +0       | +0     | +0       | NaN     |
| **+ F**              | -0       | -F     | -src0    | -inf   | +inf   | src0     | + F     | +0       | NaN     |
| **+ INF**            | NaN      | -inf   | -inf     | -inf   | +inf   | +inf     | +inf   | NaN      | NaN     |
| **NaN**             | NaN      | NaN    | NaN      | NaN    | NaN    | NaN      | NaN    | NaN      | NaN     |



 

Essa instrução se aplica aos seguintes estágios de sombreador:



| Vértice | Envoltória | Domain | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa instrução tem suporte nos seguintes modelos de sombreador:



| Modelo de Sombreador                                              | Suportado |
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

 

 





