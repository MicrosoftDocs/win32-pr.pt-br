---
description: Carrega a identidade na matriz atual.
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
ms.openlocfilehash: e7ebc7b61679dc3938c2a57aa2346a45b136e5a7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105765011"
---
# <a name="id3dxmatrixstackloadidentity-method-d3dx9mathh"></a><span data-ttu-id="4c051-103">Método ID3DXMATRIXStack:: loadidentity (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="4c051-103">ID3DXMATRIXStack::LoadIdentity method (D3dx9math.h)</span></span>

<span data-ttu-id="4c051-104">Carrega a identidade na matriz atual.</span><span class="sxs-lookup"><span data-stu-id="4c051-104">Loads identity in the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c051-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4c051-105">Syntax</span></span>


```C++
HRESULT LoadIdentity();
```



## <a name="parameters"></a><span data-ttu-id="4c051-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4c051-106">Parameters</span></span>

<span data-ttu-id="4c051-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4c051-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4c051-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4c051-108">Return value</span></span>

<span data-ttu-id="4c051-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4c051-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4c051-110">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4c051-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4c051-111">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="4c051-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c051-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c051-112">Remarks</span></span>

<span data-ttu-id="4c051-113">A matriz de identidade é uma matriz na qual todos os coeficientes são 0,0, exceto os \[ 1, 1 \] \[ 2, 2 \] \[ 3, 3 \] \[ 4, os \] coeficientes, que são definidos como 1,0.</span><span class="sxs-lookup"><span data-stu-id="4c051-113">The identity matrix is a matrix in which all coefficients are 0.0 except the \[1,1\]\[2,2\]\[3,3\]\[4,4\] coefficients, which are set to 1.0.</span></span> <span data-ttu-id="4c051-114">A matriz de identidade é especial quando ela é aplicada a vértices, elas não são alteradas.</span><span class="sxs-lookup"><span data-stu-id="4c051-114">The identity matrix is special in that when it is applied to vertices, they are unchanged.</span></span> <span data-ttu-id="4c051-115">A matriz de identidade é usada como ponto de partida para matrizes que modificarão valores de vértice para criar rotações, traduções e quaisquer outras transformações que possam ser representadas por uma matriz 4x4.</span><span class="sxs-lookup"><span data-stu-id="4c051-115">The identity matrix is used as the starting point for matrices that will modify vertex values to create rotations, translations, and any other transformations that can be represented by a 4x4 matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c051-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c051-116">Requirements</span></span>



| <span data-ttu-id="4c051-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c051-117">Requirement</span></span> | <span data-ttu-id="4c051-118">Valor</span><span class="sxs-lookup"><span data-stu-id="4c051-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c051-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4c051-119">Header</span></span><br/>  | <dl> <span data-ttu-id="4c051-120"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c051-120"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="4c051-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4c051-121">Library</span></span><br/> | <dl> <span data-ttu-id="4c051-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4c051-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4c051-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c051-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c051-124">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="4c051-124">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="4c051-125">**ID3DXMATRIXStack:: loadmatrix**</span><span class="sxs-lookup"><span data-stu-id="4c051-125">**ID3DXMATRIXStack::LoadMatrix**</span></span>](id3dxmatrixstack--loadmatrix.md)
</dt> </dl>

 

 




