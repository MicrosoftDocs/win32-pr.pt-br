---
description: Define um número inteiro.
ms.assetid: 1090d4a6-b4f5-4e15-a49f-e2724f1c3f95
title: 'Método ID3DXBaseEffect:: SetInt (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetInt
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 3c27d66544d4064c8d6c682db168b57b88d213cd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298471"
---
# <a name="id3dxbaseeffectsetint-method"></a><span data-ttu-id="04b37-103">Método ID3DXBaseEffect:: SetInt</span><span class="sxs-lookup"><span data-stu-id="04b37-103">ID3DXBaseEffect::SetInt method</span></span>

<span data-ttu-id="04b37-104">Define um número inteiro.</span><span class="sxs-lookup"><span data-stu-id="04b37-104">Sets an integer.</span></span>

## <a name="syntax"></a><span data-ttu-id="04b37-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="04b37-105">Syntax</span></span>


```C++
HRESULT SetInt(
  [in] D3DXHANDLE hParameter,
  [in] INT        n
);
```



## <a name="parameters"></a><span data-ttu-id="04b37-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="04b37-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04b37-107">*hParameter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="04b37-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04b37-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="04b37-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="04b37-109">Identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="04b37-109">Unique identifier.</span></span> <span data-ttu-id="04b37-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="04b37-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="04b37-111">*n* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="04b37-111">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04b37-112">Tipo: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="04b37-112">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="04b37-113">Valor inteiro.</span><span class="sxs-lookup"><span data-stu-id="04b37-113">Integer value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04b37-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="04b37-114">Return value</span></span>

<span data-ttu-id="04b37-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="04b37-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="04b37-116">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="04b37-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="04b37-117">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="04b37-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="04b37-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04b37-118">Requirements</span></span>



| <span data-ttu-id="04b37-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="04b37-119">Requirement</span></span> | <span data-ttu-id="04b37-120">Valor</span><span class="sxs-lookup"><span data-stu-id="04b37-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="04b37-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="04b37-121">Header</span></span><br/>  | <dl> <span data-ttu-id="04b37-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="04b37-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="04b37-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="04b37-123">Library</span></span><br/> | <dl> <span data-ttu-id="04b37-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="04b37-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="04b37-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="04b37-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04b37-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="04b37-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="04b37-127">**GetInt**</span><span class="sxs-lookup"><span data-stu-id="04b37-127">**GetInt**</span></span>](id3dxbaseeffect--getint.md)
</dt> </dl>

 

 
