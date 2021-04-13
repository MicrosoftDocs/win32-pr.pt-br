---
description: Cria um objeto de sombreador de textura do sombreador compilado.
ms.assetid: 3e8017f7-fe6b-4f4e-a80e-b16b16c0b348
title: Função D3DXCreateTextureShader (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c32715f1b939d30acb53b1cbe07e081d43d21823
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298630"
---
# <a name="d3dxcreatetextureshader-function"></a><span data-ttu-id="ac827-103">Função D3DXCreateTextureShader</span><span class="sxs-lookup"><span data-stu-id="ac827-103">D3DXCreateTextureShader function</span></span>

<span data-ttu-id="ac827-104">Cria um objeto de sombreador de textura do sombreador compilado.</span><span class="sxs-lookup"><span data-stu-id="ac827-104">Creates a texture shader object from the compiled shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac827-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ac827-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureShader(
  _In_  const DWORD               *pFunction,
  _Out_       LPD3DXTEXTURESHADER *ppTextureShader
);
```



## <a name="parameters"></a><span data-ttu-id="ac827-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ac827-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac827-107">*pFunction* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ac827-107">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac827-108">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="ac827-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ac827-109">Ponteiro para a função de fluxo DWORD.</span><span class="sxs-lookup"><span data-stu-id="ac827-109">Pointer to the function DWORD stream.</span></span>

</dd> <dt>

<span data-ttu-id="ac827-110">*ppTextureShader* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ac827-110">*ppTextureShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac827-111">Tipo: **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)\***</span><span class="sxs-lookup"><span data-stu-id="ac827-111">Type: **[**LPD3DXTEXTURESHADER**](id3dxtextureshader.md)\***</span></span>

<span data-ttu-id="ac827-112">Retorna um objeto [**ID3DXTextureShader**](id3dxtextureshader.md) que pode ser usado para preencher de procedimento o conteúdo de uma textura usando as funções [**D3DXFillTextureTX**](d3dxfilltexturetx.md) .</span><span class="sxs-lookup"><span data-stu-id="ac827-112">Returns an [**ID3DXTextureShader**](id3dxtextureshader.md) object which can be used to procedurally fill the contents of a texture using the [**D3DXFillTextureTX**](d3dxfilltexturetx.md) functions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac827-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ac827-113">Return value</span></span>

<span data-ttu-id="ac827-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ac827-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ac827-115">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ac827-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ac827-116">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="ac827-116">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac827-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac827-117">Requirements</span></span>



| <span data-ttu-id="ac827-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac827-118">Requirement</span></span> | <span data-ttu-id="ac827-119">Valor</span><span class="sxs-lookup"><span data-stu-id="ac827-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac827-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ac827-120">Header</span></span><br/>  | <dl> <span data-ttu-id="ac827-121"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac827-121"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="ac827-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ac827-122">Library</span></span><br/> | <dl> <span data-ttu-id="ac827-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac827-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ac827-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="ac827-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac827-125">Funções de sombreador</span><span class="sxs-lookup"><span data-stu-id="ac827-125">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
