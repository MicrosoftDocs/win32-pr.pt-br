---
description: 'Método ID3DXTextureShader:: SetVectorArray – define uma matriz de vetores 4D.'
ms.assetid: 45bc5cb1-b44a-468b-8c80-a639da8a033f
title: 'Método ID3DXTextureShader:: SetVectorArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetVectorArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0878594baa8828c9cca4eca8dd2c20f225fb530e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090184"
---
# <a name="id3dxtextureshadersetvectorarray-method"></a><span data-ttu-id="8896b-103">Método ID3DXTextureShader:: SetVectorArray</span><span class="sxs-lookup"><span data-stu-id="8896b-103">ID3DXTextureShader::SetVectorArray method</span></span>

<span data-ttu-id="8896b-104">Define uma matriz de vetores 4D.</span><span class="sxs-lookup"><span data-stu-id="8896b-104">Sets an array of 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="8896b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8896b-105">Syntax</span></span>


```C++
HRESULT SetVectorArray(
  [in]       D3DXHANDLE  hConstant,
  [in] const D3DXVECTOR4 *pVector,
  [in]       UINT        Count
);
```



## <a name="parameters"></a><span data-ttu-id="8896b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8896b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8896b-107">*hConstant* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8896b-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8896b-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="8896b-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="8896b-109">Identificador exclusivo para a matriz de constantes de vetor.</span><span class="sxs-lookup"><span data-stu-id="8896b-109">Unique identifier to the array of vector constants.</span></span> <span data-ttu-id="8896b-110">Consulte [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="8896b-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="8896b-111">*pVector* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8896b-111">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8896b-112">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="8896b-112">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="8896b-113">Matriz de vetores 4D.</span><span class="sxs-lookup"><span data-stu-id="8896b-113">Array of 4D vectors.</span></span> <span data-ttu-id="8896b-114">Consulte [**D3DXVECTOR4**](d3dxvector4.md).</span><span class="sxs-lookup"><span data-stu-id="8896b-114">See [**D3DXVECTOR4**](d3dxvector4.md).</span></span>

</dd> <dt>

<span data-ttu-id="8896b-115">*Contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="8896b-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8896b-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8896b-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8896b-117">Número de vetores na matriz.</span><span class="sxs-lookup"><span data-stu-id="8896b-117">Number of vectors in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8896b-118">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="8896b-118">Return value</span></span>

<span data-ttu-id="8896b-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8896b-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8896b-120">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8896b-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8896b-121">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="8896b-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="8896b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8896b-122">Requirements</span></span>



| <span data-ttu-id="8896b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8896b-123">Requirement</span></span> | <span data-ttu-id="8896b-124">Valor</span><span class="sxs-lookup"><span data-stu-id="8896b-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8896b-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8896b-125">Header</span></span><br/>  | <dl> <span data-ttu-id="8896b-126"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="8896b-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="8896b-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8896b-127">Library</span></span><br/> | <dl> <span data-ttu-id="8896b-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8896b-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="8896b-129">Consulte também</span><span class="sxs-lookup"><span data-stu-id="8896b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8896b-130">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="8896b-130">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
