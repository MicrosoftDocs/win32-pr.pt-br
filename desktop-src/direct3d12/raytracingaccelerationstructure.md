---
title: RaytracingAccelerationStructure
description: Um tipo de recurso que pode ser declarado em HLSL e passado para TraceRay para indicar o recurso de aceleração de nível superior criado usando BuildRaytracingAccelerationStructure.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: language-reference
ms.date: 05/31/2018
ms.openlocfilehash: beb6f5e397126223e9c0e6959e16a6cca3145517
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/12/2021
ms.locfileid: "105765675"
---
# <a name="raytracingaccelerationstructure"></a>RaytracingAccelerationStructure

Um tipo de recurso que pode ser declarado em HLSL e passado para [**TraceRay**](traceray-function.md) para indicar o recurso de aceleração de nível superior criado usando **BuildRaytracingAccelerationStructure**. Ele é associado como um buffer bruto do SRV em uma tabela de descritores ou um descritor de raiz SRV.  A declaração em HLSL é a seguinte:


```
RaytracingAccelerationStructure MyScene[] : register(t3,space1);
```

Este exemplo mostra uma matriz de tamanho não associado de estruturas de aceleração, que implica proveniente de um heap de descritor, pois os descritores de raiz não podem ser indexados.

**RaytracingAccelerationStructure** é um recurso opaco sem métodos disponíveis para sombreadores.


 

 




