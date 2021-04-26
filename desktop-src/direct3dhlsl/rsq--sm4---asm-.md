---
title: RSQ (sm4-ASM)
description: Raiz quadrada recíproca de componente.
ms.assetid: CDA3C2DF-2793-4CE3-87CE-4E0AA945A1BB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1528e9f187ff7d4fb6074d42a1c574686f3b22f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998163"
---
# <a name="rsq-sm4---asm"></a>RSQ (sm4-ASM)

Raiz quadrada recíproca de componente.



| RSQ \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\] |
|------------------------------------------------------------|



 



| Item                                                            | Descrição                                                                                      |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[in \] contém os resultados da operação.<br/> *dest* = 1,0 f/sqrt (*src0*)<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nos \] componentes para a operação.<br/>                                              |



 

## <a name="remarks"></a>Comentários

O erro relativo máximo é 2-21.

A tabela a seguir mostra os resultados obtidos ao executar a instrução com várias classes de números, supondo que nenhum estouro ou Subfluxo ocorra.

F significa número real finito.



| **src**  | **-INF** | **-F** | **-desnorma** | **-0** | **+0** | **+ desnormativo** | **+ F** | **+ INF** | **NaN** |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| **dest** | NaN      | NaN    | -inf        | -inf   | +inf   | +inf        | + F     | +0       | NaN     |



 

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

 

 





