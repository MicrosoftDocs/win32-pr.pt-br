---
description: A direção do espaço de objeto para o raio atual.
ms.assetid: ''
title: ObjectRayDirection
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObjectRayDirection
api_type:
- NA
ms.openlocfilehash: 1cc291a33f91bf7fc0565596bdd075a86e193246
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765317"
---
# <a name="objectraydirection"></a><span data-ttu-id="9dac5-103">ObjectRayDirection</span><span class="sxs-lookup"><span data-stu-id="9dac5-103">ObjectRayDirection</span></span>

<span data-ttu-id="9dac5-104">A direção do espaço de objeto para o raio atual.</span><span class="sxs-lookup"><span data-stu-id="9dac5-104">The object-space direction for the current ray.</span></span> <span data-ttu-id="9dac5-105">Objeto-espaço refere-se ao espaço da estrutura de aceleração de nível inferior atual.</span><span class="sxs-lookup"><span data-stu-id="9dac5-105">Object-space refers to the space of the current bottom-level acceleration structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="9dac5-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9dac5-106">Syntax</span></span>

```
float3 ObjectRayDirection();

```



## <a name="remarks"></a><span data-ttu-id="9dac5-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="9dac5-107">Remarks</span></span>

<span data-ttu-id="9dac5-108">Essa função pode ser chamada nos seguintes tipos de sombreador raytracing:</span><span class="sxs-lookup"><span data-stu-id="9dac5-108">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="9dac5-109">**Sombreador de todos os cliques**</span><span class="sxs-lookup"><span data-stu-id="9dac5-109">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="9dac5-110">**Sombreador do clique mais próximo**</span><span class="sxs-lookup"><span data-stu-id="9dac5-110">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="9dac5-111">**Sombreador de interseção**</span><span class="sxs-lookup"><span data-stu-id="9dac5-111">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="9dac5-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="9dac5-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dac5-113">Referência HLSL de raytracing do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="9dac5-113">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




