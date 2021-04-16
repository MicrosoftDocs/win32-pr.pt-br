---
description: Monte um sombreador.
ms.assetid: a0d31b15-db79-4aa8-afd8-fa1e20c61725
title: Função D3DXAssembleShaderFromResource (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXAssembleShaderFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5e748764eec94ea1f555c225c34680392610c9f5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105747663"
---
# <a name="d3dxassembleshaderfromresource-function"></a><span data-ttu-id="583f2-103">Função D3DXAssembleShaderFromResource</span><span class="sxs-lookup"><span data-stu-id="583f2-103">D3DXAssembleShaderFromResource function</span></span>

<span data-ttu-id="583f2-104">Monte um sombreador.</span><span class="sxs-lookup"><span data-stu-id="583f2-104">Assemble a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="583f2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="583f2-105">Syntax</span></span>


```C++
HRESULT D3DXAssembleShaderFromResource(
  _In_        HMODULE       hSrcModule,
  _In_        LPCTSTR       pSrcResource,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _In_        DWORD         Flags,
  _Out_       LPD3DXBUFFER  *ppShader,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="583f2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="583f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="583f2-107">*hSrcModule* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="583f2-107">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="583f2-108">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="583f2-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="583f2-109">Identificador para um módulo que contém a descrição do efeito.</span><span class="sxs-lookup"><span data-stu-id="583f2-109">Handle to a module containing the effect description.</span></span> <span data-ttu-id="583f2-110">Se esse parâmetro for **NULL**, o módulo atual será usado.</span><span class="sxs-lookup"><span data-stu-id="583f2-110">If this parameter is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="583f2-111">*pSrcResource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="583f2-111">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="583f2-112">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="583f2-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="583f2-113">Ponteiro para uma cadeia de caracteres que especifica o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="583f2-113">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="583f2-114">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="583f2-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="583f2-115">Caso contrário, o tipo de dados String será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="583f2-115">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="583f2-116">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="583f2-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="583f2-117">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="583f2-117">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="583f2-118">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="583f2-118">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="583f2-119">Uma matriz terminada **nula** opcional de estruturas [**D3DXMACRO**](d3dxmacro.md) .</span><span class="sxs-lookup"><span data-stu-id="583f2-119">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="583f2-120">Esse valor pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="583f2-120">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="583f2-121">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="583f2-121">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="583f2-122">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="583f2-122">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="583f2-123">Ponteiro de interface opcional, [**ID3DXInclude**](id3dxinclude.md), a ser usado para manipulação de \# diretivas include.</span><span class="sxs-lookup"><span data-stu-id="583f2-123">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="583f2-124">Se esse valor for **NULL**, \# incluirá que será respeitado durante a compilação de um arquivo ou causará um erro quando compilado de um recurso ou memória.</span><span class="sxs-lookup"><span data-stu-id="583f2-124">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="583f2-125">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="583f2-125">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="583f2-126">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="583f2-126">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="583f2-127">Opções de compilação identificadas por vários sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="583f2-127">Compile options identified by various flags.</span></span> <span data-ttu-id="583f2-128">O compilador do Direct3D 10 HLSL agora é o padrão.</span><span class="sxs-lookup"><span data-stu-id="583f2-128">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="583f2-129">Consulte [D3DXSHADER flags](d3dxshader-flags.md) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="583f2-129">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="583f2-130">*ppShader* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="583f2-130">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="583f2-131">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="583f2-131">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="583f2-132">Retorna um buffer que contém o sombreador criado.</span><span class="sxs-lookup"><span data-stu-id="583f2-132">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="583f2-133">Esse buffer contém o código de sombreador compilado, bem como qualquer informação de tabela de depuração e símbolo inserida.</span><span class="sxs-lookup"><span data-stu-id="583f2-133">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="583f2-134">*ppErrorMsgs* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="583f2-134">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="583f2-135">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="583f2-135">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="583f2-136">Retorna um buffer que contém uma lista de erros e avisos que foram encontrados durante a compilação.</span><span class="sxs-lookup"><span data-stu-id="583f2-136">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="583f2-137">Essas são as mesmas mensagens que o depurador exibe ao serem executados no modo de depuração.</span><span class="sxs-lookup"><span data-stu-id="583f2-137">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="583f2-138">Esse valor pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="583f2-138">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="583f2-139">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="583f2-139">Return value</span></span>

<span data-ttu-id="583f2-140">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="583f2-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="583f2-141">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="583f2-141">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="583f2-142">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="583f2-142">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="583f2-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="583f2-143">Remarks</span></span>

<span data-ttu-id="583f2-144">A configuração do compilador também determina a versão da função.</span><span class="sxs-lookup"><span data-stu-id="583f2-144">The compiler setting also determines the function version.</span></span> <span data-ttu-id="583f2-145">Se o Unicode for definido, a chamada de função será resolvida como D3DXAssembleShaderFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="583f2-145">If Unicode is defined, the function call resolves to D3DXAssembleShaderFromResourceW.</span></span> <span data-ttu-id="583f2-146">Caso contrário, a chamada de função é resolvida como D3DXAssembleShaderFromResourceA porque as cadeias de caracteres ANSI estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="583f2-146">Otherwise, the function call resolves to D3DXAssembleShaderFromResourceA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="583f2-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="583f2-147">Requirements</span></span>



| <span data-ttu-id="583f2-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="583f2-148">Requirement</span></span> | <span data-ttu-id="583f2-149">Valor</span><span class="sxs-lookup"><span data-stu-id="583f2-149">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="583f2-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="583f2-150">Header</span></span><br/>  | <dl> <span data-ttu-id="583f2-151"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="583f2-151"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="583f2-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="583f2-152">Library</span></span><br/> | <dl> <span data-ttu-id="583f2-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="583f2-153"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="583f2-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="583f2-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="583f2-155">Funções de sombreador</span><span class="sxs-lookup"><span data-stu-id="583f2-155">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="583f2-156">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="583f2-156">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="583f2-157">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="583f2-157">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
