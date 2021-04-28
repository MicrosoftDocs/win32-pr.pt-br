---
description: 'Método ID3DXMATRIXStack:: loadidentity (D3DX10. h) – carrega a identidade na matriz atual.'
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
ms.openlocfilehash: f056a911b19c0ea18f5f728a6ce8c4403dd14587
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107984"
---
# <a name="id3dxmatrixstackloadidentity-method-d3dx10h"></a><span data-ttu-id="f830f-103">Método ID3DXMATRIXStack:: loadidentity (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="f830f-103">ID3DXMATRIXStack::LoadIdentity method (D3DX10.h)</span></span>

<span data-ttu-id="f830f-104">Carrega a identidade na matriz atual.</span><span class="sxs-lookup"><span data-stu-id="f830f-104">Loads identity in the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="f830f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f830f-105">Syntax</span></span>


```C++
HRESULT LoadIdentity();
```



## <a name="parameters"></a><span data-ttu-id="f830f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f830f-106">Parameters</span></span>

<span data-ttu-id="f830f-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f830f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f830f-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f830f-108">Return value</span></span>

<span data-ttu-id="f830f-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f830f-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f830f-110">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f830f-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f830f-111">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="f830f-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="f830f-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="f830f-112">Remarks</span></span>

<span data-ttu-id="f830f-113">A matriz de identidade é uma matriz na qual todos os coeficientes são 0,0, exceto os \[ 1, 1 \] \[ 2, 2 \] \[ 3, 3 \] \[ 4, os \] coeficientes, que são definidos como 1,0.</span><span class="sxs-lookup"><span data-stu-id="f830f-113">The identity matrix is a matrix in which all coefficients are 0.0 except the \[1,1\]\[2,2\]\[3,3\]\[4,4\] coefficients, which are set to 1.0.</span></span> <span data-ttu-id="f830f-114">A matriz de identidade é especial quando ela é aplicada a vértices, elas não são alteradas.</span><span class="sxs-lookup"><span data-stu-id="f830f-114">The identity matrix is special in that when it is applied to vertices, they are unchanged.</span></span> <span data-ttu-id="f830f-115">A matriz de identidade é usada como ponto de partida para matrizes que modificarão valores de vértice para criar rotações, traduções e quaisquer outras transformações que possam ser representadas por uma matriz 4x4.</span><span class="sxs-lookup"><span data-stu-id="f830f-115">The identity matrix is used as the starting point for matrices that will modify vertex values to create rotations, translations, and any other transformations that can be represented by a 4x4 matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="f830f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f830f-116">Requirements</span></span>



| <span data-ttu-id="f830f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f830f-117">Requirement</span></span> | <span data-ttu-id="f830f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="f830f-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f830f-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f830f-119">Header</span></span><br/>  | <dl> <span data-ttu-id="f830f-120"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="f830f-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="f830f-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f830f-121">Library</span></span><br/> | <dl> <span data-ttu-id="f830f-122"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f830f-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f830f-123">Consulte também</span><span class="sxs-lookup"><span data-stu-id="f830f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f830f-124">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="f830f-124">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="f830f-125">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="f830f-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




