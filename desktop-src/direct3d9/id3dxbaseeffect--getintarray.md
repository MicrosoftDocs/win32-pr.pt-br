---
description: Obtém uma matriz de inteiros.
ms.assetid: c02b5343-db4f-4e8c-989c-6aba8c19c234
title: 'Método ID3DXBaseEffect:: GetIntArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetIntArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f13c6b8717c2108920d7b914da20b99f0451f5d9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298829"
---
# <a name="id3dxbaseeffectgetintarray-method"></a><span data-ttu-id="ba46c-103">Método ID3DXBaseEffect:: GetIntArray</span><span class="sxs-lookup"><span data-stu-id="ba46c-103">ID3DXBaseEffect::GetIntArray method</span></span>

<span data-ttu-id="ba46c-104">Obtém uma matriz de inteiros.</span><span class="sxs-lookup"><span data-stu-id="ba46c-104">Gets an array of integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba46c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ba46c-105">Syntax</span></span>


```C++
HRESULT GetIntArray(
  [in]  D3DXHANDLE hParameter,
  [out] INT        *pn,
  [in]  UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="ba46c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ba46c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba46c-107">*hParameter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ba46c-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba46c-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="ba46c-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="ba46c-109">Identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="ba46c-109">Unique identifier.</span></span> <span data-ttu-id="ba46c-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="ba46c-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba46c-111">*PN* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ba46c-111">*pn* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba46c-112">Tipo: **[ **int**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ba46c-112">Type: **[**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ba46c-113">Retorna uma matriz de inteiros.</span><span class="sxs-lookup"><span data-stu-id="ba46c-113">Returns an array of integers.</span></span>

</dd> <dt>

<span data-ttu-id="ba46c-114">*Contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="ba46c-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba46c-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ba46c-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ba46c-116">Número de inteiros na matriz.</span><span class="sxs-lookup"><span data-stu-id="ba46c-116">Number of integers in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba46c-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ba46c-117">Return value</span></span>

<span data-ttu-id="ba46c-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ba46c-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ba46c-119">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ba46c-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ba46c-120">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="ba46c-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba46c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba46c-121">Requirements</span></span>



| <span data-ttu-id="ba46c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba46c-122">Requirement</span></span> | <span data-ttu-id="ba46c-123">Valor</span><span class="sxs-lookup"><span data-stu-id="ba46c-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba46c-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ba46c-124">Header</span></span><br/>  | <dl> <span data-ttu-id="ba46c-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba46c-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="ba46c-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ba46c-126">Library</span></span><br/> | <dl> <span data-ttu-id="ba46c-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ba46c-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ba46c-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="ba46c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba46c-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="ba46c-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="ba46c-130">**SetIntArray**</span><span class="sxs-lookup"><span data-stu-id="ba46c-130">**SetIntArray**</span></span>](id3dxbaseeffect--setintarray.md)
</dt> </dl>

 

 
