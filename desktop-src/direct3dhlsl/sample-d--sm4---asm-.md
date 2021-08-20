---
title: sample_d (sm4-ASM)
description: Amostras de dados do elemento/textura especificado usando o endereço especificado e o modo de filtragem identificados pelo determinado exemplo. | sample_d (sm4-ASM)
ms.assetid: 9CF57C4A-C0D1-4D57-A5EE-62BBBB291438
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7b3e1e45c0ea41834ad258fc5a2f900f25be9a0394a5e33be5e170222b88cf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117906245"
---
# <a name="sample_d-sm4---asm"></a>exemplo \_ d (sm4-ASM)

Amostras de dados do elemento/textura especificado usando o endereço especificado e o modo de filtragem identificados pelo determinado exemplo.



| ssample \_ d \[ \_ aoffimmi (u, v, w) \] dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource \[ . swizzle \] , srcSampler, srcXDerivatives \[ . swizzle \] , srcYDerivatives \[ . swizzle\] |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| Item                                                                                                                               | Descrição                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                                    | \[no \] endereço dos resultados da operação.<br/>                                                                  |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>                     | \[em \] um conjunto de coordenadas de textura. Para obter mais informações, consulte a instrução de [exemplo](sample--sm4---asm-.md) .<br/>      |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/>                 | \[em \] um registro de textura. Para obter mais informações, consulte a instrução de **exemplo** .<br/>                                      |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>                     | \[em \] um registro de amostra. Para obter mais informações, consulte a instrução de **exemplo** .<br/>                                      |
| <span id="srcXDerivatives"></span><span id="srcxderivatives"></span><span id="SRCXDERIVATIVES"></span>*srcXDerivatives*<br/> | \[nas \] derivações do endereço de origem na direção x. Para obter mais informações, consulte a seção **comentários** .<br/> |
| <span id="srcYDerivatives"></span><span id="srcyderivatives"></span><span id="SRCYDERIVATIVES"></span>*srcYDerivatives*<br/> | \[nas \] derivações do endereço de origem na direção y. Para obter mais informações, consulte a seção **comentários** .<br/> |



 

## <a name="remarks"></a>Comentários

Essa instrução se comporta como a instrução de [exemplo](sample--sm4---asm-.md) , exceto que derivativos para o endereço de origem na direção x e a direção y são fornecidos por parâmetros extras, *srcXDerivatives* e *srcYDerivatives*, respectivamente. Esses derivativos estão no espaço de coordenadas de textura normalizado.

Os componentes r, g e b de *srcXDerivatives* (pos-swizzle) fornecem du/DX, DV/DX e DW/DX. O componente ' a ' (POS-swizzle) é ignorado.

Os componentes r, g e b de *srcYDerivatives* (pos-swizzle) fornecem du/DY, DV/DY e DW/DY. O componente ' a ' (POS-swizzle) é ignorado.

Ao contrário da instrução de **exemplo** , que tem permissão para compartilhar um único cálculo de LOD em um carimbo 2x2, o **exemplo \_ d** deve calcular o LOD completamente de forma independente, por pixel, quando usado no sombreador de pixel.

Se as entradas derivadas para a **amostra \_ d** vieram de instruções de cálculo derivativo no sombreador de pixel e os valores incluírem inf/Nan, o comportamento do **exemplo \_ d** pode não corresponder à instrução de **exemplo** , que computa implicitamente a derivada. Os valores INF/NaN podem afetar o cálculo de LOD de maneira diferente.

A busca de um slot de entrada que não tem nada associado a ele retorna 0 para todos os componentes.

### <a name="restrictions"></a>Restrições

-   o **exemplo \_ d** herda as mesmas restrições que a instrução de **exemplo** , além de uma restrição adicional abaixo para seus parâmetros adicionais.
-   *srcXDerivatives* e *srcYDerivatives* devem ser temp (r \# /x \# ), constantBuffer (CB \# ), registros de entrada (v \# ) ou valor (es) imediato (s).

Essa instrução se aplica aos seguintes estágios de sombreador:



| Sombreador de vértice | Sombreador de geometria | Sombreador de pixel |
|---------------|-----------------|--------------|
| X             | X               | x            |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                              | Com suporte |
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

 

 





