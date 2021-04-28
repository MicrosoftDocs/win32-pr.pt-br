---
description: 'Método ID3DXTextureShader:: setbool – define um valor BOOL.'
ms.assetid: 0d3c1f3a-f497-4e92-81e9-8647006910e1
title: 'Método ID3DXTextureShader:: setbool (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetBool
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 512daf7e770c72fe038622877d1756a5fd3532bf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117624"
---
# <a name="id3dxtextureshadersetbool-method"></a><span data-ttu-id="2fcbc-103">Método ID3DXTextureShader:: setbool</span><span class="sxs-lookup"><span data-stu-id="2fcbc-103">ID3DXTextureShader::SetBool method</span></span>

<span data-ttu-id="2fcbc-104">Define um valor BOOL.</span><span class="sxs-lookup"><span data-stu-id="2fcbc-104">Sets a BOOL value.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fcbc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2fcbc-105">Syntax</span></span>


```C++
HRESULT SetBool(
  [in] D3DXHANDLE hConstant,
  [in] BOOL       b
);
```



## <a name="parameters"></a><span data-ttu-id="2fcbc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2fcbc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fcbc-107">*hConstant* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2fcbc-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fcbc-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="2fcbc-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="2fcbc-109">Identificador exclusivo para a constante.</span><span class="sxs-lookup"><span data-stu-id="2fcbc-109">Unique identifier to the constant.</span></span> <span data-ttu-id="2fcbc-110">Consulte [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="2fcbc-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="2fcbc-111">*b* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="2fcbc-111">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fcbc-112">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2fcbc-112">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2fcbc-113">Valor BOOL.</span><span class="sxs-lookup"><span data-stu-id="2fcbc-113">BOOL value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fcbc-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="2fcbc-114">Return value</span></span>

<span data-ttu-id="2fcbc-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2fcbc-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2fcbc-116">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2fcbc-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2fcbc-117">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="2fcbc-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fcbc-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2fcbc-118">Requirements</span></span>



| <span data-ttu-id="2fcbc-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fcbc-119">Requirement</span></span> | <span data-ttu-id="2fcbc-120">Valor</span><span class="sxs-lookup"><span data-stu-id="2fcbc-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fcbc-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2fcbc-121">Header</span></span><br/>  | <dl> <span data-ttu-id="2fcbc-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fcbc-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="2fcbc-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2fcbc-123">Library</span></span><br/> | <dl> <span data-ttu-id="2fcbc-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2fcbc-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2fcbc-125">Consulte também</span><span class="sxs-lookup"><span data-stu-id="2fcbc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fcbc-126">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="2fcbc-126">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
