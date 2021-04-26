---
title: min (sm4-ASM)
description: Mínimo de float de componente.
ms.assetid: 8EDD5503-76D5-4078-BFBA-1DA9260C6E68
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8791589b77edc66eeab4b48f10f4a9b16b5cb2d9
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993893"
---
# <a name="min-sm4---asm"></a>min (sm4-ASM)

Mínimo de float de componente.



| o mínimo \[ \_ \] \[ de dest. Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . swizzle \] , |
|---------------------------------------------------------------------------------------------|



 



| Item                                                            | Descrição                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[no \] resultado da operação.<br/> *dest*  =  *src0*  <  *src1* ? *src0* : *src1*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nos \] componentes para comparar com o *src1*.<br/>                                                  |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[nos \] componentes para comparar com o *src0*.<br/>                                                  |



 

## <a name="remarks"></a>Comentários

>= é usado em vez de > de forma que, se min (x, y) = x, Max (x, y) = y.

NaN tem tratamento especial. Se um operando de origem for NaN, o outro operando de origem será retornado e a escolha será feita por componente. Se ambos forem NaN, qualquer representação NaN será retornada. Isso está em conformidade com as novas regras IEEE 754R.

As desnormas são liberadas, com o sinal preservado, antes da comparação. No entanto, o resultado gravado no *dest* pode ou não ser liberado.

A tabela a seguir mostra os resultados obtidos ao executar a instrução com várias classes de números, supondo que nenhum estouro ou Subfluxo ocorra. F significa número real finito.



| **src0 src1->** | **-INF** | **F**        | **+ INF** | **NaN** |
|--------------------|----------|--------------|----------|---------|
| **-INF**           | -inf     | -inf         | -inf     | -inf    |
| **F**              | -inf     | src0 ou src1 | src0     | src0    |
| **-INF**           | -inf     | src1         | +inf     | +inf    |
| **NaN**            | -inf     | src1         | +inf     | NaN     |



 

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

 

 





