---
title: Funções de transformação de vetor 3D DirectXMath
description: Lista as funções de transformação de vetor 3D.
ms.assetid: 148972da-e460-63b9-6b01-10201f63d157
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a592071970d69d7ef4b4db42960335c5fc771ac3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105772519"
---
# <a name="directxmath-3d-vector-transformation-functions"></a><span data-ttu-id="11a67-103">Funções de transformação de vetor 3D DirectXMath</span><span class="sxs-lookup"><span data-stu-id="11a67-103">DirectXMath 3D vector transformation functions</span></span>

<span data-ttu-id="11a67-104">Lista as funções de transformação de vetor 3D.</span><span class="sxs-lookup"><span data-stu-id="11a67-104">Lists the 3D vector transformation functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="11a67-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="11a67-105">In this section</span></span>



| <span data-ttu-id="11a67-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="11a67-106">Topic</span></span>                                                                               | <span data-ttu-id="11a67-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="11a67-107">Description</span></span>                                                                                                                                      |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="11a67-108">**XMVector3InverseRotate**</span><span class="sxs-lookup"><span data-stu-id="11a67-108">**XMVector3InverseRotate**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3inverserotate)<br/>                 | <span data-ttu-id="11a67-109">Gira um vetor 3D usando o inverso de um Quaternion.</span><span class="sxs-lookup"><span data-stu-id="11a67-109">Rotates a 3D vector using the inverse of a quaternion.</span></span><br/>                                                                                |
| [<span data-ttu-id="11a67-110">**XMVector3Project**</span><span class="sxs-lookup"><span data-stu-id="11a67-110">**XMVector3Project**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3project)<br/>                             | <span data-ttu-id="11a67-111">Projetar um vetor 3D do espaço do objeto no espaço da tela.</span><span class="sxs-lookup"><span data-stu-id="11a67-111">Project a 3D vector from object space into screen space.</span></span><br/>                                                                              |
| [<span data-ttu-id="11a67-112">**XMVector3ProjectStream**</span><span class="sxs-lookup"><span data-stu-id="11a67-112">**XMVector3ProjectStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3projectstream)<br/>                 | <span data-ttu-id="11a67-113">Projeta um fluxo de vetores 3D do espaço do objeto no espaço da tela.</span><span class="sxs-lookup"><span data-stu-id="11a67-113">Projects a stream of 3D vectors from object space into screen space.</span></span><br/>                                                                  |
| [<span data-ttu-id="11a67-114">**XMVector3Rotate**</span><span class="sxs-lookup"><span data-stu-id="11a67-114">**XMVector3Rotate**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3rotate)<br/>                               | <span data-ttu-id="11a67-115">Gira um vetor 3D usando um Quaternion.</span><span class="sxs-lookup"><span data-stu-id="11a67-115">Rotates a 3D vector using a quaternion.</span></span><br/>                                                                                               |
| [<span data-ttu-id="11a67-116">**XMVector3Transform**</span><span class="sxs-lookup"><span data-stu-id="11a67-116">**XMVector3Transform**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3transform)<br/>                         | <span data-ttu-id="11a67-117">Transforma um vetor 3D por uma matriz.</span><span class="sxs-lookup"><span data-stu-id="11a67-117">Transforms a 3D vector by a matrix.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="11a67-118">**XMVector3TransformCoord**</span><span class="sxs-lookup"><span data-stu-id="11a67-118">**XMVector3TransformCoord**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformcoord)<br/>               | <span data-ttu-id="11a67-119">Transforma um vetor 3D por uma determinada matriz, projetando o resultado de volta em w = 1.</span><span class="sxs-lookup"><span data-stu-id="11a67-119">Transforms a 3D vector by a given matrix, projecting the result back into w = 1.</span></span><br/>                                                      |
| [<span data-ttu-id="11a67-120">**XMVector3TransformCoordStream**</span><span class="sxs-lookup"><span data-stu-id="11a67-120">**XMVector3TransformCoordStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformcoordstream)<br/>   | <span data-ttu-id="11a67-121">Transforma um fluxo de vetores 3D por uma determinada matriz, projetando os vetores resultantes, de modo que suas coordenadas w sejam iguais a 1,0.</span><span class="sxs-lookup"><span data-stu-id="11a67-121">Transforms a stream of 3D vectors by a given matrix, projecting the resulting vectors such that their w coordinates are equal to 1.0.</span></span><br/> |
| [<span data-ttu-id="11a67-122">**XMVector3TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="11a67-122">**XMVector3TransformNormal**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformnormal)<br/>             | <span data-ttu-id="11a67-123">Transforma o vetor 3D normal pela matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="11a67-123">Transforms the 3D vector normal by the given matrix.</span></span><br/>                                                                                  |
| [<span data-ttu-id="11a67-124">**XMVector3TransformNormalStream**</span><span class="sxs-lookup"><span data-stu-id="11a67-124">**XMVector3TransformNormalStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformnormalstream)<br/> | <span data-ttu-id="11a67-125">Transforma um fluxo de vetores normais 3D por uma determinada matriz.</span><span class="sxs-lookup"><span data-stu-id="11a67-125">Transforms a stream of 3D normal vectors by a given matrix.</span></span><br/>                                                                           |
| [<span data-ttu-id="11a67-126">**XMVector3TransformStream**</span><span class="sxs-lookup"><span data-stu-id="11a67-126">**XMVector3TransformStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream)<br/>             | <span data-ttu-id="11a67-127">Transforma um fluxo de vetores 3D por uma determinada matriz.</span><span class="sxs-lookup"><span data-stu-id="11a67-127">Transforms a stream of 3D vectors by a given matrix.</span></span><br/>                                                                                  |
| [<span data-ttu-id="11a67-128">**XMVector3Unproject**</span><span class="sxs-lookup"><span data-stu-id="11a67-128">**XMVector3Unproject**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3unproject)<br/>                         | <span data-ttu-id="11a67-129">Projeta um vetor 3D do espaço da tela no espaço do objeto.</span><span class="sxs-lookup"><span data-stu-id="11a67-129">Projects a 3D vector from screen space into object space.</span></span><br/>                                                                             |
| [<span data-ttu-id="11a67-130">**XMVector3UnprojectStream**</span><span class="sxs-lookup"><span data-stu-id="11a67-130">**XMVector3UnprojectStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3unprojectstream)<br/>             | <span data-ttu-id="11a67-131">Transforma um fluxo de vetores 3D do espaço da tela para o espaço do objeto.</span><span class="sxs-lookup"><span data-stu-id="11a67-131">Transforms a stream of 3D vectors from screen space to object space.</span></span><br/>                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="11a67-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="11a67-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11a67-133">Funções de vetor 3D da biblioteca DirectXMath</span><span class="sxs-lookup"><span data-stu-id="11a67-133">DirectXMath Library 3D Vector Functions</span></span>](ovw-xnamath-reference-functions-vector3.md)
</dt> </dl>

 

 
