---
description: Recupera o índice gerado automaticamente do primitivo dentro da geometria dentro da instância de estrutura de aceleração de nível inferior.
ms.assetid: ''
title: PrimitiveIndex
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrimitiveIndex
api_type:
- NA
ms.openlocfilehash: d6d1e8ba338a3fb567b583b42074210b514ef360
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765207"
---
# <a name="primitiveindex-function"></a>Função PrimitiveIndex

Recupera o índice gerado automaticamente do primitivo dentro da geometria dentro da instância de estrutura de aceleração de nível inferior.

## <a name="syntax"></a>Sintaxe

```
uint PrimitiveIndex();
```

## <a name="remarks"></a>Comentários

Para **\_ \_ \_ \_ triângulos de tipo de geometria D3D12 RAYTRACING**, este é o índice de triângulo dentro do objeto Geometry.

Para **D3D12 \_ RAYTRACING \_ de \_ procedimento do tipo geometry \_ \_ \_ AABBS primitivo**, esse é o índice na matriz AABB que define o objeto Geometry.

Essa função pode ser chamada nos seguintes tipos de sombreador raytracing:

* [**Sombreador de todos os cliques**](any-hit-shader.md)
* [**Sombreador do clique mais próximo**](closest-hit-shader.md)
* [**Sombreador de interseção**](intersection-shader.md)

## <a name="see-also"></a>Confira também

* [Referência HLSL de raytracing do Direct3D 12](direct3d-12-raytracing-hlsl-reference.md)
