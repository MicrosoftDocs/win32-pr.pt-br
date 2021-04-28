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
# <a name="worldtoobject4x3"></a><span data-ttu-id="9dce6-103">WorldToObject4x3</span><span class="sxs-lookup"><span data-stu-id="9dce6-103">WorldToObject4x3</span></span>

<span data-ttu-id="9dce6-104">Uma matriz para transformar de espaço mundial em espaço de objeto.</span><span class="sxs-lookup"><span data-stu-id="9dce6-104">A matrix for transforming from world-space to object-space.</span></span> <span data-ttu-id="9dce6-105">Objeto-espaço refere-se ao espaço da estrutura de aceleração de nível inferior atual.</span><span class="sxs-lookup"><span data-stu-id="9dce6-105">Object-space refers to the space of the current bottom-level acceleration structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="9dce6-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9dce6-106">Syntax</span></span>

```
void WorldToObject4x3();

```




## <a name="remarks"></a><span data-ttu-id="9dce6-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="9dce6-107">Remarks</span></span>

<span data-ttu-id="9dce6-108">A matriz é uma transposição da matriz **WorldToObject3x4** .</span><span class="sxs-lookup"><span data-stu-id="9dce6-108">The matrix is a transposition of **WorldToObject3x4** matrix.</span></span>

<span data-ttu-id="9dce6-109">Essa função pode ser chamada nos seguintes tipos de sombreador raytracing:</span><span class="sxs-lookup"><span data-stu-id="9dce6-109">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="9dce6-110">**Sombreador de todos os cliques**</span><span class="sxs-lookup"><span data-stu-id="9dce6-110">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="9dce6-111">**Sombreador do clique mais próximo**</span><span class="sxs-lookup"><span data-stu-id="9dce6-111">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="9dce6-112">**Sombreador de interseção**</span><span class="sxs-lookup"><span data-stu-id="9dce6-112">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="9dce6-113">Consulte também</span><span class="sxs-lookup"><span data-stu-id="9dce6-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dce6-114">Referência HLSL de raytracing do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="9dce6-114">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




