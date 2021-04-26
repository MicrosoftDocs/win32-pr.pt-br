---
title: div (sm4-ASM)
description: Divisão por componente.
ms.assetid: B086F069-8F43-4746-A6A5-8F4462212648
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d406c5e61b4615990b445abe169619227d22124c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999093"
---
# <a name="div-sm4---asm"></a>div (sm4-ASM)

Divisão por componente.



| div \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] \[ - \] src1 \[ \_ ABS \] \[ . swizzle\] |
|-------------------------------------------------------------------------------------------|



 



| Item                                                            | Descrição                                    |
|-----------------------------------------------------------------|------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[no \] resultado da operação.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[no \] dividendo.<br/>                |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[no \] divisor.<br/>                 |



 

## <a name="remarks"></a>Comentários

A tabela a seguir mostra os resultados obtidos ao executar a instrução com várias classes de números, supondo que nenhum estouro ou Subfluxo ocorra.

Você deve observar as duas implementações permitidas de divide: a/b e a \* (1/b).

Um resultado disso é que há exceções à tabela abaixo para grandes valores de denominadores (maiores que 8.5070592 e + 37), em que 1/denominador é uma desnorma. Como as implementações podem executar a divisão como um \* (1/b), em vez de a/b diretamente, e 1/ \[ grande valor \] é uma desnorma que poderia ser liberada, alguns casos na tabela produzirão resultados diferentes. Por exemplo, (+/-) INF/(+/-) \[ valor > 8.5070592 e + 37 \] podem produzir Nan em algumas implementações, mas (+/-) inf em outras implementações

Nesta tabela, F significa um número real finito.



| **src0 src1->** | **-INF** | **-F**     | **-desnorma** | **-0** | **+0** | **+ desnormativo** | **+ F**     | **+ INF** | **Nan** |
|---------------------|----------|------------|-------------|--------|--------|-------------|------------|----------|---------|
| **-INF**            | -inf     | -inf       | -inf        | -inf   | -inf   | -inf        | -inf       | NaN      | NaN     |
| **-F**              | -inf     | -F         | src0        | src0   | src0   | src0        | +-F ou +-0 | +inf     | NaN     |
| **-desnorma**         | -inf     | src1       | -0          | -0     | +0     | +0          | src1       | +inf     | NaN     |
| **-0**              | -inf     | src1       | -0          | -0     | +0     | +0          | src1       | +inf     | NaN     |
| **+0**              | -inf     | src1       | +0          | +0     | +0     | +0          | src1       | +inf     | NaN     |
| **+ desnormativo**         | -inf     | src1       | +0          | +0     | +0     | +0          | src1       | +inf     | NaN     |
| **+ F**              | -inf     | +-F ou +-0 | src0        | src0   | src0   | src0        | + F         | +inf     | NaN     |
| **+ INF**            | NaN      | +inf       | +inf        | +inf   | +inf   | +inf        | +inf       | +inf     | NaN     |
| **NaN**             | NaN      | NaN        | NaN         | NaN    | NaN    | NaN         | NaN        | NaN      | NaN     |



 

Essa instrução se aplica aos seguintes estágios de sombreador:



| Sombreador de vértice | Sombreador de geometria | Sombreador de pixel |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                              | Suportado |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo do sombreador 4,1](dx-graphics-hlsl-sm4.md)              | sim       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sim       |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do Shader Model 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





