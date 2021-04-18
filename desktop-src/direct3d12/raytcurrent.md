---
description: Um float que representa o ponto final paramétrica atual para o raio.
ms.assetid: ''
title: RayTCurrent
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RayTCurrent
api_type:
- NA
ms.openlocfilehash: 4f090bab88c6be671ca0614255fd7bdebb0d1549
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793232"
---
# <a name="raytcurrent"></a>RayTCurrent

Um float que representa o ponto final paramétrica atual para o raio.  

## <a name="syntax"></a>Sintaxe

```
float RayTCurrent();

```


## <a name="remarks"></a>Comentários

**RayTCurrent** define o ponto final atual do raio de acordo com a seguinte fórmula: origem + (direção * RayTCurrent).  A *origem* e a *direção* podem estar no espaço do mundo ou do objeto, o que resulta em um ponto de extremidade de espaço de objeto ou em um mundo.

**RayTCurrent** é inicializado na chamada Call [**TraceRay**](traceray-function.md) com o valor [**RayDesc:: tmax**](raydesc.md) e, em seguida, é atualizado durante a consulta de rastreamento, pois as interseções são relatadas (em qualquer um deles) e aceitas.

No [sombreador de interseção](intersection-shader.md), ele representa a distância para a interseção mais próxima encontrada até o momento.  Ele será atualizado após () para o valor de THit fornecido se o pressionamento tiver sido aceito.

No [sombreador qualquer clique](any-hit-shader.md), ele representa a distância para a interseção atual que está sendo relatada.

No [sombreador de clique mais próximo](closest-hit-shader.md), ele representa a distância para a interseção mais próxima aceita.

No [sombreador ausente](miss-shader.md), é igual a *tmax* passado para a chamada **TraceRay** .


Essa função pode ser chamada nos seguintes tipos de sombreador raytracing:

* [**Sombreador de todos os cliques**](any-hit-shader.md)
* [**Sombreador do clique mais próximo**](closest-hit-shader.md)
* [**Sombreador de interseção**](intersection-shader.md)
* [**Sombreador de resolução**](miss-shader.md)





## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência HLSL de raytracing do Direct3D 12](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




