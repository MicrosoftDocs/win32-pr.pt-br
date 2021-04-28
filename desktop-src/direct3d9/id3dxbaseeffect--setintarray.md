---
description: 'Método ID3DXBaseEffect:: SetIntArray – define uma matriz de inteiros.'
ms.assetid: 4491bffd-ce5e-4f84-ac11-0314a1b16d63
title: 'Método ID3DXBaseEffect:: SetIntArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetIntArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a14e837a0903290c3197bbb17ec4b2da3f68b419
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093754"
---
# <a name="id3dxbaseeffectsetintarray-method"></a><span data-ttu-id="2154d-103">Método ID3DXBaseEffect:: SetIntArray</span><span class="sxs-lookup"><span data-stu-id="2154d-103">ID3DXBaseEffect::SetIntArray method</span></span>

<span data-ttu-id="2154d-104">Define uma matriz de inteiros.</span><span class="sxs-lookup"><span data-stu-id="2154d-104">Sets an array of integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="2154d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2154d-105">Syntax</span></span>


```C++
HRESULT SetIntArray(
  [in]       D3DXHANDLE hParameter,
  [in] const INT        *pn,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="2154d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2154d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2154d-107">*hParameter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2154d-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2154d-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="2154d-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="2154d-109">Identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="2154d-109">Unique identifier.</span></span> <span data-ttu-id="2154d-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="2154d-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="2154d-111">*PN* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2154d-111">*pn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2154d-112">Tipo: **const [**int**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="2154d-112">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2154d-113">Matriz de inteiros.</span><span class="sxs-lookup"><span data-stu-id="2154d-113">Array of integers.</span></span>

</dd> <dt>

<span data-ttu-id="2154d-114">*Contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="2154d-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2154d-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2154d-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2154d-116">Número de inteiros na matriz.</span><span class="sxs-lookup"><span data-stu-id="2154d-116">Number of integers in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2154d-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="2154d-117">Return value</span></span>

<span data-ttu-id="2154d-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2154d-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2154d-119">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2154d-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2154d-120">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="2154d-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="2154d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2154d-121">Requirements</span></span>



| <span data-ttu-id="2154d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2154d-122">Requirement</span></span> | <span data-ttu-id="2154d-123">Valor</span><span class="sxs-lookup"><span data-stu-id="2154d-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2154d-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2154d-124">Header</span></span><br/>  | <dl> <span data-ttu-id="2154d-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="2154d-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="2154d-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2154d-126">Library</span></span><br/> | <dl> <span data-ttu-id="2154d-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2154d-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2154d-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="2154d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2154d-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="2154d-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="2154d-130">**GetIntArray**</span><span class="sxs-lookup"><span data-stu-id="2154d-130">**GetIntArray**</span></span>](id3dxbaseeffect--getintarray.md)
</dt> </dl>

 

 
