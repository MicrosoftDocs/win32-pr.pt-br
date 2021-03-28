---
title: dcl_output_control_point_count (SM5-ASM)
description: Declara a contagem de pontos de controle de saída do sombreador envoltória.
ms.assetid: 51E8117F-1802-413B-9820-04D5CEBE2DB6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 147f8f7021252f07cdb6dd0f225555ff0f23d54b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104006928"
---
# <a name="dcl_output_control_point_count-sm5---asm"></a>\_ \_ \_ contagem de pontos de controle de saída de DCL \_ (SM5-ASM)

Declara a contagem de pontos de controle de saída do sombreador envoltória.



| contagem de pontos de controle de saída de DCL \_ \_ \_ \_ N |
|--------------------------------------|



 



| Item                                                   | Descrição                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="N"></span><span id="n"></span>*P*<br/> | \[em \] um valor inteiro de 0 a 32 que especifica a contagem de pontos de controle de saída.<br/> |



 

## <a name="remarks"></a>Comentários

O sombreador envoltória poderá produzir 0 pontos de controle se eles não forem necessários.

Essa instrução se aplica aos seguintes estágios de sombreador:



| Vértice | Envoltória                 | Domínio | Geometria | 16x16 | Computação |
|--------|----------------------|--------|----------|-------|---------|
|        | Seção de declarações |        |          |       |         |



 

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

 

 





