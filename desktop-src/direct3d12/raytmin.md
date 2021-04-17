---
description: Um float que representa o ponto de partida paramétrica atual para o raio.
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
ms.openlocfilehash: 00db0eb46e8c011e5b31f773679e19ca6dd4a7a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762354"
---
# <a name="raytmin"></a>RayTMin

Um float que representa o ponto de partida paramétrica atual para o raio. 

## <a name="syntax"></a>Sintaxe

```
float RayTMin();

```

## <a name="remarks"></a>Comentários

**RayTMin** define o ponto de partida do raio de acordo com a seguinte fórmula: origem + (direção * RayTMin).  A *origem* e a *direção* podem estar no espaço do mundo ou do objeto, o que resulta em um ponto de partida do mundo ou do espaço de objeto.

**RayTMin** é especificado na chamada para [**TraceRay**](traceray-function.md)e é constante para a duração dessa chamada.




Essa função pode ser chamada nos seguintes tipos de sombreador raytracing:

* [**Sombreador de todos os cliques**](any-hit-shader.md)
* [**Sombreador do clique mais próximo**](closest-hit-shader.md)
* [**Sombreador de interseção**](intersection-shader.md)
* [**Sombreador de resolução**](miss-shader.md)





## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência HLSL de raytracing do Direct3D 12](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




