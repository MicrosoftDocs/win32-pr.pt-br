---
description: Define um valor de ponto flutuante.
ms.assetid: f49fb4d2-6e3d-4452-8102-76200c55cf1f
title: 'Método ID3DXBaseEffect:: SetFloat (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetFloat
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: af955748fff66e67e0e2f5650b869a746168de54
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103837919"
---
# <a name="id3dxbaseeffectsetfloat-method"></a><span data-ttu-id="3addf-103">Método ID3DXBaseEffect:: SetFloat</span><span class="sxs-lookup"><span data-stu-id="3addf-103">ID3DXBaseEffect::SetFloat method</span></span>

<span data-ttu-id="3addf-104">Define um valor de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="3addf-104">Sets a floating point value.</span></span>

## <a name="syntax"></a><span data-ttu-id="3addf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3addf-105">Syntax</span></span>


```C++
HRESULT SetFloat(
  [in] D3DXHANDLE hParameter,
  [in] FLOAT      f
);
```



## <a name="parameters"></a><span data-ttu-id="3addf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3addf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3addf-107">*hParameter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3addf-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3addf-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="3addf-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="3addf-109">Identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="3addf-109">Unique identifier.</span></span> <span data-ttu-id="3addf-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="3addf-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="3addf-111">*f* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="3addf-111">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3addf-112">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3addf-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3addf-113">Valor de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="3addf-113">Floating point value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3addf-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3addf-114">Return value</span></span>

<span data-ttu-id="3addf-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3addf-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3addf-116">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3addf-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3addf-117">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="3addf-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="3addf-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3addf-118">Requirements</span></span>



| <span data-ttu-id="3addf-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3addf-119">Requirement</span></span> | <span data-ttu-id="3addf-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3addf-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3addf-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3addf-121">Header</span></span><br/>  | <dl> <span data-ttu-id="3addf-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="3addf-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="3addf-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3addf-123">Library</span></span><br/> | <dl> <span data-ttu-id="3addf-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3addf-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="3addf-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="3addf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3addf-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="3addf-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="3addf-127">**GetFloat**</span><span class="sxs-lookup"><span data-stu-id="3addf-127">**GetFloat**</span></span>](id3dxbaseeffect--getfloat.md)
</dt> </dl>

 

 
