---
title: sample_c_lz (sm4-ASM)
description: Executa um filtro de comparação. Essa instrução se comporta como exemplo \_ c, exceto que LOD é 0 e derivações são ignoradas.
ms.assetid: 5F11F091-AF2F-4293-88C7-824F11FE01E4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b2866bdfddf91f9bd6ab1bbccbc9d76de071065b3cf28c1093cb1fdb041f3db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981496"
---
# <a name="sample_c_lz-sm4---asm"></a>exemplo \_ c \_ LZ (sm4-ASM)

Executa um filtro de comparação. Essa instrução se comporta como [exemplo \_ c](sample-c--sm4---asm-.md), exceto que LOD é 0 e derivações são ignoradas.



| exemplo \_ c \_ LZ \[ \_ aoffimmi (u, v, w) \] dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource. r,//deve ser. r swizzle srcSampler, srcReferenceValue//componente único selecionado |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| Item                                                                                                                                       | Descrição                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                                            | \[no \] endereço dos resultados da operação.<br/>                                                             |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>                             | \[em \] um conjunto de coordenadas de textura. Para obter mais informações, consulte a instrução de [exemplo](sample--sm4---asm-.md) .<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/>                         | \[em \] um registro de textura. Para obter mais informações, consulte a instrução de **exemplo** .<br/>                                 |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>                             | \[em \] um registro de amostra. Para obter mais informações, consulte a instrução de **exemplo** .<br/>                                 |
| <span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*<br/> | \[em \] um registro com um único componente selecionado, que é usado na comparação.<br/>                            |



 

## <a name="remarks"></a>Comentários

O "LZ" significa nível zero. Como derivações são ignoradas, essa instrução está disponível em sombreadores além do sombreador de pixel.

Se essa instrução for usada com uma textura mipmapped, LOD 0 será amostrado, a menos que a amostra tenha um LOD fixe que coloca o LOD em outro lugar ou se houver uma tendência de LOD, o que simplesmente se referiria a partir de 0. Como derivações são ignoradas, a filtragem de anisotropic se comporta como filtragem de isotropic.

Em sombreadores de pixel, essa instrução pode ser usada dentro do controle de fluxo variável quando as coordenadas de textura são derivadas no sombreador, ao contrário da **amostra \_ c**.

A busca de um slot de entrada que não tem nada associado a ele retorna 0 para todos os componentes.

Essa instrução está disponível em todos os sombreadores, não apenas no sombreador de pixel, para fins de consistência.



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

 

 





