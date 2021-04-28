---
description: WorldToObject4x3 – uma matriz para transformar de espaço mundial em espaço de objeto.
ms.assetid: ''
title: WorldToObject4x3
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WorldToObject4x3
api_type:
- NA
ms.openlocfilehash: 334a79352345fb35fbbafe68248a221bdaab9f6d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105239"
---
# <a name="worldtoobject4x3"></a>WorldToObject4x3

Uma matriz para transformar de espaço mundial em espaço de objeto. Objeto-espaço refere-se ao espaço da estrutura de aceleração de nível inferior atual.

## <a name="syntax"></a>Sintaxe

```
void WorldToObject4x3();

```




## <a name="remarks"></a>Comentários

A matriz é uma transposição da matriz **WorldToObject3x4** .

Essa função pode ser chamada nos seguintes tipos de sombreador raytracing:

* [**Sombreador de todos os cliques**](any-hit-shader.md)
* [**Sombreador do clique mais próximo**](closest-hit-shader.md)
* [**Sombreador de interseção**](intersection-shader.md)





## <a name="see-also"></a>Consulte também

<dl> <dt>

[Referência HLSL de raytracing do Direct3D 12](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




