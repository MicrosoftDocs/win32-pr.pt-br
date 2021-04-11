---
description: Define uma matriz de números de ponto flutuante.
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
ms.openlocfilehash: 5dbd39e8a4acfa004fb623d578e5922d477884fc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173027"
---
# <a name="id3dxtextureshadersetfloatarray-method"></a><span data-ttu-id="460c1-103">Método ID3DXTextureShader:: SetFloatArray</span><span class="sxs-lookup"><span data-stu-id="460c1-103">ID3DXTextureShader::SetFloatArray method</span></span>

<span data-ttu-id="460c1-104">Define uma matriz de números de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="460c1-104">Sets an array of floating-point numbers.</span></span>

## <a name="syntax"></a><span data-ttu-id="460c1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="460c1-105">Syntax</span></span>


```C++
HRESULT SetFloatArray(
  [in]       D3DXHANDLE hConstant,
  [in] const FLOAT      *pf,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="460c1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="460c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="460c1-107">*hConstant* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="460c1-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="460c1-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="460c1-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="460c1-109">Identificador exclusivo para a matriz de constantes.</span><span class="sxs-lookup"><span data-stu-id="460c1-109">Unique identifier to the array of constants.</span></span> <span data-ttu-id="460c1-110">Consulte [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="460c1-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="460c1-111">*PF* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="460c1-111">*pf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="460c1-112">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="460c1-112">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="460c1-113">Matriz de números de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="460c1-113">Array of floating-point numbers.</span></span>

</dd> <dt>

<span data-ttu-id="460c1-114">*Contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="460c1-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="460c1-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="460c1-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="460c1-116">Número de valores de ponto flutuante na matriz.</span><span class="sxs-lookup"><span data-stu-id="460c1-116">Number of floating-point values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="460c1-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="460c1-117">Return value</span></span>

<span data-ttu-id="460c1-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="460c1-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="460c1-119">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="460c1-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="460c1-120">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="460c1-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="460c1-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="460c1-121">Requirements</span></span>



| <span data-ttu-id="460c1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="460c1-122">Requirement</span></span> | <span data-ttu-id="460c1-123">Valor</span><span class="sxs-lookup"><span data-stu-id="460c1-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="460c1-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="460c1-124">Header</span></span><br/>  | <dl> <span data-ttu-id="460c1-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="460c1-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="460c1-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="460c1-126">Library</span></span><br/> | <dl> <span data-ttu-id="460c1-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="460c1-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="460c1-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="460c1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="460c1-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="460c1-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
