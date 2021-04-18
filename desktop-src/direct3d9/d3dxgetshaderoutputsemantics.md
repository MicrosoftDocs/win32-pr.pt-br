---
description: Obtenha a semântica para todos os elementos de saída do sombreador.
ms.assetid: 1a3cdd5d-0ea7-48ae-a3f1-030e95b03a42
title: Função D3DXGetShaderOutputSemantics (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderOutputSemantics
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 264db967d2959c2f6e5096e0362e9db576ba9f94
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104506477"
---
# <a name="d3dxgetshaderoutputsemantics-function"></a><span data-ttu-id="0d4fb-103">Função D3DXGetShaderOutputSemantics</span><span class="sxs-lookup"><span data-stu-id="0d4fb-103">D3DXGetShaderOutputSemantics function</span></span>

<span data-ttu-id="0d4fb-104">Obtenha a semântica para todos os elementos de saída do sombreador.</span><span class="sxs-lookup"><span data-stu-id="0d4fb-104">Get the semantics for all shader output elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d4fb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0d4fb-105">Syntax</span></span>


```C++
HRESULT D3DXGetShaderOutputSemantics(
  _In_  const DWORD        *pFunction,
  _In_        D3DXSEMANTIC *pSemantics,
  _Out_       UINT         *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="0d4fb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0d4fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d4fb-107">*pFunction* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0d4fb-107">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d4fb-108">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="0d4fb-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0d4fb-109">Ponteiro para o fluxo DWORD da função de sombreador.</span><span class="sxs-lookup"><span data-stu-id="0d4fb-109">Pointer to the shader function DWORD stream.</span></span>

</dd> <dt>

<span data-ttu-id="0d4fb-110">*pSemantics* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0d4fb-110">*pSemantics* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d4fb-111">Tipo: **[ **D3DXSEMANTIC**](d3dxsemantic.md)\***</span><span class="sxs-lookup"><span data-stu-id="0d4fb-111">Type: **[**D3DXSEMANTIC**](d3dxsemantic.md)\***</span></span>

<span data-ttu-id="0d4fb-112">Ponteiro para uma matriz de estruturas [**D3DXSEMANTIC**](d3dxsemantic.md) .</span><span class="sxs-lookup"><span data-stu-id="0d4fb-112">Pointer to an array of [**D3DXSEMANTIC**](d3dxsemantic.md) structures.</span></span> <span data-ttu-id="0d4fb-113">A função preencherá essa matriz com a semântica para cada elemento de saída referenciado pelo sombreador.</span><span class="sxs-lookup"><span data-stu-id="0d4fb-113">The function will fill this array with the semantics for each output element referenced by the shader.</span></span> <span data-ttu-id="0d4fb-114">Presume-se que essa matriz contenha pelo menos elementos MAXD3DDECLLENGTH.</span><span class="sxs-lookup"><span data-stu-id="0d4fb-114">This array is assumed to contain at least MAXD3DDECLLENGTH elements.</span></span> <span data-ttu-id="0d4fb-115">No entanto, chamar **D3DXGetShaderOutputSemantics** com PSemantics = **NULL** retornará o número de elementos necessários para pCount.</span><span class="sxs-lookup"><span data-stu-id="0d4fb-115">However, calling **D3DXGetShaderOutputSemantics** with pSemantics = **NULL** will return the number of elements needed for pCount.</span></span>

</dd> <dt>

<span data-ttu-id="0d4fb-116">*pCount* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0d4fb-116">*pCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d4fb-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0d4fb-117">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0d4fb-118">Retorna o número de elementos em pSemantics.</span><span class="sxs-lookup"><span data-stu-id="0d4fb-118">Returns the number of elements in pSemantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d4fb-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0d4fb-119">Return value</span></span>

<span data-ttu-id="0d4fb-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0d4fb-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0d4fb-121">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0d4fb-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0d4fb-122">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="0d4fb-122">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d4fb-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d4fb-123">Requirements</span></span>



| <span data-ttu-id="0d4fb-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d4fb-124">Requirement</span></span> | <span data-ttu-id="0d4fb-125">Valor</span><span class="sxs-lookup"><span data-stu-id="0d4fb-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d4fb-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0d4fb-126">Header</span></span><br/>  | <dl> <span data-ttu-id="0d4fb-127"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d4fb-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="0d4fb-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0d4fb-128">Library</span></span><br/> | <dl> <span data-ttu-id="0d4fb-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0d4fb-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0d4fb-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="0d4fb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d4fb-131">Funções de sombreador</span><span class="sxs-lookup"><span data-stu-id="0d4fb-131">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
