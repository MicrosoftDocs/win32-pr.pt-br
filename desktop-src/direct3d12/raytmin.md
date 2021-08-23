---
description: Um float que representa o ponto de partida paramétrico atual para o raio.
ms.assetid: ''
title: RayTMin
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RayTMin
api_type:
- NA
ms.openlocfilehash: 5429574480cfda071dfec93cea771211bab578bdaecb4513c76f43c4d820b22b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989476"
---
# <a name="raytmin"></a>RayTMin

Um float que representa o ponto de partida paramétrico atual para o raio. 

## <a name="syntax"></a>Sintaxe

```
float RayTMin();

```

## <a name="remarks"></a>Comentários

**RayTMin** define o ponto de partida do raio de acordo com a seguinte fórmula: Origin + (Direction * RayTMin).  *Origin* e *Direction* podem estar no mundo ou no espaço do objeto, o que resulta em um mundo ou um ponto de partida do espaço de objeto.

**RayTMin** é especificado na chamada para [**TraceRay**](traceray-function.md)e é constante durante essa chamada.




Essa função pode ser chamada dos seguintes tipos de sombreador de raio:

* [**Sombreador de todos os cliques**](any-hit-shader.md)
* [**Sombreador do clique mais próximo**](closest-hit-shader.md)
* [**Sombreador de interseção**](intersection-shader.md)
* [**Sombreador de resolução**](miss-shader.md)





## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência HLSL de raytracing do Direct3D 12](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




