---
description: Obtém a semântica para as entradas do sombreador. Use este método para determinar o formato de vértice de entrada.
ms.assetid: e94b2b14-3830-4a13-8c23-7841a56d6730
title: Função D3DXGetShaderInputSemantics (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderInputSemantics
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2032f241d6ca5c22506c0875a21f9d5b431920df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105771370"
---
# <a name="d3dxgetshaderinputsemantics-function"></a><span data-ttu-id="19f1c-104">Função D3DXGetShaderInputSemantics</span><span class="sxs-lookup"><span data-stu-id="19f1c-104">D3DXGetShaderInputSemantics function</span></span>

<span data-ttu-id="19f1c-105">Obtém a semântica para as entradas do sombreador.</span><span class="sxs-lookup"><span data-stu-id="19f1c-105">Gets the semantics for the shader inputs.</span></span> <span data-ttu-id="19f1c-106">Use este método para determinar o formato de vértice de entrada.</span><span class="sxs-lookup"><span data-stu-id="19f1c-106">Use this method to determine the input vertex format.</span></span>

## <a name="syntax"></a><span data-ttu-id="19f1c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="19f1c-107">Syntax</span></span>


```C++
HRESULT D3DXGetShaderInputSemantics(
  _In_  const DWORD        *pFunction,
  _In_        D3DXSEMANTIC *pSemantics,
  _Out_       UINT         *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="19f1c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="19f1c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19f1c-109">*pFunction* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="19f1c-109">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19f1c-110">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="19f1c-110">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="19f1c-111">Ponteiro para o fluxo DWORD da função de sombreador.</span><span class="sxs-lookup"><span data-stu-id="19f1c-111">Pointer to the shader function DWORD stream.</span></span>

</dd> <dt>

<span data-ttu-id="19f1c-112">*pSemantics* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="19f1c-112">*pSemantics* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19f1c-113">Tipo: **[ **D3DXSEMANTIC**](d3dxsemantic.md)\***</span><span class="sxs-lookup"><span data-stu-id="19f1c-113">Type: **[**D3DXSEMANTIC**](d3dxsemantic.md)\***</span></span>

<span data-ttu-id="19f1c-114">Ponteiro para uma matriz de estruturas [**D3DXSEMANTIC**](d3dxsemantic.md) .</span><span class="sxs-lookup"><span data-stu-id="19f1c-114">Pointer to an array of [**D3DXSEMANTIC**](d3dxsemantic.md) structures.</span></span> <span data-ttu-id="19f1c-115">A função preencherá essa matriz com a semântica para cada elemento de entrada referenciado pelo sombreador.</span><span class="sxs-lookup"><span data-stu-id="19f1c-115">The function will fill this array with the semantics for each input element referenced by the shader.</span></span> <span data-ttu-id="19f1c-116">Presume-se que essa matriz contenha pelo menos elementos MAXD3DDECLLENGTH.</span><span class="sxs-lookup"><span data-stu-id="19f1c-116">This array is assumed to contain at least MAXD3DDECLLENGTH elements.</span></span> <span data-ttu-id="19f1c-117">No entanto, chamar **D3DXGetShaderInputSemantics** com PSemantics = **NULL** retornará o número de elementos necessários para pCount.</span><span class="sxs-lookup"><span data-stu-id="19f1c-117">However, calling **D3DXGetShaderInputSemantics** with pSemantics = **NULL** will return the number of elements needed for pCount.</span></span>

</dd> <dt>

<span data-ttu-id="19f1c-118">*pCount* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="19f1c-118">*pCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19f1c-119">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="19f1c-119">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="19f1c-120">Retorna o número de elementos em pSemantics.</span><span class="sxs-lookup"><span data-stu-id="19f1c-120">Returns the number of elements in pSemantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19f1c-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="19f1c-121">Return value</span></span>

<span data-ttu-id="19f1c-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="19f1c-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="19f1c-123">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="19f1c-123">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="19f1c-124">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="19f1c-124">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="19f1c-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="19f1c-125">Remarks</span></span>

<span data-ttu-id="19f1c-126">Use **D3DXGetShaderInputSemantics** para retornar uma lista de semântica de entrada exigida pelo sombreador.</span><span class="sxs-lookup"><span data-stu-id="19f1c-126">Use **D3DXGetShaderInputSemantics** to return a list of input semantics required by the shader.</span></span> <span data-ttu-id="19f1c-127">Esta é a maneira de descobrir qual é o formato de vértice de entrada para um sombreador de HLSL (linguagem de sombreamento de alto nível).</span><span class="sxs-lookup"><span data-stu-id="19f1c-127">This is the way to find out what the input vertex format is for a high-level shader language (HLSL) shader.</span></span> <span data-ttu-id="19f1c-128">Se o sombreador tiver entradas adicionais que sua declaração de vértice está faltando, você poderá criar um fluxo de vértice extra que tenha um stride de 0 que tenha os componentes ausentes com valores padrão.</span><span class="sxs-lookup"><span data-stu-id="19f1c-128">If the shader has additional inputs that your vertex declaration is missing, you could create an extra vertex stream that has a stride of 0 that has the missing components with default values.</span></span> <span data-ttu-id="19f1c-129">Por exemplo, essa técnica pode ser usada para fornecer a cor de vértice padrão para modelos que não o especificam.</span><span class="sxs-lookup"><span data-stu-id="19f1c-129">For instance, this technique could be used to provide default vertex color for models that do not specify it.</span></span>

## <a name="requirements"></a><span data-ttu-id="19f1c-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19f1c-130">Requirements</span></span>



| <span data-ttu-id="19f1c-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="19f1c-131">Requirement</span></span> | <span data-ttu-id="19f1c-132">Valor</span><span class="sxs-lookup"><span data-stu-id="19f1c-132">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="19f1c-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="19f1c-133">Header</span></span><br/>  | <dl> <span data-ttu-id="19f1c-134"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="19f1c-134"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="19f1c-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="19f1c-135">Library</span></span><br/> | <dl> <span data-ttu-id="19f1c-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="19f1c-136"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="19f1c-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="19f1c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19f1c-138">Funções de sombreador</span><span class="sxs-lookup"><span data-stu-id="19f1c-138">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
