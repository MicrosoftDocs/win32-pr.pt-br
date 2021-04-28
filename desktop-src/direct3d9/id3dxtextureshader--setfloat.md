---
description: 'Método ID3DXTextureShader:: SetFloat – define um número de ponto flutuante.'
ms.assetid: 69bb9b15-5d66-4b1a-9559-29bcb38a965f
title: 'Método ID3DXTextureShader:: SetFloat (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetFloat
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6230b0736cb3bc623b0413f7b5a1cb9635f00e07
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107164"
---
# <a name="id3dxtextureshadersetfloat-method"></a><span data-ttu-id="52a68-103">Método ID3DXTextureShader:: SetFloat</span><span class="sxs-lookup"><span data-stu-id="52a68-103">ID3DXTextureShader::SetFloat method</span></span>

<span data-ttu-id="52a68-104">Define um número de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="52a68-104">Sets a floating-point number.</span></span>

## <a name="syntax"></a><span data-ttu-id="52a68-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="52a68-105">Syntax</span></span>


```C++
HRESULT SetFloat(
  [in] D3DXHANDLE hConstant,
  [in] FLOAT      f
);
```



## <a name="parameters"></a><span data-ttu-id="52a68-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="52a68-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52a68-107">*hConstant* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="52a68-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52a68-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="52a68-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="52a68-109">Identificador exclusivo para a constante.</span><span class="sxs-lookup"><span data-stu-id="52a68-109">Unique identifier to the constant.</span></span> <span data-ttu-id="52a68-110">Consulte [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="52a68-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="52a68-111">*f* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="52a68-111">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52a68-112">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="52a68-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="52a68-113">Número de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="52a68-113">Floating-point number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52a68-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="52a68-114">Return value</span></span>

<span data-ttu-id="52a68-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="52a68-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="52a68-116">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="52a68-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="52a68-117">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="52a68-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="52a68-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52a68-118">Requirements</span></span>



| <span data-ttu-id="52a68-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="52a68-119">Requirement</span></span> | <span data-ttu-id="52a68-120">Valor</span><span class="sxs-lookup"><span data-stu-id="52a68-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="52a68-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="52a68-121">Header</span></span><br/>  | <dl> <span data-ttu-id="52a68-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="52a68-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="52a68-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="52a68-123">Library</span></span><br/> | <dl> <span data-ttu-id="52a68-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="52a68-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="52a68-125">Consulte também</span><span class="sxs-lookup"><span data-stu-id="52a68-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52a68-126">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="52a68-126">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
