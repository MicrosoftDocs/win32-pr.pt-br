---
description: 'Método ID3DXTextureShader:: SetInt – define um valor inteiro.'
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
ms.openlocfilehash: 23c347c35b8accd60bdb81c931ebc3d35b48f957
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117598"
---
# <a name="id3dxtextureshadersetint-method"></a><span data-ttu-id="d6151-103">Método ID3DXTextureShader:: SetInt</span><span class="sxs-lookup"><span data-stu-id="d6151-103">ID3DXTextureShader::SetInt method</span></span>

<span data-ttu-id="d6151-104">Define um valor inteiro.</span><span class="sxs-lookup"><span data-stu-id="d6151-104">Sets an integer value.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6151-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d6151-105">Syntax</span></span>


```C++
HRESULT SetInt(
  [in] D3DXHANDLE hConstant,
  [in] INT        n
);
```



## <a name="parameters"></a><span data-ttu-id="d6151-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d6151-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6151-107">*hConstant* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d6151-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6151-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="d6151-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="d6151-109">Identificador exclusivo para a constante.</span><span class="sxs-lookup"><span data-stu-id="d6151-109">Unique identifier to the constant.</span></span> <span data-ttu-id="d6151-110">Consulte [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="d6151-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="d6151-111">*n* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="d6151-111">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6151-112">Tipo: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d6151-112">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d6151-113">Valor inteiro.</span><span class="sxs-lookup"><span data-stu-id="d6151-113">Integer value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6151-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="d6151-114">Return value</span></span>

<span data-ttu-id="d6151-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d6151-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d6151-116">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d6151-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d6151-117">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d6151-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6151-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6151-118">Requirements</span></span>



| <span data-ttu-id="d6151-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6151-119">Requirement</span></span> | <span data-ttu-id="d6151-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d6151-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6151-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d6151-121">Header</span></span><br/>  | <dl> <span data-ttu-id="d6151-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6151-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="d6151-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d6151-123">Library</span></span><br/> | <dl> <span data-ttu-id="d6151-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d6151-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d6151-125">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d6151-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6151-126">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="d6151-126">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
