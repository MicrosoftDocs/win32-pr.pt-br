---
description: Pré-processa um arquivo de sombreador sem executar a compilação. Isso resolve todas as \# definições e \# inclusões, fornecendo um sombreador independente para a compilação subsequente.
ms.assetid: 1be68cc0-b4a3-41b4-b956-b96ed439be9e
title: Função D3DXPreprocessShaderFromFile (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPreprocessShaderFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1ba9cf35418bbbe6fe4b39341031fd1e056b27dd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298605"
---
# <a name="d3dxpreprocessshaderfromfile-function"></a><span data-ttu-id="e57c6-104">Função D3DXPreprocessShaderFromFile</span><span class="sxs-lookup"><span data-stu-id="e57c6-104">D3DXPreprocessShaderFromFile function</span></span>

<span data-ttu-id="e57c6-105">Pré-processa um arquivo de sombreador sem executar a compilação.</span><span class="sxs-lookup"><span data-stu-id="e57c6-105">Preprocesses a shader file without performing compilation.</span></span> <span data-ttu-id="e57c6-106">Isso resolve todas as \# definições e \# inclusões, fornecendo um sombreador independente para a compilação subsequente.</span><span class="sxs-lookup"><span data-stu-id="e57c6-106">This resolves all \#defines and \#includes, providing a self-contained shader for subsequent compilation.</span></span>

> [!Note]  
> <span data-ttu-id="e57c6-107">Em vez de usar essa função herdada, recomendamos que você use a API [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="e57c6-107">Instead of using this legacy function, we recommend that you use the [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="e57c6-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e57c6-108">Syntax</span></span>


```C++
HRESULT D3DXPreprocessShaderFromFile(
  _In_        LPCSTR        pSrcFile,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _Out_       LPD3DXBUFFER  *ppShaderText,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="e57c6-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e57c6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e57c6-110">*pSrcFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e57c6-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e57c6-111">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e57c6-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e57c6-112">Ponteiro para uma cadeia de caracteres que especifica o nome do arquivo do sombreador.</span><span class="sxs-lookup"><span data-stu-id="e57c6-112">Pointer to a string that specifies the filename of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="e57c6-113">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e57c6-113">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e57c6-114">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="e57c6-114">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="e57c6-115">Uma matriz terminada **nula** opcional de estruturas [**D3DXMACRO**](d3dxmacro.md) .</span><span class="sxs-lookup"><span data-stu-id="e57c6-115">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="e57c6-116">Esse valor pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="e57c6-116">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e57c6-117">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e57c6-117">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e57c6-118">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="e57c6-118">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="e57c6-119">Ponteiro de interface opcional, [**ID3DXInclude**](id3dxinclude.md), a ser usado para manipulação de \# diretivas include.</span><span class="sxs-lookup"><span data-stu-id="e57c6-119">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="e57c6-120">Se esse valor for **NULL**, \# incluirá que será respeitado durante a compilação de um arquivo ou causará um erro quando compilado de um recurso ou memória.</span><span class="sxs-lookup"><span data-stu-id="e57c6-120">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="e57c6-121">*ppShaderText* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e57c6-121">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e57c6-122">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="e57c6-122">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="e57c6-123">Retorna um buffer que contém uma única cadeia de caracteres grande que representa o fluxo de token formatado resultante.</span><span class="sxs-lookup"><span data-stu-id="e57c6-123">Returns a buffer containing a single large string that represents the resulting formatted token stream.</span></span>

</dd> <dt>

<span data-ttu-id="e57c6-124">*ppErrorMsgs* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e57c6-124">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e57c6-125">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="e57c6-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="e57c6-126">Retorna um buffer que contém uma lista de erros e avisos que foram encontrados durante a compilação.</span><span class="sxs-lookup"><span data-stu-id="e57c6-126">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="e57c6-127">Essas são as mesmas mensagens que o depurador exibe ao serem executados no modo de depuração.</span><span class="sxs-lookup"><span data-stu-id="e57c6-127">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="e57c6-128">Esse valor pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="e57c6-128">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e57c6-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e57c6-129">Return value</span></span>

<span data-ttu-id="e57c6-130">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e57c6-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e57c6-131">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e57c6-131">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e57c6-132">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="e57c6-132">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="e57c6-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e57c6-133">Requirements</span></span>



| <span data-ttu-id="e57c6-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="e57c6-134">Requirement</span></span> | <span data-ttu-id="e57c6-135">Valor</span><span class="sxs-lookup"><span data-stu-id="e57c6-135">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e57c6-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e57c6-136">Header</span></span><br/>  | <dl> <span data-ttu-id="e57c6-137"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="e57c6-137"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="e57c6-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e57c6-138">Library</span></span><br/> | <dl> <span data-ttu-id="e57c6-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e57c6-139"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e57c6-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="e57c6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e57c6-141">Funções de sombreador</span><span class="sxs-lookup"><span data-stu-id="e57c6-141">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="e57c6-142">**D3DXPreprocessShader**</span><span class="sxs-lookup"><span data-stu-id="e57c6-142">**D3DXPreprocessShader**</span></span>](d3dxpreprocessshader.md)
</dt> <dt>

[<span data-ttu-id="e57c6-143">**D3DXPreprocessShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="e57c6-143">**D3DXPreprocessShaderFromResource**</span></span>](d3dxpreprocessshaderfromresource.md)
</dt> </dl>

 

 
