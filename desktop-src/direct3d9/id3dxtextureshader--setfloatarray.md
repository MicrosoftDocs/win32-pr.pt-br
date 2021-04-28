---
description: 'Método ID3DXTextureShader:: SetFloatArray – define uma matriz de números de ponto flutuante.'
ms.assetid: 8e64b569-a6bf-4925-9d21-4df0b6661ee2
title: 'Método ID3DXTextureShader:: SetFloatArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetFloatArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bd42455e16cbfc203f76de868a82935e0e25401f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090244"
---
# <a name="id3dxtextureshadersetfloatarray-method"></a><span data-ttu-id="10cd4-103">Método ID3DXTextureShader:: SetFloatArray</span><span class="sxs-lookup"><span data-stu-id="10cd4-103">ID3DXTextureShader::SetFloatArray method</span></span>

<span data-ttu-id="10cd4-104">Define uma matriz de números de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="10cd4-104">Sets an array of floating-point numbers.</span></span>

## <a name="syntax"></a><span data-ttu-id="10cd4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="10cd4-105">Syntax</span></span>


```C++
HRESULT SetFloatArray(
  [in]       D3DXHANDLE hConstant,
  [in] const FLOAT      *pf,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="10cd4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="10cd4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10cd4-107">*hConstant* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="10cd4-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10cd4-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="10cd4-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="10cd4-109">Identificador exclusivo para a matriz de constantes.</span><span class="sxs-lookup"><span data-stu-id="10cd4-109">Unique identifier to the array of constants.</span></span> <span data-ttu-id="10cd4-110">Consulte [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="10cd4-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="10cd4-111">*PF* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="10cd4-111">*pf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10cd4-112">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="10cd4-112">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="10cd4-113">Matriz de números de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="10cd4-113">Array of floating-point numbers.</span></span>

</dd> <dt>

<span data-ttu-id="10cd4-114">*Contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="10cd4-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10cd4-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="10cd4-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="10cd4-116">Número de valores de ponto flutuante na matriz.</span><span class="sxs-lookup"><span data-stu-id="10cd4-116">Number of floating-point values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10cd4-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="10cd4-117">Return value</span></span>

<span data-ttu-id="10cd4-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="10cd4-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="10cd4-119">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="10cd4-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="10cd4-120">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="10cd4-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="10cd4-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10cd4-121">Requirements</span></span>



| <span data-ttu-id="10cd4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="10cd4-122">Requirement</span></span> | <span data-ttu-id="10cd4-123">Valor</span><span class="sxs-lookup"><span data-stu-id="10cd4-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="10cd4-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="10cd4-124">Header</span></span><br/>  | <dl> <span data-ttu-id="10cd4-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="10cd4-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="10cd4-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="10cd4-126">Library</span></span><br/> | <dl> <span data-ttu-id="10cd4-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="10cd4-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="10cd4-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="10cd4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10cd4-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="10cd4-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
