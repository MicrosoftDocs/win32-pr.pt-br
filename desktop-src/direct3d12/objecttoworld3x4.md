---
description: ObjectToWorld3x4 – uma matriz para transformar de espaço de objeto em espaço mundial.
ms.assetid: ''
title: ObjectToWorld3x4
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObjectToWorld3x4
api_type:
- NA
ms.openlocfilehash: 947676c25bd5cac50749c737afd7e4ff75426c0a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107734"
---
# <a name="objecttoworld3x4"></a><span data-ttu-id="0bcc9-103">ObjectToWorld3x4</span><span class="sxs-lookup"><span data-stu-id="0bcc9-103">ObjectToWorld3x4</span></span>

<span data-ttu-id="0bcc9-104">Uma matriz para transformar de espaço de objeto em espaço mundial.</span><span class="sxs-lookup"><span data-stu-id="0bcc9-104">A matrix for transforming from object-space to world-space.</span></span> <span data-ttu-id="0bcc9-105">Objeto-espaço refere-se ao espaço da estrutura de aceleração de nível inferior atual.</span><span class="sxs-lookup"><span data-stu-id="0bcc9-105">Object-space refers to the space of the current bottom-level acceleration structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bcc9-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0bcc9-106">Syntax</span></span>

```
void ObjectToWorld3x4();

```




## <a name="remarks"></a><span data-ttu-id="0bcc9-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="0bcc9-107">Remarks</span></span>

<span data-ttu-id="0bcc9-108">A matriz é uma transposição da matriz **ObjectToWorld4x3** .</span><span class="sxs-lookup"><span data-stu-id="0bcc9-108">The matrix is a transposition of **ObjectToWorld4x3** matrix.</span></span>

<span data-ttu-id="0bcc9-109">Essa função pode ser chamada nos seguintes tipos de sombreador raytracing:</span><span class="sxs-lookup"><span data-stu-id="0bcc9-109">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="0bcc9-110">**Sombreador de todos os cliques**</span><span class="sxs-lookup"><span data-stu-id="0bcc9-110">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="0bcc9-111">**Sombreador do clique mais próximo**</span><span class="sxs-lookup"><span data-stu-id="0bcc9-111">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="0bcc9-112">**Sombreador de interseção**</span><span class="sxs-lookup"><span data-stu-id="0bcc9-112">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="0bcc9-113">Consulte também</span><span class="sxs-lookup"><span data-stu-id="0bcc9-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bcc9-114">Referência HLSL de raytracing do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="0bcc9-114">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




