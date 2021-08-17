---
title: Estrutura de atributos de interseção
description: Uma estrutura declarada em HLSL para representar os atributos de acesso para a interseção de triângulo de função fixa ou a caixa delimitadora alinhada por eixo para a interseção de procedimento primitivo.
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

Uma estrutura declarada em HLSL para representar os atributos de acesso para a interseção de triângulo de função fixa ou a caixa delimitadora alinhada por eixo para a interseção de procedimento primitivo.

## <a name="fixed-function-triangle-intersection"></a>Interseção de triângulo de função fixa

A seguinte estrutura é declarada em HLSL para representar os atributos de acesso para a interseção de triângulo de função fixa:


```
struct BuiltInTriangleIntersectionAttributes
{
    float2 barycentrics;
};
```

[Quaisquer pressionamentos](any-hit-shader.md) de tecla de acesso e [mais próximos](closest-hit-shader.md) invocados usando a interseção de triângulo de função fixa devem usar essa estrutura para os atributos de pressionamento. Determinados atributos a0, a1 e a2 para os 3 vértices de um triângulo, barycentrics. x é o peso para a1 e barycentrics. y é o peso de a2.  Por exemplo, o aplicativo pode se interpolar fazendo: a = a0 + barycentrics. x * (a1-a0) + barycentrics. y * (a2 – a0).

## <a name="axis-aligned-bounding-box-for-procedural-primitive-intersection"></a>Caixa delimitadora alinhada ao eixo para a interseção de procedimento primitivo

Quando caixas delimitadores alinhadas por eixo são usadas para interseção com primitivos de procedimento, um sombreador de interseção é disparado.  Esse sombreador fornece uma estrutura de atributo de interseção definida pelo usuário para a chamada [**ReportHit**](reporthit-function.md) .  Os sombreadores de pressionamento de qualquer clique e mais próximo vinculados no mesmo grupo de acesso com esse sombreador de interseção devem usar a mesma estrutura para atributos de pressionamento, mesmo que os atributos não sejam referenciados.  O tamanho máximo da estrutura de atributo é 32 bytes, definido como **D3D12 \_ RAYTRACING \_ \_ tamanho máximo \_ do atributo \_ em \_ bytes**.


