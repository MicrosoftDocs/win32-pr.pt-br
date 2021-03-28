---
title: samplepos (SM 4.1-ASM)
description: Consulta a posição de um exemplo em uma determinada exibição de recurso do sombreador ou no rasterizador.
ms.assetid: 5A53B342-3A1D-4016-ABF2-CA6236D562C9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 910a542dafddb8b855e218f8702c746220780d6e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365276"
---
# <a name="samplepos-sm41---asm"></a>samplepos (SM 4.1-ASM)

Consulta a posição de um exemplo em uma determinada exibição de recurso do sombreador ou no rasterizador.



| samplepos dest \[ . Mask \] , srcResource \[ . swizzle \] , sampleIndex (operando escalar) |
|--------------------------------------------------------------------------------|



 



| Item                                                                                                               | Descrição                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[no \] endereço dos resultados da operação.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[no \] recurso do sombreador.<br/>                         |
| <span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*sampleIndex*<br/> | \[no \] índice do exemplo.<br/>                     |



 

## <a name="remarks"></a>Comentários

Essa instrução retorna a posição de exemplo 2D de *sampleIndex* de exemplo para o recurso fornecido. Ele é válido somente para recursos que podem ser carregados usando [**ld2dms**](ld2dms--sm4-1---asm-.md) , a menos que o rasterizador seja especificado como *srcResource*.

*srcResource* pode ser um \# registro t (uma exibição de recurso do sombreador) ou um registro do rasterizador.

A instrução computa o vetor de ponto flutuante (XPosition, YPosition, 0, 0).

O swizzle no *srcResource* permite que os valores retornados sejam swizzled arbitrariamente antes de serem gravados no destino. A posição de exemplo é relativa ao centro do pixel, com base no sistema de coordenadas de pixels.

Se *sampleIndex* estiver fora dos limites, um vetor zero será retornado. Se não houver nenhum recurso associado ao slot especificado, 0 será retornado.

**samplepos** pode ser usado para coisas como resolvedores personalizados no código do sombreador.

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

 

 





