---
description: 'Método ID3DXMATRIXStack:: loadidentity (D3dx9math. h) – carrega a identidade na matriz atual.'
ms.assetid: e314a51f-4016-4819-a95d-d91864a54b2e
title: 'Método ID3DXMATRIXStack:: loadidentity (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.LoadIdentity
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 663559db0746b9d689066e537c1473f467341cbc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093554"
---
# <a name="id3dxmatrixstackloadidentity-method-d3dx9mathh"></a><span data-ttu-id="c731b-103">Método ID3DXMATRIXStack:: loadidentity (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="c731b-103">ID3DXMATRIXStack::LoadIdentity method (D3dx9math.h)</span></span>

<span data-ttu-id="c731b-104">Carrega a identidade na matriz atual.</span><span class="sxs-lookup"><span data-stu-id="c731b-104">Loads identity in the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="c731b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c731b-105">Syntax</span></span>


```C++
HRESULT LoadIdentity();
```



## <a name="parameters"></a><span data-ttu-id="c731b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c731b-106">Parameters</span></span>

<span data-ttu-id="c731b-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c731b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c731b-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c731b-108">Return value</span></span>

<span data-ttu-id="c731b-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c731b-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c731b-110">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c731b-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c731b-111">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="c731b-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c731b-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="c731b-112">Remarks</span></span>

<span data-ttu-id="c731b-113">A matriz de identidade é uma matriz na qual todos os coeficientes são 0,0, exceto os \[ 1, 1 \] \[ 2, 2 \] \[ 3, 3 \] \[ 4, os \] coeficientes, que são definidos como 1,0.</span><span class="sxs-lookup"><span data-stu-id="c731b-113">The identity matrix is a matrix in which all coefficients are 0.0 except the \[1,1\]\[2,2\]\[3,3\]\[4,4\] coefficients, which are set to 1.0.</span></span> <span data-ttu-id="c731b-114">A matriz de identidade é especial quando ela é aplicada a vértices, elas não são alteradas.</span><span class="sxs-lookup"><span data-stu-id="c731b-114">The identity matrix is special in that when it is applied to vertices, they are unchanged.</span></span> <span data-ttu-id="c731b-115">A matriz de identidade é usada como ponto de partida para matrizes que modificarão valores de vértice para criar rotações, traduções e quaisquer outras transformações que possam ser representadas por uma matriz 4x4.</span><span class="sxs-lookup"><span data-stu-id="c731b-115">The identity matrix is used as the starting point for matrices that will modify vertex values to create rotations, translations, and any other transformations that can be represented by a 4x4 matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="c731b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c731b-116">Requirements</span></span>



| <span data-ttu-id="c731b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c731b-117">Requirement</span></span> | <span data-ttu-id="c731b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c731b-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c731b-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c731b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="c731b-120"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c731b-120"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c731b-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c731b-121">Library</span></span><br/> | <dl> <span data-ttu-id="c731b-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c731b-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c731b-123">Consulte também</span><span class="sxs-lookup"><span data-stu-id="c731b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c731b-124">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="c731b-124">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="c731b-125">**ID3DXMATRIXStack:: loadmatrix**</span><span class="sxs-lookup"><span data-stu-id="c731b-125">**ID3DXMATRIXStack::LoadMatrix**</span></span>](id3dxmatrixstack--loadmatrix.md)
</dt> </dl>

 

 




