---
description: Monte um sombreador.
ms.assetid: 2977b64a-b8cc-454b-8e28-291f6f2c6fc1
title: Função D3DXAssembleShaderFromFile (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXAssembleShaderFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a6e355f6ce51158f72757f771114346899557c59
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105762980"
---
# <a name="d3dxassembleshaderfromfile-function"></a><span data-ttu-id="2171c-103">Função D3DXAssembleShaderFromFile</span><span class="sxs-lookup"><span data-stu-id="2171c-103">D3DXAssembleShaderFromFile function</span></span>

<span data-ttu-id="2171c-104">Monte um sombreador.</span><span class="sxs-lookup"><span data-stu-id="2171c-104">Assemble a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="2171c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2171c-105">Syntax</span></span>


```C++
HRESULT D3DXAssembleShaderFromFile(
  _In_        LPCTSTR       pSrcFile,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _In_        DWORD         Flags,
  _Out_       LPD3DXBUFFER  *ppShader,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="2171c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2171c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2171c-107">*pSrcFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2171c-107">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2171c-108">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2171c-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2171c-109">Ponteiro para uma cadeia de caracteres que especifica o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="2171c-109">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="2171c-110">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="2171c-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="2171c-111">Caso contrário, o tipo de dados String será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="2171c-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="2171c-112">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="2171c-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="2171c-113">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2171c-113">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2171c-114">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="2171c-114">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="2171c-115">Uma matriz terminada **nula** opcional de estruturas [**D3DXMACRO**](d3dxmacro.md) .</span><span class="sxs-lookup"><span data-stu-id="2171c-115">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="2171c-116">Esse valor pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="2171c-116">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2171c-117">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2171c-117">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2171c-118">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="2171c-118">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="2171c-119">Ponteiro de interface opcional, [**ID3DXInclude**](id3dxinclude.md), a ser usado para manipulação de \# diretivas include.</span><span class="sxs-lookup"><span data-stu-id="2171c-119">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="2171c-120">Se esse valor for **NULL**, \# incluirá que será respeitado durante a compilação de um arquivo ou causará um erro quando compilado de um recurso ou memória.</span><span class="sxs-lookup"><span data-stu-id="2171c-120">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="2171c-121">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="2171c-121">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2171c-122">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2171c-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2171c-123">Opções de compilação identificadas por vários sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="2171c-123">Compile options identified by various flags.</span></span> <span data-ttu-id="2171c-124">O compilador do Direct3D 10 HLSL agora é o padrão.</span><span class="sxs-lookup"><span data-stu-id="2171c-124">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="2171c-125">Consulte [D3DXSHADER flags](d3dxshader-flags.md) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="2171c-125">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="2171c-126">*ppShader* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2171c-126">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2171c-127">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="2171c-127">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="2171c-128">Retorna um buffer que contém o sombreador criado.</span><span class="sxs-lookup"><span data-stu-id="2171c-128">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="2171c-129">Esse buffer contém o código de sombreador compilado, bem como qualquer informação de tabela de depuração e símbolo inserida.</span><span class="sxs-lookup"><span data-stu-id="2171c-129">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="2171c-130">*ppErrorMsgs* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2171c-130">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2171c-131">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="2171c-131">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="2171c-132">Retorna um buffer que contém uma lista de erros e avisos que foram encontrados durante a compilação.</span><span class="sxs-lookup"><span data-stu-id="2171c-132">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="2171c-133">Essas são as mesmas mensagens que o depurador exibe ao serem executados no modo de depuração.</span><span class="sxs-lookup"><span data-stu-id="2171c-133">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="2171c-134">Esse valor pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="2171c-134">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2171c-135">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2171c-135">Return value</span></span>

<span data-ttu-id="2171c-136">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2171c-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2171c-137">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2171c-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2171c-138">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="2171c-138">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="2171c-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="2171c-139">Remarks</span></span>

<span data-ttu-id="2171c-140">A configuração do compilador também determina a versão da função.</span><span class="sxs-lookup"><span data-stu-id="2171c-140">The compiler setting also determines the function version.</span></span> <span data-ttu-id="2171c-141">Se o Unicode for definido, a chamada de função será resolvida como D3DXAssembleShaderFromFileW.</span><span class="sxs-lookup"><span data-stu-id="2171c-141">If Unicode is defined, the function call resolves to D3DXAssembleShaderFromFileW.</span></span> <span data-ttu-id="2171c-142">Caso contrário, a chamada de função é resolvida como D3DXAssembleShaderFromFileA porque as cadeias de caracteres ANSI estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="2171c-142">Otherwise, the function call resolves to D3DXAssembleShaderFromFileA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="2171c-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2171c-143">Requirements</span></span>



| <span data-ttu-id="2171c-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="2171c-144">Requirement</span></span> | <span data-ttu-id="2171c-145">Valor</span><span class="sxs-lookup"><span data-stu-id="2171c-145">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2171c-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2171c-146">Header</span></span><br/>  | <dl> <span data-ttu-id="2171c-147"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="2171c-147"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="2171c-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2171c-148">Library</span></span><br/> | <dl> <span data-ttu-id="2171c-149"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2171c-149"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2171c-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="2171c-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2171c-151">Funções de sombreador</span><span class="sxs-lookup"><span data-stu-id="2171c-151">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="2171c-152">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="2171c-152">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="2171c-153">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="2171c-153">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
