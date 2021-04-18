---
description: Obtém uma cadeia de caracteres.
ms.assetid: 49388582-a110-4aa2-90ab-2282b59da951
title: 'Método ID3DXBaseEffect:: GetString (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetString
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 74c82bb80603dc4519e717d86297f6529ad36193
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105766500"
---
# <a name="id3dxbaseeffectgetstring-method"></a><span data-ttu-id="148d2-103">Método ID3DXBaseEffect:: GetString</span><span class="sxs-lookup"><span data-stu-id="148d2-103">ID3DXBaseEffect::GetString method</span></span>

<span data-ttu-id="148d2-104">Obtém uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="148d2-104">Gets a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="148d2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="148d2-105">Syntax</span></span>


```C++
HRESULT GetString(
  [in]  D3DXHANDLE hParameter,
  [out] LPCSTR     *ppString
);
```



## <a name="parameters"></a><span data-ttu-id="148d2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="148d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="148d2-107">*hParameter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="148d2-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="148d2-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="148d2-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="148d2-109">Identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="148d2-109">Unique identifier.</span></span> <span data-ttu-id="148d2-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="148d2-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="148d2-111">*ppString* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="148d2-111">*ppString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="148d2-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="148d2-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="148d2-113">Retorna uma cadeia de caracteres identificada por hParameter.</span><span class="sxs-lookup"><span data-stu-id="148d2-113">Returns a string identified by hParameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="148d2-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="148d2-114">Return value</span></span>

<span data-ttu-id="148d2-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="148d2-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="148d2-116">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="148d2-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="148d2-117">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="148d2-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="148d2-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="148d2-118">Requirements</span></span>



| <span data-ttu-id="148d2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="148d2-119">Requirement</span></span> | <span data-ttu-id="148d2-120">Valor</span><span class="sxs-lookup"><span data-stu-id="148d2-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="148d2-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="148d2-121">Header</span></span><br/>  | <dl> <span data-ttu-id="148d2-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="148d2-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="148d2-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="148d2-123">Library</span></span><br/> | <dl> <span data-ttu-id="148d2-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="148d2-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="148d2-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="148d2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="148d2-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="148d2-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="148d2-127">**SetString**</span><span class="sxs-lookup"><span data-stu-id="148d2-127">**SetString**</span></span>](id3dxbaseeffect--setstring.md)
</dt> </dl>

 

 
