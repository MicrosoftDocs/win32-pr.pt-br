---
description: Define uma matriz de inteiros.
ms.assetid: 1ceb8bb0-d168-49cf-8964-8ae582b5ec2e
title: 'Método ID3DXTextureShader:: SetIntArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetIntArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d2e43ac1451ec776339d7aba1a4b0288e948f43d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105772490"
---
# <a name="id3dxtextureshadersetintarray-method"></a><span data-ttu-id="c7417-103">Método ID3DXTextureShader:: SetIntArray</span><span class="sxs-lookup"><span data-stu-id="c7417-103">ID3DXTextureShader::SetIntArray method</span></span>

<span data-ttu-id="c7417-104">Define uma matriz de inteiros.</span><span class="sxs-lookup"><span data-stu-id="c7417-104">Sets an array of integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7417-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c7417-105">Syntax</span></span>


```C++
HRESULT SetIntArray(
  [in]       D3DXHANDLE hConstant,
  [in] const INT        *pn,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="c7417-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c7417-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7417-107">*hConstant* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c7417-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7417-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="c7417-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="c7417-109">Identificador exclusivo para a matriz de constantes.</span><span class="sxs-lookup"><span data-stu-id="c7417-109">Unique identifier to the array of constants.</span></span> <span data-ttu-id="c7417-110">Consulte [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="c7417-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7417-111">*PN* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c7417-111">*pn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7417-112">Tipo: **const [**int**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="c7417-112">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c7417-113">Matriz de inteiros.</span><span class="sxs-lookup"><span data-stu-id="c7417-113">Array of integers.</span></span>

</dd> <dt>

<span data-ttu-id="c7417-114">*Contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="c7417-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7417-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c7417-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c7417-116">Número de inteiros na matriz.</span><span class="sxs-lookup"><span data-stu-id="c7417-116">Number of integers in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7417-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c7417-117">Return value</span></span>

<span data-ttu-id="c7417-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c7417-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c7417-119">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c7417-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c7417-120">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="c7417-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7417-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7417-121">Requirements</span></span>



| <span data-ttu-id="c7417-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7417-122">Requirement</span></span> | <span data-ttu-id="c7417-123">Valor</span><span class="sxs-lookup"><span data-stu-id="c7417-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7417-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c7417-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c7417-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7417-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="c7417-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c7417-126">Library</span></span><br/> | <dl> <span data-ttu-id="c7417-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c7417-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c7417-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="c7417-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7417-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="c7417-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
