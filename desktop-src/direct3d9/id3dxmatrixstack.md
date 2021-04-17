---
description: Os aplicativos usam os métodos da interface ID3DXMATRIXStack para manipular uma pilha de matriz.
ms.assetid: 4d382d39-a9da-4a3b-b7b6-d6890357d467
title: Interface ID3DXMATRIXStack (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9446301ce057e788b4039f8ea3a144fb1fa19024
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105762384"
---
# <a name="id3dxmatrixstack-interface"></a><span data-ttu-id="2d759-103">Interface ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="2d759-103">ID3DXMATRIXStack interface</span></span>

<span data-ttu-id="2d759-104">Os aplicativos usam os métodos da interface ID3DXMATRIXStack para manipular uma pilha de matriz.</span><span class="sxs-lookup"><span data-stu-id="2d759-104">Applications use the methods of the ID3DXMATRIXStack interface to manipulate a matrix stack.</span></span>

## <a name="members"></a><span data-ttu-id="2d759-105">Membros</span><span class="sxs-lookup"><span data-stu-id="2d759-105">Members</span></span>

<span data-ttu-id="2d759-106">A interface **ID3DXMATRIXStack** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="2d759-106">The **ID3DXMATRIXStack** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2d759-107">**ID3DXMATRIXStack** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2d759-107">**ID3DXMATRIXStack** also has these types of members:</span></span>

-   [<span data-ttu-id="2d759-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="2d759-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2d759-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="2d759-109">Methods</span></span>

<span data-ttu-id="2d759-110">A interface **ID3DXMATRIXStack** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="2d759-110">The **ID3DXMATRIXStack** interface has these methods.</span></span>



| <span data-ttu-id="2d759-111">Método</span><span class="sxs-lookup"><span data-stu-id="2d759-111">Method</span></span>                                                                       | <span data-ttu-id="2d759-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="2d759-112">Description</span></span>                                                                                                                                |
|:-----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2d759-113">**GetTop**</span><span class="sxs-lookup"><span data-stu-id="2d759-113">**GetTop**</span></span>](id3dxmatrixstack--gettop.md)                                   | <span data-ttu-id="2d759-114">Recupera a matriz atual na parte superior da pilha.</span><span class="sxs-lookup"><span data-stu-id="2d759-114">Retrieves the current matrix at the top of the stack.</span></span><br/>                                                                           |
| [<span data-ttu-id="2d759-115">**Loadidentity**</span><span class="sxs-lookup"><span data-stu-id="2d759-115">**LoadIdentity**</span></span>](id3dxmatrixstack--loadidentity.md)                       | <span data-ttu-id="2d759-116">Carrega a identidade na matriz atual.</span><span class="sxs-lookup"><span data-stu-id="2d759-116">Loads identity in the current matrix.</span></span><br/>                                                                                           |
| [<span data-ttu-id="2d759-117">**Loadmatrix**</span><span class="sxs-lookup"><span data-stu-id="2d759-117">**LoadMatrix**</span></span>](id3dxmatrixstack--loadmatrix.md)                           | <span data-ttu-id="2d759-118">Carrega a matriz determinada na matriz atual.</span><span class="sxs-lookup"><span data-stu-id="2d759-118">Loads the given matrix into the current matrix.</span></span><br/>                                                                                 |
| [<span data-ttu-id="2d759-119">**MultMatrix**</span><span class="sxs-lookup"><span data-stu-id="2d759-119">**MultMatrix**</span></span>](id3dxmatrixstack--multmatrix.md)                           | <span data-ttu-id="2d759-120">Determina o produto da matriz atual e a matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="2d759-120">Determines the product of the current matrix and the given matrix.</span></span><br/>                                                              |
| [<span data-ttu-id="2d759-121">**MultMatrixLocal**</span><span class="sxs-lookup"><span data-stu-id="2d759-121">**MultMatrixLocal**</span></span>](id3dxmatrixstack--multmatrixlocal.md)                 | <span data-ttu-id="2d759-122">Determina o produto da matriz e da matriz atual.</span><span class="sxs-lookup"><span data-stu-id="2d759-122">Determines the product of the given matrix and the current matrix.</span></span><br/>                                                              |
| [<span data-ttu-id="2d759-123">**Pop**</span><span class="sxs-lookup"><span data-stu-id="2d759-123">**Pop**</span></span>](id3dxmatrixstack--pop.md)                                         | <span data-ttu-id="2d759-124">Remove a matriz atual da parte superior da pilha.</span><span class="sxs-lookup"><span data-stu-id="2d759-124">Removes the current matrix from the top of the stack.</span></span><br/>                                                                           |
| [<span data-ttu-id="2d759-125">**Push**</span><span class="sxs-lookup"><span data-stu-id="2d759-125">**Push**</span></span>](id3dxmatrixstack--push.md)                                       | <span data-ttu-id="2d759-126">Adiciona uma matriz à pilha.</span><span class="sxs-lookup"><span data-stu-id="2d759-126">Adds a matrix to the stack.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="2d759-127">**RotateAxis**</span><span class="sxs-lookup"><span data-stu-id="2d759-127">**RotateAxis**</span></span>](id3dxmatrixstack--rotateaxis.md)                           | <span data-ttu-id="2d759-128">Gira (em relação ao espaço de coordenadas mundiais) em um eixo arbitrário.</span><span class="sxs-lookup"><span data-stu-id="2d759-128">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span><br/>                                                          |
| [<span data-ttu-id="2d759-129">**RotateAxisLocal**</span><span class="sxs-lookup"><span data-stu-id="2d759-129">**RotateAxisLocal**</span></span>](id3dxmatrixstack--rotateaxislocal.md)                 | <span data-ttu-id="2d759-130">Gira (em relação ao espaço de coordenadas local do objeto) em um eixo arbitrário.</span><span class="sxs-lookup"><span data-stu-id="2d759-130">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span><br/>                                             |
| [<span data-ttu-id="2d759-131">**RotateYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="2d759-131">**RotateYawPitchRoll**</span></span>](id3dxmatrixstack--rotateyawpitchroll.md)           | <span data-ttu-id="2d759-132">Gira (em relação ao espaço de coordenadas mundiais) em um eixo arbitrário.</span><span class="sxs-lookup"><span data-stu-id="2d759-132">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span><br/>                                                          |
| [<span data-ttu-id="2d759-133">**RotateYawPitchRollLocal**</span><span class="sxs-lookup"><span data-stu-id="2d759-133">**RotateYawPitchRollLocal**</span></span>](id3dxmatrixstack--rotateyawpitchrolllocal.md) | <span data-ttu-id="2d759-134">Gira (em relação ao espaço de coordenadas local do objeto) em um eixo arbitrário.</span><span class="sxs-lookup"><span data-stu-id="2d759-134">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span><br/>                                             |
| [<span data-ttu-id="2d759-135">**Escalonáve**</span><span class="sxs-lookup"><span data-stu-id="2d759-135">**Scale**</span></span>](id3dxmatrixstack--scale.md)                                     | <span data-ttu-id="2d759-136">Dimensione a matriz atual sobre a origem da coordenada mundial.</span><span class="sxs-lookup"><span data-stu-id="2d759-136">Scale the current matrix about the world coordinate origin.</span></span><br/>                                                                     |
| [<span data-ttu-id="2d759-137">**ScaleLocal**</span><span class="sxs-lookup"><span data-stu-id="2d759-137">**ScaleLocal**</span></span>](id3dxmatrixstack--scalelocal.md)                           | <span data-ttu-id="2d759-138">Dimensione a matriz atual sobre a origem do objeto.</span><span class="sxs-lookup"><span data-stu-id="2d759-138">Scale the current matrix about the object origin.</span></span><br/>                                                                               |
| [<span data-ttu-id="2d759-139">**Traduzir**</span><span class="sxs-lookup"><span data-stu-id="2d759-139">**Translate**</span></span>](id3dxmatrixstack--translate.md)                             | <span data-ttu-id="2d759-140">Determina o produto da matriz atual e a matriz de conversão computada determinada pelos fatores especificados (x, y e z).</span><span class="sxs-lookup"><span data-stu-id="2d759-140">Determines the product of the current matrix and the computed translation matrix determined by the given factors (x, y, and z).</span></span><br/> |
| [<span data-ttu-id="2d759-141">**TranslateLocal**</span><span class="sxs-lookup"><span data-stu-id="2d759-141">**TranslateLocal**</span></span>](id3dxmatrixstack--translatelocal.md)                   | <span data-ttu-id="2d759-142">Determina o produto da matriz de conversão computada determinada pelos fatores especificados (x, y e z) e a matriz atual.</span><span class="sxs-lookup"><span data-stu-id="2d759-142">Determines the product of the computed translation matrix determined by the given factors (x, y, and z) and the current matrix.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2d759-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="2d759-143">Remarks</span></span>

<span data-ttu-id="2d759-144">A interface **ID3DXMATRIXStack** é obtida chamando a função [**D3DXCreateMatrixStack**](d3dxcreatematrixstack.md) .</span><span class="sxs-lookup"><span data-stu-id="2d759-144">The **ID3DXMATRIXStack** interface is obtained by calling the [**D3DXCreateMatrixStack**](d3dxcreatematrixstack.md) function.</span></span>

<span data-ttu-id="2d759-145">O tipo LPD3DXMATRIXSTACK é definido como um ponteiro para a interface **ID3DXMATRIXStack** .</span><span class="sxs-lookup"><span data-stu-id="2d759-145">The LPD3DXMATRIXSTACK type is defined as a pointer to the **ID3DXMATRIXStack** interface.</span></span>


```
typedef interface ID3DXMATRIXStack ID3DXMATRIXStack;
typedef interface ID3DXMATRIXStack *LPD3DXMATRIXSTACK;
```



## <a name="requirements"></a><span data-ttu-id="2d759-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d759-146">Requirements</span></span>



| <span data-ttu-id="2d759-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d759-147">Requirement</span></span> | <span data-ttu-id="2d759-148">Valor</span><span class="sxs-lookup"><span data-stu-id="2d759-148">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d759-149">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2d759-149">Header</span></span><br/>  | <dl> <span data-ttu-id="2d759-150"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d759-150"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="2d759-151">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2d759-151">Library</span></span><br/> | <dl> <span data-ttu-id="2d759-152"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d759-152"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2d759-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="2d759-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d759-154">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="2d759-154">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
