---
description: Obtém um sombreador de pixel.
ms.assetid: 173a20a5-dda0-493f-a161-2dc2881e71f2
title: 'Método ID3DXBaseEffect:: GetPixelShader (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetPixelShader
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e555bac2e20ebab1cb0aec3d313cab8ad05e833e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105802080"
---
# <a name="id3dxbaseeffectgetpixelshader-method"></a><span data-ttu-id="29679-103">Método ID3DXBaseEffect:: GetPixelShader</span><span class="sxs-lookup"><span data-stu-id="29679-103">ID3DXBaseEffect::GetPixelShader method</span></span>

<span data-ttu-id="29679-104">Obtém um sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="29679-104">Gets a pixel shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="29679-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="29679-105">Syntax</span></span>


```C++
HRESULT GetPixelShader(
  [in]  D3DXHANDLE             hParameter,
  [out] LPDIRECT3DPIXELSHADER9 *ppPShader
);
```



## <a name="parameters"></a><span data-ttu-id="29679-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="29679-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29679-107">*hParameter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="29679-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29679-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="29679-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="29679-109">Identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="29679-109">Unique identifier.</span></span> <span data-ttu-id="29679-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="29679-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="29679-111">*ppPShader* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="29679-111">*ppPShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="29679-112">Tipo: **[ **LPDIRECT3DPIXELSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9)\***</span><span class="sxs-lookup"><span data-stu-id="29679-112">Type: **[**LPDIRECT3DPIXELSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9)\***</span></span>

<span data-ttu-id="29679-113">Retorna um objeto de sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="29679-113">Returns a pixel shader object.</span></span> <span data-ttu-id="29679-114">Consulte o objeto [**IDirect3DPixelShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9) .</span><span class="sxs-lookup"><span data-stu-id="29679-114">See [**IDirect3DPixelShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29679-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="29679-115">Return value</span></span>

<span data-ttu-id="29679-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="29679-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="29679-117">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="29679-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="29679-118">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="29679-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="29679-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29679-119">Requirements</span></span>



| <span data-ttu-id="29679-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="29679-120">Requirement</span></span> | <span data-ttu-id="29679-121">Valor</span><span class="sxs-lookup"><span data-stu-id="29679-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="29679-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="29679-122">Header</span></span><br/>  | <dl> <span data-ttu-id="29679-123"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="29679-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="29679-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="29679-124">Library</span></span><br/> | <dl> <span data-ttu-id="29679-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="29679-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="29679-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="29679-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29679-127">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="29679-127">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
