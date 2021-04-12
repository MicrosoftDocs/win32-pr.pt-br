---
description: Pré-processa um recurso de sombreador sem executar a compilação. Isso resolve todas as \# definições e \# inclusões, fornecendo um sombreador independente para a compilação subsequente.
ms.assetid: a00c2db9-d7ba-48ab-80e3-dc20774e1b1e
title: Função D3DXPreprocessShaderFromResource (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPreprocessShaderFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c45073d0b84ef6fb33d378c4c18f862f55c6b84a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298580"
---
# <a name="d3dxpreprocessshaderfromresource-function"></a><span data-ttu-id="6e0ab-104">Função D3DXPreprocessShaderFromResource</span><span class="sxs-lookup"><span data-stu-id="6e0ab-104">D3DXPreprocessShaderFromResource function</span></span>

<span data-ttu-id="6e0ab-105">Pré-processa um recurso de sombreador sem executar a compilação.</span><span class="sxs-lookup"><span data-stu-id="6e0ab-105">Preprocesses a shader resource without performing compilation.</span></span> <span data-ttu-id="6e0ab-106">Isso resolve todas as \# definições e \# inclusões, fornecendo um sombreador independente para a compilação subsequente.</span><span class="sxs-lookup"><span data-stu-id="6e0ab-106">This resolves all \#defines and \#includes, providing a self-contained shader for subsequent compilation.</span></span>

> [!Note]  
> <span data-ttu-id="6e0ab-107">Em vez de usar essa função herdada, recomendamos que você use a API [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="6e0ab-107">Instead of using this legacy function, we recommend that you use the [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="6e0ab-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6e0ab-108">Syntax</span></span>


```C++
HRESULT D3DXPreprocessShaderFromResource(
  _In_        HMODULE       hSrcModule,
  _In_        LPCSTR        pSrcResource,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _Out_       LPD3DXBUFFER  *ppShaderText,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="6e0ab-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6e0ab-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e0ab-110">*hSrcModule* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6e0ab-110">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e0ab-111">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6e0ab-111">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6e0ab-112">Identificador para o módulo que contém o recurso de sombreador.</span><span class="sxs-lookup"><span data-stu-id="6e0ab-112">Handle to the module that holds the shader resource.</span></span> <span data-ttu-id="6e0ab-113">Se esse valor for **nulo**, o módulo atual será usado.</span><span class="sxs-lookup"><span data-stu-id="6e0ab-113">If this value is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="6e0ab-114">*pSrcResource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6e0ab-114">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e0ab-115">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6e0ab-115">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6e0ab-116">Cadeia de caracteres que representa o nome do recurso no módulo.</span><span class="sxs-lookup"><span data-stu-id="6e0ab-116">String that represents the name of the resource in the module.</span></span>

</dd> <dt>

<span data-ttu-id="6e0ab-117">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6e0ab-117">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e0ab-118">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="6e0ab-118">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="6e0ab-119">Uma matriz terminada **nula** opcional de estruturas [**D3DXMACRO**](d3dxmacro.md) .</span><span class="sxs-lookup"><span data-stu-id="6e0ab-119">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="6e0ab-120">Esse valor pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="6e0ab-120">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6e0ab-121">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6e0ab-121">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e0ab-122">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="6e0ab-122">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="6e0ab-123">Ponteiro de interface opcional, [**ID3DXInclude**](id3dxinclude.md), a ser usado para manipulação de \# diretivas include.</span><span class="sxs-lookup"><span data-stu-id="6e0ab-123">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="6e0ab-124">Se esse valor for **NULL**, \# incluirá que será respeitado durante a compilação de um arquivo ou causará um erro quando compilado de um recurso ou memória.</span><span class="sxs-lookup"><span data-stu-id="6e0ab-124">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="6e0ab-125">*ppShaderText* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6e0ab-125">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e0ab-126">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="6e0ab-126">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="6e0ab-127">Retorna um buffer que contém uma única cadeia de caracteres grande que representa o fluxo de token formatado resultante.</span><span class="sxs-lookup"><span data-stu-id="6e0ab-127">Returns a buffer containing a single large string that represents the resulting formatted token stream.</span></span>

</dd> <dt>

<span data-ttu-id="6e0ab-128">*ppErrorMsgs* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6e0ab-128">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e0ab-129">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="6e0ab-129">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="6e0ab-130">Retorna um buffer que contém uma lista de erros e avisos que foram encontrados durante a compilação.</span><span class="sxs-lookup"><span data-stu-id="6e0ab-130">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="6e0ab-131">Essas são as mesmas mensagens que o depurador exibe ao serem executados no modo de depuração.</span><span class="sxs-lookup"><span data-stu-id="6e0ab-131">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="6e0ab-132">Esse valor pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="6e0ab-132">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e0ab-133">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6e0ab-133">Return value</span></span>

<span data-ttu-id="6e0ab-134">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6e0ab-134">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6e0ab-135">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6e0ab-135">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6e0ab-136">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="6e0ab-136">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e0ab-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e0ab-137">Requirements</span></span>



| <span data-ttu-id="6e0ab-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e0ab-138">Requirement</span></span> | <span data-ttu-id="6e0ab-139">Valor</span><span class="sxs-lookup"><span data-stu-id="6e0ab-139">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e0ab-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6e0ab-140">Header</span></span><br/>  | <dl> <span data-ttu-id="6e0ab-141"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e0ab-141"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="6e0ab-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6e0ab-142">Library</span></span><br/> | <dl> <span data-ttu-id="6e0ab-143"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6e0ab-143"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="6e0ab-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="6e0ab-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e0ab-145">Funções de sombreador</span><span class="sxs-lookup"><span data-stu-id="6e0ab-145">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="6e0ab-146">**D3DXPreprocessShaderFromFile**</span><span class="sxs-lookup"><span data-stu-id="6e0ab-146">**D3DXPreprocessShaderFromFile**</span></span>](d3dxpreprocessshaderfromfile.md)
</dt> <dt>

[<span data-ttu-id="6e0ab-147">**D3DXPreprocessShader**</span><span class="sxs-lookup"><span data-stu-id="6e0ab-147">**D3DXPreprocessShader**</span></span>](d3dxpreprocessshader.md)
</dt> </dl>

 

 
