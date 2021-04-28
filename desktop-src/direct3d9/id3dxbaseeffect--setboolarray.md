---
description: 'Método ID3DXBaseEffect:: SetBoolArray – define uma matriz de valores Boolianos.'
ms.assetid: 920b3482-cc30-4ab2-bfce-59f03afe11da
title: 'Método ID3DXBaseEffect:: SetBoolArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetBoolArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: cad6846914d348dd49d6362d70271c5af078e35d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093824"
---
# <a name="id3dxbaseeffectsetboolarray-method"></a><span data-ttu-id="7da71-103">Método ID3DXBaseEffect:: SetBoolArray</span><span class="sxs-lookup"><span data-stu-id="7da71-103">ID3DXBaseEffect::SetBoolArray method</span></span>

<span data-ttu-id="7da71-104">Define uma matriz de valores Boolianos.</span><span class="sxs-lookup"><span data-stu-id="7da71-104">Sets an array of Boolean values.</span></span>

## <a name="syntax"></a><span data-ttu-id="7da71-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7da71-105">Syntax</span></span>


```C++
HRESULT SetBoolArray(
  [in]       D3DXHANDLE hParameter,
  [in] const BOOL       *pB,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="7da71-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7da71-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7da71-107">*hParameter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7da71-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7da71-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="7da71-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="7da71-109">Identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="7da71-109">Unique identifier.</span></span> <span data-ttu-id="7da71-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="7da71-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="7da71-111">*PB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7da71-111">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7da71-112">Tipo: **const [**bool**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="7da71-112">Type: **const [**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7da71-113">Matriz de valores Boolianos.</span><span class="sxs-lookup"><span data-stu-id="7da71-113">Array of Boolean values.</span></span>

</dd> <dt>

<span data-ttu-id="7da71-114">*Contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="7da71-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7da71-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7da71-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7da71-116">Número de valores Boolianos na matriz.</span><span class="sxs-lookup"><span data-stu-id="7da71-116">Number of Boolean values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7da71-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="7da71-117">Return value</span></span>

<span data-ttu-id="7da71-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7da71-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7da71-119">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7da71-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7da71-120">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="7da71-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="7da71-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7da71-121">Requirements</span></span>



| <span data-ttu-id="7da71-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7da71-122">Requirement</span></span> | <span data-ttu-id="7da71-123">Valor</span><span class="sxs-lookup"><span data-stu-id="7da71-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7da71-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7da71-124">Header</span></span><br/>  | <dl> <span data-ttu-id="7da71-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="7da71-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="7da71-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7da71-126">Library</span></span><br/> | <dl> <span data-ttu-id="7da71-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7da71-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7da71-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="7da71-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7da71-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="7da71-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="7da71-130">**GetBoolArray**</span><span class="sxs-lookup"><span data-stu-id="7da71-130">**GetBoolArray**</span></span>](id3dxbaseeffect--getboolarray.md)
</dt> </dl>

 

 
