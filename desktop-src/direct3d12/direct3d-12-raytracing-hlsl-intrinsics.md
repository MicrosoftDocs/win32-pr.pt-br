---
title: Intrínsecos HLSL de raytracing do Direct3D 12
description: Os seguintes sombreadores HLSL dão suporte ao pipeline do Direct3D 12 raytracing.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b2e7cc7053705bd66b37d91f3ee06a6a1f249a2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105789395"
---
# <a name="raytracing-hlsl-intrinsics"></a>Raytracing HLSL intrínsecos

As seguintes funções do HLSL intrinisc dão suporte ao pipeline do Direct3D 12 raytracing. 

## <a name="in-this-section"></a>Nesta seção



| Tópico | Descrição |
|-|-|
| [**Função AcceptHitAndEndSearch**](accepthitandendsearch-function.md) | Usado em um sombreador qualquer ocorrência para confirmar a ocorrência atual e, em seguida, parar de Pesquisar mais ocorrências para Ray. |
| [**Função CallShader**](callshader-function.md) | Invoca outro sombreador de dentro de um sombreador. |
| [**Função IgnoreHit**](ignorehit-function.md) | Chamado de um sombreador qualquer clique para rejeitar o erro e encerrar o sombreador. |
| [**Função PrimitiveIndex**](primitiveindex.md) | Recupera o índice gerado automaticamente do primitivo dentro da geometria dentro da instância de estrutura de aceleração de nível inferior. |
| [**Função ReportHit**](reporthit-function.md) | Chamado por um sombreador de interseção para relatar uma interseção de Ray. |
| [**Função TraceRay**](traceray-function.md) | Envia um raio para uma pesquisa de ocorrências em uma estrutura de aceleração. |

## <a name="related-topics"></a>Tópicos relacionados

* [Referência principal](direct3d-12-core-reference.md)
* [Referência do Direct3D 12](direct3d-12-reference.md)
