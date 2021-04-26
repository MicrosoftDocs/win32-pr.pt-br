---
title: log (sm4-ASM)
description: Base do log baseado em componente 2.
ms.assetid: 6D28864A-C2BA-44AF-9E78-7C2B34F5E462
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88e4b89b4dcc085cf4fd4fda762d96fb71271af2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998313"
---
# <a name="log-sm4---asm"></a>log (sm4-ASM)

Base do log baseado em componente 2.



| log \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle |
|----------------------------------------------------------|



 



| Item                                                            | Descrição                                                                                |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[no \] endereço do resultado da operação.<br/> dest = log2 (src0)<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[no \] valor da operação.<br/>                                             |



 

## <a name="remarks"></a>Comentários

### <a name="restrictions"></a>Restrições

-   Segue a teoria do limite.
-   Tolerância a erros: se *src0* for \[ 0,5.. 2 \] , o erro Absolue não deverá ser maior que 2-21. Se *src0* for (0.. 0,5) ou (2.. + inf \] , o erro relativo não deverá ser maior que 2-21.

A tabela a seguir mostra os resultados obtidos ao executar a instrução com várias classes de números, supondo que nenhum estouro ou Subfluxo ocorra. F significa número real finito.



| **src**  | **-INF** | **-F** | **-desnorma** | **-0** | **+0** | **+ desnormativo** | **+ F** | **+ INF** | **NaN** |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| **dest** | NaN      | NaN    | -inf        | -inf   | -inf   | -inf        | F      | +inf     | NaN     |



 

Essa instrução se aplica aos seguintes estágios de sombreador:



| Sombreador de vértice | Sombreador de geometria | Sombreador de pixel |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

### <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

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

 

 





