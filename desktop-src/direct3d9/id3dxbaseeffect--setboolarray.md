---
description: Define uma matriz de valores Boolianos.
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
ms.openlocfilehash: 813259fc9fcca954c4d7a992c7542387be33bb6f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105751529"
---
# <a name="id3dxbaseeffectsetboolarray-method"></a><span data-ttu-id="25b83-103">Método ID3DXBaseEffect:: SetBoolArray</span><span class="sxs-lookup"><span data-stu-id="25b83-103">ID3DXBaseEffect::SetBoolArray method</span></span>

<span data-ttu-id="25b83-104">Define uma matriz de valores Boolianos.</span><span class="sxs-lookup"><span data-stu-id="25b83-104">Sets an array of Boolean values.</span></span>

## <a name="syntax"></a><span data-ttu-id="25b83-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="25b83-105">Syntax</span></span>


```C++
HRESULT SetBoolArray(
  [in]       D3DXHANDLE hParameter,
  [in] const BOOL       *pB,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="25b83-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="25b83-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25b83-107">*hParameter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="25b83-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25b83-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="25b83-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="25b83-109">Identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="25b83-109">Unique identifier.</span></span> <span data-ttu-id="25b83-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="25b83-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="25b83-111">*PB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="25b83-111">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25b83-112">Tipo: **const [**bool**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="25b83-112">Type: **const [**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="25b83-113">Matriz de valores Boolianos.</span><span class="sxs-lookup"><span data-stu-id="25b83-113">Array of Boolean values.</span></span>

</dd> <dt>

<span data-ttu-id="25b83-114">*Contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="25b83-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25b83-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="25b83-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="25b83-116">Número de valores Boolianos na matriz.</span><span class="sxs-lookup"><span data-stu-id="25b83-116">Number of Boolean values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25b83-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="25b83-117">Return value</span></span>

<span data-ttu-id="25b83-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="25b83-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="25b83-119">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="25b83-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="25b83-120">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="25b83-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="25b83-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25b83-121">Requirements</span></span>



| <span data-ttu-id="25b83-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="25b83-122">Requirement</span></span> | <span data-ttu-id="25b83-123">Valor</span><span class="sxs-lookup"><span data-stu-id="25b83-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="25b83-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="25b83-124">Header</span></span><br/>  | <dl> <span data-ttu-id="25b83-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="25b83-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="25b83-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="25b83-126">Library</span></span><br/> | <dl> <span data-ttu-id="25b83-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="25b83-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="25b83-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="25b83-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25b83-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="25b83-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="25b83-130">**GetBoolArray**</span><span class="sxs-lookup"><span data-stu-id="25b83-130">**GetBoolArray**</span></span>](id3dxbaseeffect--getboolarray.md)
</dt> </dl>

 

 
