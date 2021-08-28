---
title: RaytracingAccelerationStructure
description: Um tipo de recurso que pode ser declarado em HLSL e passado para TraceRay para indicar o recurso de aceleração de nível superior criado usando BuildRaytracingAccelerationStructure.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: language-reference
ms.date: 05/31/2018
ms.openlocfilehash: 4728e167fe9fbc353c51accaa92d9b9d4086a0bfff3f098f43b93523cd63a792
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123614"
---
# <a name="raytracingaccelerationstructure"></a>RaytracingAccelerationStructure

Um tipo de recurso que pode ser declarado em HLSL e passado para [**TraceRay**](traceray-function.md) para indicar o recurso de aceleração de nível superior criado usando **BuildRaytracingAccelerationStructure**. Ele é vinculado como um SRV de buffer bruto em uma tabela de descritor ou SRV de descritor raiz.  A declaração em HLSL é a seguinte:


```
RaytracingAccelerationStructure MyScene[] : register(t3,space1);
```

Este exemplo mostra uma matriz de tamanho não limitada de estruturas de aceleração, o que implica em vir de um heap de descritor, pois os descritores raiz não podem ser indexados.

**RaytracingAccelerationStructure** é um recurso opaco sem métodos disponíveis para sombreadores.


 

 




