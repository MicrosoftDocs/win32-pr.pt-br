---
title: dcl_output_control_point_count (sm5 – asm)
description: Declara a contagem de pontos de controle de saída do sombreador de chassi.
ms.assetid: 51E8117F-1802-413B-9820-04D5CEBE2DB6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93dc28a2af3ac50c835fa7ec38d7d344029af76a11cb2b84945dbf5009d68473
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024696"
---
# <a name="dcl_output_control_point_count-sm5---asm"></a>dcl \_ output control point count \_ \_ \_ (sm5 - asm)

Declara a contagem de pontos de controle de saída do sombreador de chassi.



| dcl \_ contagem de pontos de controle de saída \_ \_ \_ N |
|--------------------------------------|



 



| Item                                                   | Descrição                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="N"></span><span id="n"></span>*N*<br/> | \[em \] Um valor inteiro de 0 a 32 que especifica a contagem de pontos de controle de saída.<br/> |



 

## <a name="remarks"></a>Comentários

O sombreador de chassi poderá saída de 0 pontos de controle se eles não são necessários.

Essa instrução se aplica aos seguintes estágios do sombreador:



| Vértice | Casco                 | Domínio | Geometry | Pixel | Computação |
|--------|----------------------|--------|----------|-------|---------|
|        | Seção Declarações |        |          |       |         |



 

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

 

 





