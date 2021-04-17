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
# <a name="raytracingaccelerationstructure"></a><span data-ttu-id="e01a4-103">RaytracingAccelerationStructure</span><span class="sxs-lookup"><span data-stu-id="e01a4-103">RaytracingAccelerationStructure</span></span>

<span data-ttu-id="e01a4-104">Um tipo de recurso que pode ser declarado em HLSL e passado para [**TraceRay**](traceray-function.md) para indicar o recurso de aceleração de nível superior criado usando **BuildRaytracingAccelerationStructure**.</span><span class="sxs-lookup"><span data-stu-id="e01a4-104">A resource type that can be declared in HLSL and passed into [**TraceRay**](traceray-function.md) to indicate the top-level acceleration resource built using **BuildRaytracingAccelerationStructure**.</span></span> <span data-ttu-id="e01a4-105">Ele é associado como um buffer bruto do SRV em uma tabela de descritores ou um descritor de raiz SRV.</span><span class="sxs-lookup"><span data-stu-id="e01a4-105">It is bound as a raw buffer SRV in a descriptor table or root descriptor SRV.</span></span>  <span data-ttu-id="e01a4-106">A declaração em HLSL é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="e01a4-106">The declaration in HLSL is as follows:</span></span>


```
RaytracingAccelerationStructure MyScene[] : register(t3,space1);
```

<span data-ttu-id="e01a4-107">Este exemplo mostra uma matriz de tamanho não associado de estruturas de aceleração, que implica proveniente de um heap de descritor, pois os descritores de raiz não podem ser indexados.</span><span class="sxs-lookup"><span data-stu-id="e01a4-107">This example shows an unbounded size array of acceleration structures, which implies coming from a descriptor heap since root descriptors can’t be indexed.</span></span>

<span data-ttu-id="e01a4-108">**RaytracingAccelerationStructure** é um recurso opaco sem métodos disponíveis para sombreadores.</span><span class="sxs-lookup"><span data-stu-id="e01a4-108">**RaytracingAccelerationStructure** is an opaque resource with no methods available to shaders.</span></span>


 

 




