---
description: Carrega a identidade na matriz atual.
ms.assetid: 324b49c2-3aca-4bbb-90f3-62f3ffb2fa45
title: 'Método ID3DXMATRIXStack:: loadidentity (D3DX10. h)'
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 85a58529be3bfcb4d52ba096bb6134fe08994d77
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105768223"
---
# <a name="id3dxmatrixstackloadidentity-method-d3dx10h"></a><span data-ttu-id="5d227-103">Método ID3DXMATRIXStack:: loadidentity (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="5d227-103">ID3DXMATRIXStack::LoadIdentity method (D3DX10.h)</span></span>

<span data-ttu-id="5d227-104">Carrega a identidade na matriz atual.</span><span class="sxs-lookup"><span data-stu-id="5d227-104">Loads identity in the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d227-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5d227-105">Syntax</span></span>


```C++
HRESULT LoadIdentity();
```



## <a name="parameters"></a><span data-ttu-id="5d227-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5d227-106">Parameters</span></span>

<span data-ttu-id="5d227-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="5d227-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5d227-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5d227-108">Return value</span></span>

<span data-ttu-id="5d227-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5d227-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5d227-110">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5d227-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5d227-111">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="5d227-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d227-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="5d227-112">Remarks</span></span>

<span data-ttu-id="5d227-113">A matriz de identidade é uma matriz na qual todos os coeficientes são 0,0, exceto os \[ 1, 1 \] \[ 2, 2 \] \[ 3, 3 \] \[ 4, os \] coeficientes, que são definidos como 1,0.</span><span class="sxs-lookup"><span data-stu-id="5d227-113">The identity matrix is a matrix in which all coefficients are 0.0 except the \[1,1\]\[2,2\]\[3,3\]\[4,4\] coefficients, which are set to 1.0.</span></span> <span data-ttu-id="5d227-114">A matriz de identidade é especial quando ela é aplicada a vértices, elas não são alteradas.</span><span class="sxs-lookup"><span data-stu-id="5d227-114">The identity matrix is special in that when it is applied to vertices, they are unchanged.</span></span> <span data-ttu-id="5d227-115">A matriz de identidade é usada como ponto de partida para matrizes que modificarão valores de vértice para criar rotações, traduções e quaisquer outras transformações que possam ser representadas por uma matriz 4x4.</span><span class="sxs-lookup"><span data-stu-id="5d227-115">The identity matrix is used as the starting point for matrices that will modify vertex values to create rotations, translations, and any other transformations that can be represented by a 4x4 matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d227-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d227-116">Requirements</span></span>



| <span data-ttu-id="5d227-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d227-117">Requirement</span></span> | <span data-ttu-id="5d227-118">Valor</span><span class="sxs-lookup"><span data-stu-id="5d227-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5d227-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5d227-119">Header</span></span><br/>  | <dl> <span data-ttu-id="5d227-120"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d227-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="5d227-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5d227-121">Library</span></span><br/> | <dl> <span data-ttu-id="5d227-122"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5d227-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d227-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="5d227-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d227-124">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="5d227-124">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="5d227-125">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="5d227-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




