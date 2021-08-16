---
title: samplepos (sm4.1 – asm)
description: Consulta a posição de um exemplo em uma determinada exibição de recurso de sombreador ou no rasterizador.
ms.assetid: 5A53B342-3A1D-4016-ABF2-CA6236D562C9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2457ca682adacf5daa274b3efbe6c76eb37523df4267cdb20131576815c2b6f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118510160"
---
# <a name="samplepos-sm41---asm"></a>samplepos (sm4.1 – asm)

Consulta a posição de um exemplo em uma determinada exibição de recurso de sombreador ou no rasterizador.



| samplepos dest \[ .mask \] , srcResource \[ .swizzle, \] sampleIndex (operand escalar) |
|--------------------------------------------------------------------------------|



 



| Item                                                                                                               | Descrição                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                    | \[em \] O endereço dos resultados da operação.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[em \] O recurso de sombreador.<br/>                         |
| <span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*sampleIndex*<br/> | \[em \] O índice do exemplo.<br/>                     |



 

## <a name="remarks"></a>Comentários

Essa instrução retorna a posição de exemplo 2D de *sampleIndex para* o recurso determinado. Ele é válido somente para recursos que podem ser carregados usando [**ld2dms,**](ld2dms--sm4-1---asm-.md) a menos que o rasterizador seja especificado *como srcResource*.

*srcResource pode* ser um registro t (uma exibição de recurso de \# sombreador) ou um registro de rasterizador.

A instrução calcula o vetor de ponto flutuante (Xposition, Yposition, 0, 0).

O swizzle em *srcResource* permite que os valores retornados sejam swizzled arbitrariamente antes de serem gravados no destino. A posição de exemplo é relativa ao centro do pixel, com base no Sistema de Coordenadas de Pixel.

Se *sampleIndex* estiver fora dos limites, um vetor zero será retornado. Se não houver nenhum recurso vinculado ao slot especificado, 0 será retornado.

**samplepos** podem ser usados para coisas como resolveções personalizadas no código do sombreador.

Essa instrução se aplica aos seguintes estágios do sombreador:



| Sombreador de vértice | Sombreador de geometria | Sombreador de pixel |
|---------------|-----------------|--------------|
|               |                 | x            |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa função tem suporte nos modelos de sombreador a seguir.



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | sim       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | não        |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do modelo de sombreador 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





