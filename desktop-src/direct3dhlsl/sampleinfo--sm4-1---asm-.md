---
title: sampleinfo (SM 4.1-ASM)
description: Consulta o número de amostras em uma determinada exibição de recurso do sombreador ou no rasterizador.
ms.assetid: 1F0968D7-01E9-4213-9F83-172B88374C3C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d307dbc8c79618a6401737874a9f6e060a899ccc
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103823467"
---
# <a name="sampleinfo-sm41---asm"></a>sampleinfo (SM 4.1-ASM)

Consulta o número de amostras em uma determinada exibição de recurso do sombreador ou no rasterizador.



| \[\_\]dest \[ . Mask \] , srcResource \[ . swizzle\] |
|---------------------------------------------------|



 



| Item                                                                                                               | Descrição                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[no \] endereço dos resultados da operação.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[no \] recurso do sombreador.<br/>                         |



 

## <a name="remarks"></a>Comentários

Essa instrução retorna o número de amostras para o recurso fornecido ou o rasterizador. Ele é válido somente para recursos que podem ser carregados usando [**ld2dms**](ld2dms--sm4-1---asm-.md) , a menos que o rasterizador seja especificado como *srcResource*. *srcResource* poderia ser um \# registro t (uma exibição de recurso do sombreador) ou um registro do rasterizador.

A instrução computa o vetor (SampleCount, 0, 0, 0).

O swizzle no *srcResource* permite que os valores retornados sejam swizzled arbitrariamente antes de serem gravados no destino. O valor retornado é ponto flutuante, a menos que o \_ modificador uint seja usado; nesse caso, o valor retornado é inteiro. Se não houver nenhum recurso associado ao slot especificado, 0 será retornado.

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
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | não        |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do Shader Model 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





