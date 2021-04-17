---
description: Define um vetor 4D.
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
ms.openlocfilehash: b7bc7e3b7f4920c21c52111410c626090e452fa7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105755768"
---
# <a name="id3dxtextureshadersetvector-method"></a><span data-ttu-id="22314-103">Método ID3DXTextureShader:: setvector</span><span class="sxs-lookup"><span data-stu-id="22314-103">ID3DXTextureShader::SetVector method</span></span>

<span data-ttu-id="22314-104">Define um vetor 4D.</span><span class="sxs-lookup"><span data-stu-id="22314-104">Sets a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="22314-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="22314-105">Syntax</span></span>


```C++
HRESULT SetVector(
  [in]       D3DXHANDLE  hConstant,
  [in] const D3DXVECTOR4 *pVector
);
```



## <a name="parameters"></a><span data-ttu-id="22314-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="22314-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22314-107">*hConstant* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="22314-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22314-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="22314-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="22314-109">Identificador exclusivo para a constante de vetor.</span><span class="sxs-lookup"><span data-stu-id="22314-109">Unique identifier to the vector constant.</span></span> <span data-ttu-id="22314-110">Consulte [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="22314-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="22314-111">*pVector* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="22314-111">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22314-112">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="22314-112">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="22314-113">Ponteiro para um vetor 4D.</span><span class="sxs-lookup"><span data-stu-id="22314-113">Pointer to a 4D vector.</span></span> <span data-ttu-id="22314-114">Consulte [**D3DXVECTOR4**](d3dxvector4.md).</span><span class="sxs-lookup"><span data-stu-id="22314-114">See [**D3DXVECTOR4**](d3dxvector4.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22314-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="22314-115">Return value</span></span>

<span data-ttu-id="22314-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="22314-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="22314-117">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="22314-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="22314-118">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="22314-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="22314-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22314-119">Requirements</span></span>



| <span data-ttu-id="22314-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="22314-120">Requirement</span></span> | <span data-ttu-id="22314-121">Valor</span><span class="sxs-lookup"><span data-stu-id="22314-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="22314-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="22314-122">Header</span></span><br/>  | <dl> <span data-ttu-id="22314-123"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="22314-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="22314-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="22314-124">Library</span></span><br/> | <dl> <span data-ttu-id="22314-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="22314-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="22314-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="22314-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22314-127">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="22314-127">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




