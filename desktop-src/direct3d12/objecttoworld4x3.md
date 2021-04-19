---
description: Uma matriz para transformar de espaço de objeto em espaço mundial.
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
ms.openlocfilehash: 613b4c403f235819845114e7019e07051a25ec80
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105807977"
---
# <a name="objecttoworld4x3"></a><span data-ttu-id="9b001-103">ObjectToWorld4x3</span><span class="sxs-lookup"><span data-stu-id="9b001-103">ObjectToWorld4x3</span></span>

<span data-ttu-id="9b001-104">Uma matriz para transformar de espaço de objeto em espaço mundial.</span><span class="sxs-lookup"><span data-stu-id="9b001-104">A matrix for transforming from object-space to world-space.</span></span> <span data-ttu-id="9b001-105">Objeto-espaço refere-se ao espaço da estrutura de aceleração de nível inferior atual.</span><span class="sxs-lookup"><span data-stu-id="9b001-105">Object-space refers to the space of the current bottom-level acceleration structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b001-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9b001-106">Syntax</span></span>

```
void ObjectToWorld4x3();

```




## <a name="remarks"></a><span data-ttu-id="9b001-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="9b001-107">Remarks</span></span>

<span data-ttu-id="9b001-108">A matriz é uma transposição da matriz **ObjectToWorld3x4** .</span><span class="sxs-lookup"><span data-stu-id="9b001-108">The matrix is a transposition of **ObjectToWorld3x4** matrix.</span></span>

<span data-ttu-id="9b001-109">Essa função pode ser chamada nos seguintes tipos de sombreador raytracing:</span><span class="sxs-lookup"><span data-stu-id="9b001-109">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="9b001-110">**Sombreador de todos os cliques**</span><span class="sxs-lookup"><span data-stu-id="9b001-110">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="9b001-111">**Sombreador do clique mais próximo**</span><span class="sxs-lookup"><span data-stu-id="9b001-111">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="9b001-112">**Sombreador de interseção**</span><span class="sxs-lookup"><span data-stu-id="9b001-112">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="9b001-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="9b001-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b001-114">Referência HLSL de raytracing do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="9b001-114">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




