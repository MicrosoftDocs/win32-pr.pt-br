---
description: Obtém uma matriz de valores de ponto flutuante.
ms.assetid: ba839129-c332-4ce8-b7c1-ea0ef4697ade
title: 'Método ID3DXBaseEffect:: GetFloatArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFloatArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 2ea71daa3b207a8f7716bf0a0db3608554c0b9f8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298833"
---
# <a name="id3dxbaseeffectgetfloatarray-method"></a><span data-ttu-id="7c83f-103">Método ID3DXBaseEffect:: GetFloatArray</span><span class="sxs-lookup"><span data-stu-id="7c83f-103">ID3DXBaseEffect::GetFloatArray method</span></span>

<span data-ttu-id="7c83f-104">Obtém uma matriz de valores de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="7c83f-104">Gets an array of floating point values.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c83f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7c83f-105">Syntax</span></span>


```C++
HRESULT GetFloatArray(
  [in]  D3DXHANDLE hParameter,
  [out] FLOAT      *pf,
  [in]  UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="7c83f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7c83f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c83f-107">*hParameter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7c83f-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c83f-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="7c83f-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="7c83f-109">Identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="7c83f-109">Unique identifier.</span></span> <span data-ttu-id="7c83f-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="7c83f-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c83f-111">*PF* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7c83f-111">*pf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c83f-112">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="7c83f-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7c83f-113">Retorna uma matriz de valores de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="7c83f-113">Returns an array of floating point values.</span></span>

</dd> <dt>

<span data-ttu-id="7c83f-114">*Contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="7c83f-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c83f-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7c83f-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7c83f-116">Número de valores de ponto flutuante na matriz.</span><span class="sxs-lookup"><span data-stu-id="7c83f-116">Number of floating point values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c83f-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7c83f-117">Return value</span></span>

<span data-ttu-id="7c83f-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7c83f-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7c83f-119">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7c83f-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7c83f-120">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="7c83f-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c83f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c83f-121">Requirements</span></span>



| <span data-ttu-id="7c83f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c83f-122">Requirement</span></span> | <span data-ttu-id="7c83f-123">Valor</span><span class="sxs-lookup"><span data-stu-id="7c83f-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c83f-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7c83f-124">Header</span></span><br/>  | <dl> <span data-ttu-id="7c83f-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c83f-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="7c83f-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7c83f-126">Library</span></span><br/> | <dl> <span data-ttu-id="7c83f-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c83f-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7c83f-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c83f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c83f-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="7c83f-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="7c83f-130">**SetFloatArray**</span><span class="sxs-lookup"><span data-stu-id="7c83f-130">**SetFloatArray**</span></span>](id3dxbaseeffect--setfloatarray.md)
</dt> </dl>

 

 
