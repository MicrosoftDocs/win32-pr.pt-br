---
description: Define um número de ponto flutuante.
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
ms.openlocfilehash: 85923fe20731b4482f70c439cb9df75712ab09f5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105748861"
---
# <a name="id3dxtextureshadersetfloat-method"></a><span data-ttu-id="92488-103">Método ID3DXTextureShader:: SetFloat</span><span class="sxs-lookup"><span data-stu-id="92488-103">ID3DXTextureShader::SetFloat method</span></span>

<span data-ttu-id="92488-104">Define um número de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="92488-104">Sets a floating-point number.</span></span>

## <a name="syntax"></a><span data-ttu-id="92488-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="92488-105">Syntax</span></span>


```C++
HRESULT SetFloat(
  [in] D3DXHANDLE hConstant,
  [in] FLOAT      f
);
```



## <a name="parameters"></a><span data-ttu-id="92488-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="92488-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92488-107">*hConstant* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="92488-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92488-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="92488-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="92488-109">Identificador exclusivo para a constante.</span><span class="sxs-lookup"><span data-stu-id="92488-109">Unique identifier to the constant.</span></span> <span data-ttu-id="92488-110">Consulte [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="92488-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="92488-111">*f* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="92488-111">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92488-112">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="92488-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="92488-113">Número de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="92488-113">Floating-point number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92488-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="92488-114">Return value</span></span>

<span data-ttu-id="92488-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="92488-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="92488-116">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="92488-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="92488-117">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="92488-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="92488-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92488-118">Requirements</span></span>



| <span data-ttu-id="92488-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="92488-119">Requirement</span></span> | <span data-ttu-id="92488-120">Valor</span><span class="sxs-lookup"><span data-stu-id="92488-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="92488-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="92488-121">Header</span></span><br/>  | <dl> <span data-ttu-id="92488-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="92488-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="92488-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="92488-123">Library</span></span><br/> | <dl> <span data-ttu-id="92488-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="92488-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="92488-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="92488-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92488-126">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="92488-126">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
