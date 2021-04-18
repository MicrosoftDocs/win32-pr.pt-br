---
description: Define uma cadeia de caracteres.
ms.assetid: 7e8eef70-85ee-461d-bf8c-44cda5f184cd
title: 'Método ID3DXBaseEffect:: SetString (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetString
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 1a7c4f86c6b7fa78c869eb1d5bd49634ec4b496d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105793730"
---
# <a name="id3dxbaseeffectsetstring-method"></a><span data-ttu-id="ea467-103">Método ID3DXBaseEffect:: SetString</span><span class="sxs-lookup"><span data-stu-id="ea467-103">ID3DXBaseEffect::SetString method</span></span>

<span data-ttu-id="ea467-104">Define uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="ea467-104">Sets a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea467-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ea467-105">Syntax</span></span>


```C++
HRESULT SetString(
  [in] D3DXHANDLE hParameter,
  [in] LPCSTR     pString
);
```



## <a name="parameters"></a><span data-ttu-id="ea467-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ea467-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea467-107">*hParameter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ea467-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea467-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="ea467-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="ea467-109">Identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="ea467-109">Unique identifier.</span></span> <span data-ttu-id="ea467-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="ea467-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea467-111">*pString* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ea467-111">*pString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea467-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ea467-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ea467-113">Cadeia de caracteres a ser definida.</span><span class="sxs-lookup"><span data-stu-id="ea467-113">String to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea467-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ea467-114">Return value</span></span>

<span data-ttu-id="ea467-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ea467-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ea467-116">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ea467-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ea467-117">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="ea467-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea467-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea467-118">Requirements</span></span>



| <span data-ttu-id="ea467-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea467-119">Requirement</span></span> | <span data-ttu-id="ea467-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ea467-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea467-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ea467-121">Header</span></span><br/>  | <dl> <span data-ttu-id="ea467-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea467-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="ea467-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ea467-123">Library</span></span><br/> | <dl> <span data-ttu-id="ea467-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea467-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ea467-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="ea467-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea467-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="ea467-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="ea467-127">**GetString**</span><span class="sxs-lookup"><span data-stu-id="ea467-127">**GetString**</span></span>](id3dxbaseeffect--getstring.md)
</dt> </dl>

 

 
