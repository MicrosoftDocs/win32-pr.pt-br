---
title: Estrutura de atributos de interseção
description: Uma estrutura declarada em HLSL para representar atributos de acerto para interseção de triângulo de função fixa ou caixa delimitada alinhada por eixo para interseção primitiva de procedimento.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: language-reference
ms.date: 05/31/2018
ms.openlocfilehash: fea10edb8402f07431d488ff9d28d1de539259e51bc1893d20e76e8f4cc3cdab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118528114"
---
# <a name="intersection-attributes-structure"></a>Estrutura de atributos de interseção 

Uma estrutura declarada em HLSL para representar atributos de acerto para interseção de triângulo de função fixa ou caixa delimitada alinhada por eixo para interseção primitiva de procedimento.

## <a name="fixed-function-triangle-intersection"></a>Interseção de triângulo de função fixa

A seguinte estrutura é declarada em HLSL para representar atributos de acerto para interseção de triângulo de função fixa:


```
struct BuiltInTriangleIntersectionAttributes
{
    float2 barycentrics;
};
```

[Todos os sombreadores](any-hit-shader.md) [de acerto e de](closest-hit-shader.md) acerto mais próximos invocados usando interseção de triângulo de função fixa devem usar essa estrutura para atributos de acerto. Considerando os atributos a0, a1 e a2 para os três vértices de um triângulo, barycentrics.x é o peso para a1 e barycentrics.y é o peso para a2.  Por exemplo, o aplicativo pode interpolar fazendo: a = a0 + barycentrics.x * (a1-a0) + barycentrics.y* (a2 – a0).

## <a name="axis-aligned-bounding-box-for-procedural-primitive-intersection"></a>Caixa delimitada alinhada por eixo para interseção primitiva de procedimento

Quando caixas delimitadas alinhadas por eixo são usadas para interseção com primitivos de procedimento, um sombreador de interseção é disparado.  Esse sombreador fornece uma estrutura de atributo de interseção definida pelo usuário para a [**chamada ReportHit.**](reporthit-function.md)  Os sombreadores de acerto e de acerto mais próximos vinculados no mesmo grupo de acertos com esse sombreador de interseção devem usar a mesma estrutura para atributos de acerto, mesmo que os atributos não sejam referenciados.  O tamanho máximo da estrutura de atributo é de 32 bytes, definido como **D3D12 \_ RAYTRACING \_ MAX ATTRIBUTE SIZE IN \_ \_ \_ \_ BYTES**.


