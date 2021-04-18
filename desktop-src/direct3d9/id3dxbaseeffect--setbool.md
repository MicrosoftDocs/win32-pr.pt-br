---
description: Define um valor BOOL.
ms.assetid: bb7c4860-50a0-416a-b9e0-5a2bec113e3c
title: 'Método ID3DXBaseEffect:: setbool (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetBool
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: be137ac210297b9fce12dafaffb6fead61d39512
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105787720"
---
# <a name="id3dxbaseeffectsetbool-method"></a><span data-ttu-id="be221-103">Método ID3DXBaseEffect:: setbool</span><span class="sxs-lookup"><span data-stu-id="be221-103">ID3DXBaseEffect::SetBool method</span></span>

<span data-ttu-id="be221-104">Define um valor BOOL.</span><span class="sxs-lookup"><span data-stu-id="be221-104">Sets a BOOL value.</span></span>

## <a name="syntax"></a><span data-ttu-id="be221-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="be221-105">Syntax</span></span>


```C++
HRESULT SetBool(
  [in] D3DXHANDLE hParameter,
  [in] BOOL       b
);
```



## <a name="parameters"></a><span data-ttu-id="be221-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="be221-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be221-107">*hParameter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="be221-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be221-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="be221-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="be221-109">Identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="be221-109">Unique identifier.</span></span> <span data-ttu-id="be221-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="be221-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="be221-111">*b* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="be221-111">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be221-112">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="be221-112">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="be221-113">$True.</span><span class="sxs-lookup"><span data-stu-id="be221-113">Boolean value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be221-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="be221-114">Return value</span></span>

<span data-ttu-id="be221-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="be221-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="be221-116">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="be221-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="be221-117">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="be221-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="be221-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be221-118">Requirements</span></span>



| <span data-ttu-id="be221-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="be221-119">Requirement</span></span> | <span data-ttu-id="be221-120">Valor</span><span class="sxs-lookup"><span data-stu-id="be221-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="be221-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="be221-121">Header</span></span><br/>  | <dl> <span data-ttu-id="be221-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="be221-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="be221-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="be221-123">Library</span></span><br/> | <dl> <span data-ttu-id="be221-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be221-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="be221-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="be221-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be221-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="be221-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="be221-127">**Getbool**</span><span class="sxs-lookup"><span data-stu-id="be221-127">**GetBool**</span></span>](id3dxbaseeffect--getbool.md)
</dt> </dl>

 

 
