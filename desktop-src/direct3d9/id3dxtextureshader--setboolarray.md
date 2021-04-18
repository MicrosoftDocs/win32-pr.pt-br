---
description: Define uma matriz de valores BOOL.
ms.assetid: d168d362-86b3-4db4-bc52-748a640ebc18
title: 'Método ID3DXTextureShader:: SetBoolArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetBoolArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0799e4ef9d35a886e59fae44c37a841bcda3aed6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105763269"
---
# <a name="id3dxtextureshadersetboolarray-method"></a><span data-ttu-id="bf915-103">Método ID3DXTextureShader:: SetBoolArray</span><span class="sxs-lookup"><span data-stu-id="bf915-103">ID3DXTextureShader::SetBoolArray method</span></span>

<span data-ttu-id="bf915-104">Define uma matriz de valores BOOL.</span><span class="sxs-lookup"><span data-stu-id="bf915-104">Sets an array of BOOL values.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf915-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bf915-105">Syntax</span></span>


```C++
HRESULT SetBoolArray(
  [in]       D3DXHANDLE hConstant,
  [in] const BOOL       *pB,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="bf915-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bf915-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf915-107">*hConstant* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bf915-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf915-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="bf915-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="bf915-109">Identificador exclusivo para a matriz de constantes.</span><span class="sxs-lookup"><span data-stu-id="bf915-109">Unique identifier to the array of constants.</span></span> <span data-ttu-id="bf915-110">Consulte [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="bf915-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="bf915-111">*PB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bf915-111">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf915-112">Tipo: **const [**bool**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="bf915-112">Type: **const [**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="bf915-113">Matriz de valores BOOL.</span><span class="sxs-lookup"><span data-stu-id="bf915-113">Array of BOOL values.</span></span>

</dd> <dt>

<span data-ttu-id="bf915-114">*Contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="bf915-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf915-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bf915-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bf915-116">Número de valores BOOL na matriz.</span><span class="sxs-lookup"><span data-stu-id="bf915-116">Number of BOOL values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf915-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bf915-117">Return value</span></span>

<span data-ttu-id="bf915-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bf915-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bf915-119">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bf915-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="bf915-120">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="bf915-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf915-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf915-121">Requirements</span></span>



| <span data-ttu-id="bf915-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf915-122">Requirement</span></span> | <span data-ttu-id="bf915-123">Valor</span><span class="sxs-lookup"><span data-stu-id="bf915-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf915-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bf915-124">Header</span></span><br/>  | <dl> <span data-ttu-id="bf915-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf915-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="bf915-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bf915-126">Library</span></span><br/> | <dl> <span data-ttu-id="bf915-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bf915-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="bf915-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="bf915-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf915-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="bf915-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
