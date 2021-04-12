---
description: Essa interface encapsula a funcionalidade mínima necessária de uma animação definida por um controlador de animação.
ms.assetid: vs|directx_sdk|~\id3dxanimationset.htm
title: Interface ID3DXAnimationSet (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b5aa27494931e8b6c528627fa8e96278a6d86b05
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173185"
---
# <a name="id3dxanimationset-interface"></a><span data-ttu-id="fb2fb-103">Interface ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="fb2fb-103">ID3DXAnimationSet interface</span></span>

<span data-ttu-id="fb2fb-104">Essa interface encapsula a funcionalidade mínima necessária de uma animação definida por um controlador de animação.</span><span class="sxs-lookup"><span data-stu-id="fb2fb-104">This interface encapsulates the minimum functionality required of an animation set by an animation controller.</span></span> <span data-ttu-id="fb2fb-105">Os usuários avançados podem querer implementar essa interface para atender às suas necessidades especializadas; no entanto, para a maioria dos usuários, as interfaces [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) e [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) derivadas devem ser suficientes.</span><span class="sxs-lookup"><span data-stu-id="fb2fb-105">Advanced users might want to implement this interface themselves to suit their specialized needs; for most users, however, the derived [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) and [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) interfaces should suffice.</span></span>

## <a name="members"></a><span data-ttu-id="fb2fb-106">Membros</span><span class="sxs-lookup"><span data-stu-id="fb2fb-106">Members</span></span>

<span data-ttu-id="fb2fb-107">A interface **ID3DXAnimationSet** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="fb2fb-107">The **ID3DXAnimationSet** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="fb2fb-108">**ID3DXAnimationSet** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="fb2fb-108">**ID3DXAnimationSet** also has these types of members:</span></span>

-   [<span data-ttu-id="fb2fb-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="fb2fb-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="fb2fb-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="fb2fb-110">Methods</span></span>

<span data-ttu-id="fb2fb-111">A interface **ID3DXAnimationSet** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="fb2fb-111">The **ID3DXAnimationSet** interface has these methods.</span></span>



| <span data-ttu-id="fb2fb-112">Método</span><span class="sxs-lookup"><span data-stu-id="fb2fb-112">Method</span></span>                                                                        | <span data-ttu-id="fb2fb-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="fb2fb-113">Description</span></span>                                                                       |
|:------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="fb2fb-114">**GetAnimationIndexByName**</span><span class="sxs-lookup"><span data-stu-id="fb2fb-114">**GetAnimationIndexByName**</span></span>](id3dxanimationset--getanimationindexbyname.md) | <span data-ttu-id="fb2fb-115">Obtém o índice de uma animação, dado seu nome.</span><span class="sxs-lookup"><span data-stu-id="fb2fb-115">Gets the index of an animation, given its name.</span></span><br/>                        |
| [<span data-ttu-id="fb2fb-116">**GetAnimationNameByIndex**</span><span class="sxs-lookup"><span data-stu-id="fb2fb-116">**GetAnimationNameByIndex**</span></span>](id3dxanimationset--getanimationnamebyindex.md) | <span data-ttu-id="fb2fb-117">Obtém o nome de uma animação, dado seu índice.</span><span class="sxs-lookup"><span data-stu-id="fb2fb-117">Gets the name of an animation, given its index.</span></span><br/>                        |
| [<span data-ttu-id="fb2fb-118">**Getcallback**</span><span class="sxs-lookup"><span data-stu-id="fb2fb-118">**GetCallback**</span></span>](id3dxanimationset--getcallback.md)                         | <span data-ttu-id="fb2fb-119">Obtém informações sobre um retorno de chamada específico no conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="fb2fb-119">Gets information about a specific callback in the animation set.</span></span><br/>       |
| [<span data-ttu-id="fb2fb-120">**GetName**</span><span class="sxs-lookup"><span data-stu-id="fb2fb-120">**GetName**</span></span>](id3dxanimationset--getname.md)                                 | <span data-ttu-id="fb2fb-121">Obtém o nome do conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="fb2fb-121">Gets the animation set name.</span></span><br/>                                           |
| [<span data-ttu-id="fb2fb-122">**GetNumAnimations**</span><span class="sxs-lookup"><span data-stu-id="fb2fb-122">**GetNumAnimations**</span></span>](id3dxanimationset--getnumanimations.md)               | <span data-ttu-id="fb2fb-123">Obtém o número de animações no conjunto de animação.</span><span class="sxs-lookup"><span data-stu-id="fb2fb-123">Gets the number of animations in the animation set.</span></span><br/>                    |
| [<span data-ttu-id="fb2fb-124">**Getperiod**</span><span class="sxs-lookup"><span data-stu-id="fb2fb-124">**GetPeriod**</span></span>](id3dxanimationset--getperiod.md)                             | <span data-ttu-id="fb2fb-125">Obtém o período do conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="fb2fb-125">Gets the period of the animation set.</span></span><br/>                                  |
| [<span data-ttu-id="fb2fb-126">**GetPeriodicPosition**</span><span class="sxs-lookup"><span data-stu-id="fb2fb-126">**GetPeriodicPosition**</span></span>](id3dxanimationset--getperiodicposition.md)         | <span data-ttu-id="fb2fb-127">Retorna a posição de hora no período de tempo local de um conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="fb2fb-127">Returns time position in the local timeframe of an animation set.</span></span><br/>      |
| [<span data-ttu-id="fb2fb-128">**GetSRT**</span><span class="sxs-lookup"><span data-stu-id="fb2fb-128">**GetSRT**</span></span>](id3dxanimationset--getsrt.md)                                   | <span data-ttu-id="fb2fb-129">Obtém os valores de escala, rotação e translação do conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="fb2fb-129">Gets the scale, rotation, and translation values of the animation set.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fb2fb-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="fb2fb-130">Remarks</span></span>

<span data-ttu-id="fb2fb-131">Um conjunto de animação consiste em animações para muitos nós para a mesma animação.</span><span class="sxs-lookup"><span data-stu-id="fb2fb-131">An animation set consists of animations for many nodes for the same animation.</span></span>

<span data-ttu-id="fb2fb-132">O tipo LPD3DXANIMATIONSET é definido como um ponteiro para essa interface.</span><span class="sxs-lookup"><span data-stu-id="fb2fb-132">The LPD3DXANIMATIONSET type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXAnimationSet ID3DXAnimationSet;
typedef interface ID3DXAnimationSet *LPD3DXANIMATIONSET;
```



## <a name="requirements"></a><span data-ttu-id="fb2fb-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb2fb-133">Requirements</span></span>



| <span data-ttu-id="fb2fb-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb2fb-134">Requirement</span></span> | <span data-ttu-id="fb2fb-135">Valor</span><span class="sxs-lookup"><span data-stu-id="fb2fb-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb2fb-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fb2fb-136">Header</span></span><br/>  | <dl> <span data-ttu-id="fb2fb-137"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb2fb-137"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="fb2fb-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fb2fb-138">Library</span></span><br/> | <dl> <span data-ttu-id="fb2fb-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb2fb-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fb2fb-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="fb2fb-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb2fb-141">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="fb2fb-141">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
