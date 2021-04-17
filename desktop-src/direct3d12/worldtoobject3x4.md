---
description: Uma matriz para transformar de espaço mundial em espaço de objeto.
ms.assetid: ''
title: WorldToObject3x4
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WorldToObject3x4
api_type:
- NA
ms.openlocfilehash: 6274b1d4d18aff0464d933c20f7b8052f3389e5f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782284"
---
# <a name="worldtoobject3x4"></a>WorldToObject3x4

Uma matriz para transformar de espaço mundial em espaço de objeto. Objeto-espaço refere-se ao espaço da estrutura de aceleração de nível inferior atual.

## <a name="syntax"></a>Sintaxe

```
void WorldToObject3x4();

```




## <a name="remarks"></a>Comentários

A matriz é uma transposição da matriz **WorldToObject4x3** .

Essa função pode ser chamada nos seguintes tipos de sombreador raytracing:

* [**Sombreador de todos os cliques**](any-hit-shader.md)
* [**Sombreador do clique mais próximo**](closest-hit-shader.md)
* [**Sombreador de interseção**](intersection-shader.md)





## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência HLSL de raytracing do Direct3D 12](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




