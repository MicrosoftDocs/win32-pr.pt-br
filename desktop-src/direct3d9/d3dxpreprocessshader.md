---
description: Pré-processa um sombreador sem executar a compilação. Isso resolve todas as \# definições e \# inclusões, fornecendo um sombreador independente para a compilação subsequente.
ms.assetid: d91258ed-6206-487a-aa81-e7c2bcea21ea
title: Função D3DXPreprocessShader (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPreprocessShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 042cebe4e678ac1715a37ec3425ec0f21561797c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104506461"
---
# <a name="d3dxpreprocessshader-function"></a><span data-ttu-id="abdab-104">Função D3DXPreprocessShader</span><span class="sxs-lookup"><span data-stu-id="abdab-104">D3DXPreprocessShader function</span></span>

<span data-ttu-id="abdab-105">Pré-processa um sombreador sem executar a compilação.</span><span class="sxs-lookup"><span data-stu-id="abdab-105">Preprocesses a shader without performing compilation.</span></span> <span data-ttu-id="abdab-106">Isso resolve todas as \# definições e \# inclusões, fornecendo um sombreador independente para a compilação subsequente.</span><span class="sxs-lookup"><span data-stu-id="abdab-106">This resolves all \#defines and \#includes, providing a self-contained shader for subsequent compilation.</span></span>

> [!Note]  
> <span data-ttu-id="abdab-107">Em vez de usar essa função herdada, recomendamos que você use a API [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="abdab-107">Instead of using this legacy function, we recommend that you use the [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="abdab-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="abdab-108">Syntax</span></span>


```C++
HRESULT D3DXPreprocessShader(
  _In_        LPCSTR        pSrcData,
  _In_        UINT          SrcDataSize,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _Out_       LPD3DXBUFFER  *ppShaderText,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="abdab-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="abdab-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abdab-110">*pSrcData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="abdab-110">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abdab-111">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="abdab-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="abdab-112">Ponteiro para uma cadeia de caracteres que contém o sombreador.</span><span class="sxs-lookup"><span data-stu-id="abdab-112">Pointer to a string that contains the shader.</span></span>

</dd> <dt>

<span data-ttu-id="abdab-113">*SrcDataSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="abdab-113">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abdab-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="abdab-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="abdab-115">Comprimento dos dados em bytes.</span><span class="sxs-lookup"><span data-stu-id="abdab-115">Length of the data in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="abdab-116">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="abdab-116">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abdab-117">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="abdab-117">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="abdab-118">Uma matriz terminada **nula** opcional de estruturas [**D3DXMACRO**](d3dxmacro.md) .</span><span class="sxs-lookup"><span data-stu-id="abdab-118">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="abdab-119">Esse valor pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="abdab-119">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="abdab-120">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="abdab-120">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abdab-121">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="abdab-121">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="abdab-122">Ponteiro de interface opcional, [**ID3DXInclude**](id3dxinclude.md), a ser usado para manipulação de \# diretivas include.</span><span class="sxs-lookup"><span data-stu-id="abdab-122">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="abdab-123">Se esse valor for **NULL**, \# incluirá que será respeitado durante a compilação de um arquivo ou causará um erro quando compilado de um recurso ou memória.</span><span class="sxs-lookup"><span data-stu-id="abdab-123">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="abdab-124">*ppShaderText* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="abdab-124">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="abdab-125">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="abdab-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="abdab-126">Retorna um buffer que contém uma única cadeia de caracteres grande que representa o fluxo de token formatado resultante.</span><span class="sxs-lookup"><span data-stu-id="abdab-126">Returns a buffer containing a single large string that represents the resulting formatted token stream.</span></span>

</dd> <dt>

<span data-ttu-id="abdab-127">*ppErrorMsgs* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="abdab-127">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="abdab-128">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="abdab-128">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="abdab-129">Retorna um buffer que contém uma lista de erros e avisos que foram encontrados durante a compilação.</span><span class="sxs-lookup"><span data-stu-id="abdab-129">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="abdab-130">Essas são as mesmas mensagens que o depurador exibe ao serem executados no modo de depuração.</span><span class="sxs-lookup"><span data-stu-id="abdab-130">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="abdab-131">Esse valor pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="abdab-131">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abdab-132">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="abdab-132">Return value</span></span>

<span data-ttu-id="abdab-133">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="abdab-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="abdab-134">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="abdab-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="abdab-135">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="abdab-135">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="abdab-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="abdab-136">Requirements</span></span>



| <span data-ttu-id="abdab-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="abdab-137">Requirement</span></span> | <span data-ttu-id="abdab-138">Valor</span><span class="sxs-lookup"><span data-stu-id="abdab-138">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="abdab-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="abdab-139">Header</span></span><br/>  | <dl> <span data-ttu-id="abdab-140"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="abdab-140"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="abdab-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="abdab-141">Library</span></span><br/> | <dl> <span data-ttu-id="abdab-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="abdab-142"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="abdab-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="abdab-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abdab-144">Funções de sombreador</span><span class="sxs-lookup"><span data-stu-id="abdab-144">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="abdab-145">**D3DXPreprocessShaderFromFile**</span><span class="sxs-lookup"><span data-stu-id="abdab-145">**D3DXPreprocessShaderFromFile**</span></span>](d3dxpreprocessshaderfromfile.md)
</dt> <dt>

[<span data-ttu-id="abdab-146">**D3DXPreprocessShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="abdab-146">**D3DXPreprocessShaderFromResource**</span></span>](d3dxpreprocessshaderfromresource.md)
</dt> </dl>

 

 
