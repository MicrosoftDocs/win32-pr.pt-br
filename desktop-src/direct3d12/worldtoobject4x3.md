---
description: WorldToObject4x3 – uma matriz para transformar do espaço do mundo para o espaço do objeto.
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
ms.openlocfilehash: 26775e10723a768aa5b526fadfae55414dafa2311b020b1683a99e2b2139dc30
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565556"
---
# <a name="worldtoobject4x3"></a>WorldToObject4x3

Uma matriz para transformar do espaço do mundo para o espaço do objeto. O espaço do objeto refere-se ao espaço da estrutura de aceleração de nível inferior atual.

## <a name="syntax"></a>Sintaxe

```
void WorldToObject4x3();

```




## <a name="remarks"></a>Comentários

A matriz é uma transposição da **matriz WorldToObject3x4.**

Essa função pode ser chamada dos seguintes tipos de sombreador de raio:

* [**Sombreador de todos os cliques**](any-hit-shader.md)
* [**Sombreador do clique mais próximo**](closest-hit-shader.md)
* [**Sombreador de interseção**](intersection-shader.md)





## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência HLSL de raytracing do Direct3D 12](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




