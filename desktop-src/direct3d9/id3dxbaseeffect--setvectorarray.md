---
description: Define uma matriz de vetores.
ms.assetid: 7a9c61b4-7bfc-4879-abd2-a42d40e9b2a7
title: 'Método ID3DXBaseEffect:: SetVectorArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetVectorArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 4c5deace65608ee547b8fdcc4fb236b11d38c810
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930668"
---
# <a name="id3dxbaseeffectsetvectorarray-method"></a><span data-ttu-id="6ba8d-103">Método ID3DXBaseEffect:: SetVectorArray</span><span class="sxs-lookup"><span data-stu-id="6ba8d-103">ID3DXBaseEffect::SetVectorArray method</span></span>

<span data-ttu-id="6ba8d-104">Define uma matriz de vetores.</span><span class="sxs-lookup"><span data-stu-id="6ba8d-104">Sets an array of vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ba8d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6ba8d-105">Syntax</span></span>


```C++
HRESULT SetVectorArray(
  [in]       D3DXHANDLE  hParameter,
  [in] const D3DXVECTOR4 *pVector,
  [in]       UINT        Count
);
```



## <a name="parameters"></a><span data-ttu-id="6ba8d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6ba8d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ba8d-107">*hParameter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6ba8d-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ba8d-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="6ba8d-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="6ba8d-109">Identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="6ba8d-109">Unique identifier.</span></span> <span data-ttu-id="6ba8d-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="6ba8d-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ba8d-111">*pVector* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6ba8d-111">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ba8d-112">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="6ba8d-112">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="6ba8d-113">Matriz de vetores de ponto flutuante 4D.</span><span class="sxs-lookup"><span data-stu-id="6ba8d-113">Array of 4D floating point vectors.</span></span>

</dd> <dt>

<span data-ttu-id="6ba8d-114">*Contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="6ba8d-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ba8d-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6ba8d-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6ba8d-116">Número de vetores na matriz.</span><span class="sxs-lookup"><span data-stu-id="6ba8d-116">Number of vectors in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ba8d-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6ba8d-117">Return value</span></span>

<span data-ttu-id="6ba8d-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6ba8d-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6ba8d-119">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6ba8d-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6ba8d-120">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="6ba8d-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ba8d-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ba8d-121">Remarks</span></span>

<span data-ttu-id="6ba8d-122">Se os vetores de destino forem menores do que os vetores de origem, os componentes adicionais dos vetores de origem serão ignorados.</span><span class="sxs-lookup"><span data-stu-id="6ba8d-122">If the destination vectors are smaller than the source vectors, the additional components of the source vectors will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ba8d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ba8d-123">Requirements</span></span>



| <span data-ttu-id="6ba8d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ba8d-124">Requirement</span></span> | <span data-ttu-id="6ba8d-125">Valor</span><span class="sxs-lookup"><span data-stu-id="6ba8d-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ba8d-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6ba8d-126">Header</span></span><br/>  | <dl> <span data-ttu-id="6ba8d-127"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ba8d-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="6ba8d-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6ba8d-128">Library</span></span><br/> | <dl> <span data-ttu-id="6ba8d-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6ba8d-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="6ba8d-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="6ba8d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ba8d-131">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="6ba8d-131">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="6ba8d-132">**GetVectorArray**</span><span class="sxs-lookup"><span data-stu-id="6ba8d-132">**GetVectorArray**</span></span>](id3dxbaseeffect--getvectorarray.md)
</dt> </dl>

 

 
