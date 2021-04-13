---
description: Os aplicativos usam os métodos da interface ID3DXMATRIXStack para manipular uma pilha de matriz.
ms.assetid: 6c76f9e0-5f59-4cf3-b34a-2475536af6c7
title: Interface ID3DXMatrixStack (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMatrixStack
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3d6956a6764683378c732c4ed859bfa13e537422
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298777"
---
# <a name="id3dxmatrixstack-interface"></a><span data-ttu-id="67baa-103">Interface ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="67baa-103">ID3DXMatrixStack interface</span></span>

<span data-ttu-id="67baa-104">Os aplicativos usam os métodos da interface ID3DXMATRIXStack para manipular uma pilha de matriz.</span><span class="sxs-lookup"><span data-stu-id="67baa-104">Applications use the methods of the ID3DXMATRIXStack interface to manipulate a matrix stack.</span></span>

## <a name="members"></a><span data-ttu-id="67baa-105">Membros</span><span class="sxs-lookup"><span data-stu-id="67baa-105">Members</span></span>

<span data-ttu-id="67baa-106">A interface **ID3DXMatrixStack** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="67baa-106">The **ID3DXMatrixStack** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="67baa-107">**ID3DXMatrixStack** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="67baa-107">**ID3DXMatrixStack** also has these types of members:</span></span>

-   [<span data-ttu-id="67baa-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="67baa-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="67baa-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="67baa-109">Methods</span></span>

<span data-ttu-id="67baa-110">A interface **ID3DXMatrixStack** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="67baa-110">The **ID3DXMatrixStack** interface has these methods.</span></span>



| <span data-ttu-id="67baa-111">Método</span><span class="sxs-lookup"><span data-stu-id="67baa-111">Method</span></span>                                                                      | <span data-ttu-id="67baa-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="67baa-112">Description</span></span>                                                                                                                                |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="67baa-113">**GetTop**</span><span class="sxs-lookup"><span data-stu-id="67baa-113">**GetTop**</span></span>](id3dxmatrixstack-gettop.md)                                   | <span data-ttu-id="67baa-114">Recupera a matriz atual na parte superior da pilha.</span><span class="sxs-lookup"><span data-stu-id="67baa-114">Retrieves the current matrix at the top of the stack.</span></span><br/>                                                                           |
| [<span data-ttu-id="67baa-115">**Loadidentity**</span><span class="sxs-lookup"><span data-stu-id="67baa-115">**LoadIdentity**</span></span>](id3dxmatrixstack-loadidentity.md)                       | <span data-ttu-id="67baa-116">Carrega a identidade na matriz atual.</span><span class="sxs-lookup"><span data-stu-id="67baa-116">Loads identity in the current matrix.</span></span><br/>                                                                                           |
| [<span data-ttu-id="67baa-117">**Loadmatrix**</span><span class="sxs-lookup"><span data-stu-id="67baa-117">**LoadMatrix**</span></span>](id3dxmatrixstack-loadmatrix.md)                           | <span data-ttu-id="67baa-118">Carrega a matriz determinada na matriz atual.</span><span class="sxs-lookup"><span data-stu-id="67baa-118">Loads the given matrix into the current matrix.</span></span><br/>                                                                                 |
| [<span data-ttu-id="67baa-119">**MultMatrix**</span><span class="sxs-lookup"><span data-stu-id="67baa-119">**MultMatrix**</span></span>](id3dxmatrixstack-multmatrix.md)                           | <span data-ttu-id="67baa-120">Determina o produto da matriz atual e a matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="67baa-120">Determines the product of the current matrix and the given matrix.</span></span><br/>                                                              |
| [<span data-ttu-id="67baa-121">**MultMatrixLocal**</span><span class="sxs-lookup"><span data-stu-id="67baa-121">**MultMatrixLocal**</span></span>](id3dxmatrixstack-multmatrixlocal.md)                 | <span data-ttu-id="67baa-122">Determina o produto da matriz e da matriz atual.</span><span class="sxs-lookup"><span data-stu-id="67baa-122">Determines the product of the given matrix and the current matrix.</span></span><br/>                                                              |
| [<span data-ttu-id="67baa-123">**Pop**</span><span class="sxs-lookup"><span data-stu-id="67baa-123">**Pop**</span></span>](id3dxmatrixstack-pop.md)                                         | <span data-ttu-id="67baa-124">Remove a matriz atual da parte superior da pilha.</span><span class="sxs-lookup"><span data-stu-id="67baa-124">Removes the current matrix from the top of the stack.</span></span><br/>                                                                           |
| [<span data-ttu-id="67baa-125">**Push**</span><span class="sxs-lookup"><span data-stu-id="67baa-125">**Push**</span></span>](id3dxmatrixstack-push.md)                                       | <span data-ttu-id="67baa-126">Adiciona uma matriz à pilha.</span><span class="sxs-lookup"><span data-stu-id="67baa-126">Adds a matrix to the stack.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="67baa-127">**RotateAxis**</span><span class="sxs-lookup"><span data-stu-id="67baa-127">**RotateAxis**</span></span>](id3dxmatrixstack-rotateaxis.md)                           | <span data-ttu-id="67baa-128">Gira (em relação ao espaço de coordenadas mundiais) em um eixo arbitrário.</span><span class="sxs-lookup"><span data-stu-id="67baa-128">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span><br/>                                                          |
| [<span data-ttu-id="67baa-129">**RotateAxisLocal**</span><span class="sxs-lookup"><span data-stu-id="67baa-129">**RotateAxisLocal**</span></span>](id3dxmatrixstack-rotateaxislocal.md)                 | <span data-ttu-id="67baa-130">Gira (em relação ao espaço de coordenadas local do objeto) em um eixo arbitrário.</span><span class="sxs-lookup"><span data-stu-id="67baa-130">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span><br/>                                             |
| [<span data-ttu-id="67baa-131">**RotateYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="67baa-131">**RotateYawPitchRoll**</span></span>](id3dxmatrixstack-rotateyawpitchroll.md)           | <span data-ttu-id="67baa-132">Gira (em relação ao espaço de coordenadas mundiais) em um eixo arbitrário.</span><span class="sxs-lookup"><span data-stu-id="67baa-132">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span><br/>                                                          |
| [<span data-ttu-id="67baa-133">**RotateYawPitchRollLocal**</span><span class="sxs-lookup"><span data-stu-id="67baa-133">**RotateYawPitchRollLocal**</span></span>](id3dxmatrixstack-rotateyawpitchrolllocal.md) | <span data-ttu-id="67baa-134">Gira (em relação ao espaço de coordenadas local do objeto) em um eixo arbitrário.</span><span class="sxs-lookup"><span data-stu-id="67baa-134">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span><br/>                                             |
| [<span data-ttu-id="67baa-135">**Escalonáve**</span><span class="sxs-lookup"><span data-stu-id="67baa-135">**Scale**</span></span>](id3dxmatrixstack-scale.md)                                     | <span data-ttu-id="67baa-136">Dimensione a matriz atual sobre a origem da coordenada mundial.</span><span class="sxs-lookup"><span data-stu-id="67baa-136">Scale the current matrix about the world coordinate origin.</span></span><br/>                                                                     |
| [<span data-ttu-id="67baa-137">**ScaleLocal**</span><span class="sxs-lookup"><span data-stu-id="67baa-137">**ScaleLocal**</span></span>](id3dxmatrixstack-scalelocal.md)                           | <span data-ttu-id="67baa-138">Dimensione a matriz atual sobre a origem do objeto.</span><span class="sxs-lookup"><span data-stu-id="67baa-138">Scale the current matrix about the object origin.</span></span><br/>                                                                               |
| [<span data-ttu-id="67baa-139">**Traduzir**</span><span class="sxs-lookup"><span data-stu-id="67baa-139">**Translate**</span></span>](id3dxmatrixstack-translate.md)                             | <span data-ttu-id="67baa-140">Determina o produto da matriz atual e a matriz de conversão computada determinada pelos fatores especificados (x, y e z).</span><span class="sxs-lookup"><span data-stu-id="67baa-140">Determines the product of the current matrix and the computed translation matrix determined by the given factors (x, y, and z).</span></span><br/> |
| [<span data-ttu-id="67baa-141">**TranslateLocal**</span><span class="sxs-lookup"><span data-stu-id="67baa-141">**TranslateLocal**</span></span>](id3dxmatrixstack-translatelocal.md)                   | <span data-ttu-id="67baa-142">Determina o produto da matriz de conversão computada determinada pelos fatores especificados (x, y e z) e a matriz atual.</span><span class="sxs-lookup"><span data-stu-id="67baa-142">Determines the product of the computed translation matrix determined by the given factors (x, y, and z) and the current matrix.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="67baa-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="67baa-143">Remarks</span></span>

<span data-ttu-id="67baa-144">A interface ID3DX10MATRIXStack é obtida chamando a função [**D3DXCreateMatrixStack**](d3d10-d3dxcreatematrixstack.md) .</span><span class="sxs-lookup"><span data-stu-id="67baa-144">The ID3DX10MATRIXStack interface is obtained by calling the [**D3DXCreateMatrixStack**](d3d10-d3dxcreatematrixstack.md) function.</span></span>

<span data-ttu-id="67baa-145">O tipo LPD3DX10MATRIXSTACK é definido como um ponteiro para a interface **ID3DXMatrixStack** .</span><span class="sxs-lookup"><span data-stu-id="67baa-145">The LPD3DX10MATRIXSTACK type is defined as a pointer to the **ID3DXMatrixStack** interface.</span></span>


```
typedef interface ID3DXMatrixStack ID3DXMatrixStack;
typedef interface ID3DXMatrixStack *LPD3DXMATRIXSTACK;
```



## <a name="requirements"></a><span data-ttu-id="67baa-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67baa-146">Requirements</span></span>



| <span data-ttu-id="67baa-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="67baa-147">Requirement</span></span> | <span data-ttu-id="67baa-148">Valor</span><span class="sxs-lookup"><span data-stu-id="67baa-148">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="67baa-149">parâmetro</span><span class="sxs-lookup"><span data-stu-id="67baa-149">Header</span></span><br/>  | <dl> <span data-ttu-id="67baa-150"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="67baa-150"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="67baa-151">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="67baa-151">Library</span></span><br/> | <dl> <span data-ttu-id="67baa-152"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="67baa-152"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67baa-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="67baa-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67baa-154">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="67baa-154">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
