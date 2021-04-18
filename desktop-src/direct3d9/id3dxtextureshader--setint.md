---
description: Define um valor inteiro.
ms.assetid: e7dcf3f4-1d0c-432a-85fc-0473c49956ff
title: 'Método ID3DXTextureShader:: SetInt (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetInt
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3b440811123935f279b0c4c1661c2a39aa86669f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105787650"
---
# <a name="id3dxtextureshadersetint-method"></a><span data-ttu-id="d0bfb-103">Método ID3DXTextureShader:: SetInt</span><span class="sxs-lookup"><span data-stu-id="d0bfb-103">ID3DXTextureShader::SetInt method</span></span>

<span data-ttu-id="d0bfb-104">Define um valor inteiro.</span><span class="sxs-lookup"><span data-stu-id="d0bfb-104">Sets an integer value.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0bfb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d0bfb-105">Syntax</span></span>


```C++
HRESULT SetInt(
  [in] D3DXHANDLE hConstant,
  [in] INT        n
);
```



## <a name="parameters"></a><span data-ttu-id="d0bfb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d0bfb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0bfb-107">*hConstant* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d0bfb-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0bfb-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="d0bfb-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="d0bfb-109">Identificador exclusivo para a constante.</span><span class="sxs-lookup"><span data-stu-id="d0bfb-109">Unique identifier to the constant.</span></span> <span data-ttu-id="d0bfb-110">Consulte [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="d0bfb-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0bfb-111">*n* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="d0bfb-111">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0bfb-112">Tipo: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d0bfb-112">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d0bfb-113">Valor inteiro.</span><span class="sxs-lookup"><span data-stu-id="d0bfb-113">Integer value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0bfb-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d0bfb-114">Return value</span></span>

<span data-ttu-id="d0bfb-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d0bfb-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d0bfb-116">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d0bfb-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d0bfb-117">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d0bfb-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0bfb-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0bfb-118">Requirements</span></span>



| <span data-ttu-id="d0bfb-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0bfb-119">Requirement</span></span> | <span data-ttu-id="d0bfb-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d0bfb-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0bfb-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d0bfb-121">Header</span></span><br/>  | <dl> <span data-ttu-id="d0bfb-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0bfb-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="d0bfb-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d0bfb-123">Library</span></span><br/> | <dl> <span data-ttu-id="d0bfb-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d0bfb-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d0bfb-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="d0bfb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0bfb-126">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="d0bfb-126">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
