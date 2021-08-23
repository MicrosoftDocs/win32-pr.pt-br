---
description: ObjectToWorld4x3 – uma matriz para transformar do espaço do objeto para o espaço do mundo.
ms.assetid: ''
title: ObjectToWorld4x3
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObjectToWorld4x3
api_type:
- NA
ms.openlocfilehash: 22ad7bfafae89e33001d1d72878bc268ebfbd44649176b118a447fa16cf97d76
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608266"
---
# <a name="objecttoworld4x3"></a>ObjectToWorld4x3

Uma matriz para transformar do espaço do objeto para o espaço do mundo. O espaço do objeto refere-se ao espaço da estrutura de aceleração de nível inferior atual.

## <a name="syntax"></a>Sintaxe

```
void ObjectToWorld4x3();

```




## <a name="remarks"></a>Comentários

A matriz é uma transposição da **matriz ObjectToWorld3x4.**

Essa função pode ser chamada dos seguintes tipos de sombreador de raio:

* [**Sombreador de todos os cliques**](any-hit-shader.md)
* [**Sombreador do clique mais próximo**](closest-hit-shader.md)
* [**Sombreador de interseção**](intersection-shader.md)





## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência HLSL de raytracing do Direct3D 12](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




