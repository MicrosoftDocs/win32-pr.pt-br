---
description: Define uma matriz de valores de ponto flutuante.
ms.assetid: 4b9c27b4-0255-4bbf-9168-491936d64fb9
title: 'Método ID3DXBaseEffect:: SetFloatArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetFloatArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 9927f3cd79d7950a94e62881089fb06c67395bac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172919"
---
# <a name="id3dxbaseeffectsetfloatarray-method"></a><span data-ttu-id="67305-103">Método ID3DXBaseEffect:: SetFloatArray</span><span class="sxs-lookup"><span data-stu-id="67305-103">ID3DXBaseEffect::SetFloatArray method</span></span>

<span data-ttu-id="67305-104">Define uma matriz de valores de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="67305-104">Sets an array of floating point values.</span></span>

## <a name="syntax"></a><span data-ttu-id="67305-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="67305-105">Syntax</span></span>


```C++
HRESULT SetFloatArray(
  [in]       D3DXHANDLE hParameter,
  [in] const FLOAT      *pf,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="67305-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="67305-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67305-107">*hParameter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="67305-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67305-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="67305-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="67305-109">Identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="67305-109">Unique identifier.</span></span> <span data-ttu-id="67305-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="67305-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="67305-111">*PF* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="67305-111">*pf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67305-112">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="67305-112">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="67305-113">Matriz de valores de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="67305-113">Array of floating point values.</span></span>

</dd> <dt>

<span data-ttu-id="67305-114">*Contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="67305-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67305-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="67305-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="67305-116">Número de valores de ponto flutuante na matriz.</span><span class="sxs-lookup"><span data-stu-id="67305-116">Number of floating point values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67305-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="67305-117">Return value</span></span>

<span data-ttu-id="67305-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="67305-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="67305-119">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="67305-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="67305-120">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="67305-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="67305-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67305-121">Requirements</span></span>



| <span data-ttu-id="67305-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="67305-122">Requirement</span></span> | <span data-ttu-id="67305-123">Valor</span><span class="sxs-lookup"><span data-stu-id="67305-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="67305-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="67305-124">Header</span></span><br/>  | <dl> <span data-ttu-id="67305-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="67305-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="67305-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="67305-126">Library</span></span><br/> | <dl> <span data-ttu-id="67305-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="67305-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="67305-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="67305-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67305-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="67305-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="67305-130">**GetFloatArray**</span><span class="sxs-lookup"><span data-stu-id="67305-130">**GetFloatArray**</span></span>](id3dxbaseeffect--getfloatarray.md)
</dt> </dl>

 

 
