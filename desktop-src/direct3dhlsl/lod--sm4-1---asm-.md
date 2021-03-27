---
title: LOD (SM 4.1-ASM)
description: Retorna o nível de detalhe (LOD) que seria usado para filtragem de textura.
ms.assetid: A5931203-8CD7-4FC9-A4A4-CA981F38C7A3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1c1ca5a22a735945b76a60c175c665c5cf58fb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103638872"
---
# <a name="lod-sm41---asm"></a>LOD (SM 4.1-ASM)

Retorna o nível de detalhe (LOD) que seria usado para filtragem de textura.



| LOD dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource \[ . swizzle \] , srcSampler |
|--------------------------------------------------------------------------------|



 



| Item                                                                                                               | Descrição                                     |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[no \] endereço dos resultados.<br/>   |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[em \] um conjunto de coordenadas de textura.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[em \] um registro de textura.<br/>           |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[em \] um registro de amostra.<br/>           |



 

## <a name="remarks"></a>Comentários

Isso se comporta como a instrução de [exemplo](sample--sm4---asm-.md) , mas um exemplo filtrado não é gerado. A instrução computa o seguinte vetor (ClampedLOD, NonClampedLOD, 0, 0). NonClampedLOD é um valor LOD computado que ignora qualquer fixação MSS da amostra ou da textura (ou seja, pode retornar valores negativos). ClampedLOD é um valor LOD computado que seria usado pela instrução de **exemplo** real. O swizzle no *srcResource* permite que os valores retornados sejam swizzled arbitrariamente antes de serem gravados no destino.

Se não houver nenhum recurso associado ao slot especificado, 0 será retornado.

Se a amostra estiver usando a filtragem de anisotropic, o LOD deverá corresponder ao nível de MIP fracionário com base no eixo menor do espaço elíptico.

Isso é válido para os seguintes tipos de textura: Texture1D, Texture2D, Texture3D e TextureCube.

A instrução **LOD** não é definida quando usada com uma amostra que especifica a filtragem de MIP de ponto, especificamente, qualquer \_ enumeração de filtro d3d10 que termina no ponto de MIP \_ . (Um exemplo disso seria D3D10 \_ FILTRAR \_ o \_ ponto de MIP Mag mín \_ \_ .)

Essa instrução se aplica aos seguintes estágios de sombreador:



| Sombreador de vértice | Sombreador de geometria | Sombreador de pixel |
|---------------|-----------------|--------------|
|               |                 | x            |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo do sombreador 4,1](dx-graphics-hlsl-sm4.md)              | sim       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | não        |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do Shader Model 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





