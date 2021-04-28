---
description: Função D3DXCompileShaderFromFile – compilar um arquivo de sombreador.
ms.assetid: 2ad6042f-3601-4f4a-9624-6319a3372355
title: Função D3DXCompileShaderFromFile (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCompileShaderFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a4392a3c36b31deb4071c215ad9b41e7f40c21ee
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115844"
---
# <a name="d3dxcompileshaderfromfile-function"></a><span data-ttu-id="b0f52-103">Função D3DXCompileShaderFromFile</span><span class="sxs-lookup"><span data-stu-id="b0f52-103">D3DXCompileShaderFromFile function</span></span>

<span data-ttu-id="b0f52-104">Compilar um arquivo de sombreador.</span><span class="sxs-lookup"><span data-stu-id="b0f52-104">Compile a shader file.</span></span>

> [!Note]  
> <span data-ttu-id="b0f52-105">Em vez de usar essa função herdada, recomendamos que você compile offline usando o compilador de linha de comando Fxc.exe ou use a API [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) .</span><span class="sxs-lookup"><span data-stu-id="b0f52-105">Instead of using this legacy function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b0f52-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b0f52-106">Syntax</span></span>


```C++
HRESULT D3DXCompileShaderFromFile(
  _In_        LPCTSTR             pSrcFile,
  _In_  const D3DXMACRO           *pDefines,
  _In_        LPD3DXINCLUDE       pInclude,
  _In_        LPCSTR              pFunctionName,
  _In_        LPCSTR              pProfile,
  _In_        DWORD               Flags,
  _Out_       LPD3DXBUFFER        *ppShader,
  _Out_       LPD3DXBUFFER        *ppErrorMsgs,
  _Out_       LPD3DXCONSTANTTABLE *ppConstantTable
);
```



## <a name="parameters"></a><span data-ttu-id="b0f52-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0f52-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0f52-108">*pSrcFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b0f52-108">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0f52-109">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0f52-109">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b0f52-110">Ponteiro para uma cadeia de caracteres que especifica o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="b0f52-110">Pointer to a string that specifies the filename.</span></span>

</dd> <dt>

<span data-ttu-id="b0f52-111">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b0f52-111">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0f52-112">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="b0f52-112">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="b0f52-113">Uma matriz terminada **nula** opcional de estruturas [**D3DXMACRO**](d3dxmacro.md) .</span><span class="sxs-lookup"><span data-stu-id="b0f52-113">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="b0f52-114">Esse valor pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="b0f52-114">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b0f52-115">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b0f52-115">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0f52-116">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="b0f52-116">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="b0f52-117">Ponteiro de interface opcional, [**ID3DXInclude**](id3dxinclude.md), a ser usado para manipulação de \# diretivas include.</span><span class="sxs-lookup"><span data-stu-id="b0f52-117">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="b0f52-118">Se esse valor for **NULL**, \# incluirá que será respeitado durante a compilação de um arquivo ou causará um erro quando compilado de um recurso ou memória.</span><span class="sxs-lookup"><span data-stu-id="b0f52-118">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="b0f52-119">*pFunctionName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b0f52-119">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0f52-120">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0f52-120">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b0f52-121">Ponteiro para a função de ponto de entrada do sombreador onde a execução começa.</span><span class="sxs-lookup"><span data-stu-id="b0f52-121">Pointer to the shader entry point function where execution begins.</span></span>

</dd> <dt>

<span data-ttu-id="b0f52-122">*pProfile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b0f52-122">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0f52-123">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0f52-123">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b0f52-124">Ponteiro para um perfil de sombreador que determina o conjunto de instruções do sombreador.</span><span class="sxs-lookup"><span data-stu-id="b0f52-124">Pointer to a shader profile which determines the shader instruction set.</span></span> <span data-ttu-id="b0f52-125">Consulte [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) ou [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) para obter uma lista dos perfis disponíveis.</span><span class="sxs-lookup"><span data-stu-id="b0f52-125">See [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) or [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) for a list of the profiles available.</span></span>

</dd> <dt>

<span data-ttu-id="b0f52-126">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="b0f52-126">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0f52-127">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0f52-127">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b0f52-128">Opções de compilação identificadas por vários sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="b0f52-128">Compile options identified by various flags.</span></span> <span data-ttu-id="b0f52-129">O compilador do Direct3D 10 HLSL agora é o padrão.</span><span class="sxs-lookup"><span data-stu-id="b0f52-129">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="b0f52-130">Consulte [D3DXSHADER flags](d3dxshader-flags.md) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="b0f52-130">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="b0f52-131">*ppShader* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b0f52-131">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0f52-132">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="b0f52-132">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="b0f52-133">Retorna um buffer que contém o sombreador criado.</span><span class="sxs-lookup"><span data-stu-id="b0f52-133">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="b0f52-134">Esse buffer contém o código de sombreador compilado, bem como qualquer informação de tabela de depuração e símbolo inserida.</span><span class="sxs-lookup"><span data-stu-id="b0f52-134">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="b0f52-135">*ppErrorMsgs* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b0f52-135">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0f52-136">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="b0f52-136">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="b0f52-137">Retorna um buffer que contém uma lista de erros e avisos que foram encontrados durante a compilação.</span><span class="sxs-lookup"><span data-stu-id="b0f52-137">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="b0f52-138">Essas são as mesmas mensagens que o depurador exibe ao serem executados no modo de depuração.</span><span class="sxs-lookup"><span data-stu-id="b0f52-138">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="b0f52-139">Esse valor pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="b0f52-139">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b0f52-140">*ppConstantTable* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b0f52-140">*ppConstantTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0f52-141">Tipo: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span><span class="sxs-lookup"><span data-stu-id="b0f52-141">Type: **[**LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span></span>

<span data-ttu-id="b0f52-142">Retorna uma interface [**ID3DXConstantTable**](id3dxconstanttable.md) , que pode ser usada para acessar constantes de sombreador.</span><span class="sxs-lookup"><span data-stu-id="b0f52-142">Returns an [**ID3DXConstantTable**](id3dxconstanttable.md) interface, which can be used to access shader constants.</span></span> <span data-ttu-id="b0f52-143">Esse valor pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="b0f52-143">This value can be **NULL**.</span></span> <span data-ttu-id="b0f52-144">Se você compilar seu aplicativo como grande reconhecimento de endereço (ou seja, usar a opção de vinculador/LARGEADDRESSAWARE para tratar endereços maiores que 2 GB), não poderá usar esse parâmetro e deve defini-lo como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="b0f52-144">If you compile your application as large address aware (that is, you use the /LARGEADDRESSAWARE linker option to handle addresses larger than 2 GB), you cannot use this parameter and must set it to **NULL**.</span></span> <span data-ttu-id="b0f52-145">Em vez disso, você deve usar a função [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) para recuperar a tabela de constante de sombreador que está inserida dentro do sombreador.</span><span class="sxs-lookup"><span data-stu-id="b0f52-145">Instead, you must use the [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) function to retrieve the shader-constant table that is embedded inside the shader.</span></span> <span data-ttu-id="b0f52-146">Nesta chamada **D3DXGetShaderConstantTableEx** , você deve passar o sinalizador **D3DXCONSTTABLE \_ LARGEADDRESSAWARE** para o parâmetro *flags* para especificar o acesso a até 4 GB de espaço de endereço virtual.</span><span class="sxs-lookup"><span data-stu-id="b0f52-146">In this **D3DXGetShaderConstantTableEx** call, you must pass the **D3DXCONSTTABLE\_LARGEADDRESSAWARE** flag to the *Flags* parameter to specify to access up to 4 GB of virtual address space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0f52-147">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="b0f52-147">Return value</span></span>

<span data-ttu-id="b0f52-148">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b0f52-148">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b0f52-149">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b0f52-149">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b0f52-150">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, e \_ NOTIMPL, e \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="b0f52-150">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_NOTIMPL, E\_OUTOFMEMORY.</span></span>

<span data-ttu-id="b0f52-151">E \_ NOTIMPL será retornado se você estiver usando sombreadores 1,1 (vs \_ 1 \_ 1 e PS \_ 1 \_ 1).</span><span class="sxs-lookup"><span data-stu-id="b0f52-151">E\_NOTIMPL is returned if you're using 1.1 shaders (vs\_1\_1 and ps\_1\_1).</span></span>

## <a name="requirements"></a><span data-ttu-id="b0f52-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0f52-152">Requirements</span></span>



| <span data-ttu-id="b0f52-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0f52-153">Requirement</span></span> | <span data-ttu-id="b0f52-154">Valor</span><span class="sxs-lookup"><span data-stu-id="b0f52-154">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0f52-155">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b0f52-155">Header</span></span><br/>  | <dl> <span data-ttu-id="b0f52-156"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0f52-156"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="b0f52-157">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b0f52-157">Library</span></span><br/> | <dl> <span data-ttu-id="b0f52-158"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b0f52-158"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b0f52-159">Consulte também</span><span class="sxs-lookup"><span data-stu-id="b0f52-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0f52-160">Funções de sombreador</span><span class="sxs-lookup"><span data-stu-id="b0f52-160">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="b0f52-161">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="b0f52-161">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="b0f52-162">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="b0f52-162">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
