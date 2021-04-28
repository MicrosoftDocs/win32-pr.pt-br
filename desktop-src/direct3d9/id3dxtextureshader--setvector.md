---
description: 'Método ID3DXTextureShader:: setvector – define um vetor 4D.'
ms.assetid: befed2a8-7695-4f06-a6ee-aff466d1940a
title: 'Método ID3DXTextureShader:: setvector (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetVector
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e917e4ff13cf7c03de264542dc1995364f1dc526
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090154"
---
# <a name="id3dxtextureshadersetvector-method"></a><span data-ttu-id="69dfa-103">Método ID3DXTextureShader:: setvector</span><span class="sxs-lookup"><span data-stu-id="69dfa-103">ID3DXTextureShader::SetVector method</span></span>

<span data-ttu-id="69dfa-104">Define um vetor 4D.</span><span class="sxs-lookup"><span data-stu-id="69dfa-104">Sets a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="69dfa-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="69dfa-105">Syntax</span></span>


```C++
HRESULT SetVector(
  [in]       D3DXHANDLE  hConstant,
  [in] const D3DXVECTOR4 *pVector
);
```



## <a name="parameters"></a><span data-ttu-id="69dfa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="69dfa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69dfa-107">*hConstant* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="69dfa-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69dfa-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="69dfa-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="69dfa-109">Identificador exclusivo para a constante de vetor.</span><span class="sxs-lookup"><span data-stu-id="69dfa-109">Unique identifier to the vector constant.</span></span> <span data-ttu-id="69dfa-110">Consulte [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="69dfa-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="69dfa-111">*pVector* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="69dfa-111">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69dfa-112">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="69dfa-112">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="69dfa-113">Ponteiro para um vetor 4D.</span><span class="sxs-lookup"><span data-stu-id="69dfa-113">Pointer to a 4D vector.</span></span> <span data-ttu-id="69dfa-114">Consulte [**D3DXVECTOR4**](d3dxvector4.md).</span><span class="sxs-lookup"><span data-stu-id="69dfa-114">See [**D3DXVECTOR4**](d3dxvector4.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69dfa-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="69dfa-115">Return value</span></span>

<span data-ttu-id="69dfa-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="69dfa-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="69dfa-117">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="69dfa-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="69dfa-118">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="69dfa-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="69dfa-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69dfa-119">Requirements</span></span>



| <span data-ttu-id="69dfa-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="69dfa-120">Requirement</span></span> | <span data-ttu-id="69dfa-121">Valor</span><span class="sxs-lookup"><span data-stu-id="69dfa-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="69dfa-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="69dfa-122">Header</span></span><br/>  | <dl> <span data-ttu-id="69dfa-123"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="69dfa-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="69dfa-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="69dfa-124">Library</span></span><br/> | <dl> <span data-ttu-id="69dfa-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="69dfa-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="69dfa-126">Consulte também</span><span class="sxs-lookup"><span data-stu-id="69dfa-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69dfa-127">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="69dfa-127">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




