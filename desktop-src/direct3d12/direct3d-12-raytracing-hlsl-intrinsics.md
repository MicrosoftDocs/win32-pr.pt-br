---
title: Intrínsecos HLSL de raytracing do Direct3D 12
description: Veja links para artigos que descrevem funções intrínsecas de HLSL (linguagem de sombreador de alto nível) que suportam o pipeline de raytracing do Direct3D 12.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ce12f90233dee05bb4959498d3cb366aa88f1140182384bc26f5b017ee2bf64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117733779"
---
# <a name="raytracing-hlsl-intrinsics"></a>Raytracing HLSL Intrinsics

As funções intrínteses HLSL a seguir são suportadas pelo pipeline de raytracing do Direct3D 12. 

## <a name="in-this-section"></a>Nesta seção



| Tópico | Descrição |
|-|-|
| [**Função AcceptHitAndEndSearch**](accepthitandendsearch-function.md) | Usado em qualquer sombreador de acerto para fazer commit do hit atual e, em seguida, parar de procurar mais acertos para o raio. |
| [**Função CallShader**](callshader-function.md) | Invoca outro sombreador de dentro de um sombreador. |
| [**Função IgnoreHit**](ignorehit-function.md) | Chamado de um sombreador de qualquer hit para rejeitar o hit e encerrar o sombreador. |
| [**Função PrimitiveIndex**](primitiveindex.md) | Recupera o índice gerado automaticamente do primitivo dentro da geometria dentro da instância da estrutura de aceleração de nível inferior. |
| [**Função ReportHit**](reporthit-function.md) | Chamado por um sombreador de interseção para relatar uma interseção de raio. |
| [**Função TraceRay**](traceray-function.md) | Envia um raio para uma pesquisa de acertos em uma estrutura de aceleração. |

## <a name="related-topics"></a>Tópicos relacionados

* [Referência principal](direct3d-12-core-reference.md)
* [Referência do Direct3D 12](direct3d-12-reference.md)
