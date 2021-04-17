---
description: Compilar um arquivo de sombreador.
ms.assetid: e944ae61-0c27-4795-8381-0ec9b3d8c3f4
title: Função D3DXCompileShaderFromResource (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCompileShaderFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e1bbb48fa2932eecb82c1c45d303d7afb948fa4d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105787563"
---
# <a name="d3dxcompileshaderfromresource-function"></a><span data-ttu-id="5ff63-103">Função D3DXCompileShaderFromResource</span><span class="sxs-lookup"><span data-stu-id="5ff63-103">D3DXCompileShaderFromResource function</span></span>

<span data-ttu-id="5ff63-104">Compilar um arquivo de sombreador.</span><span class="sxs-lookup"><span data-stu-id="5ff63-104">Compile a shader file.</span></span>

> [!Note]  
> <span data-ttu-id="5ff63-105">Em vez de usar essa função herdada, recomendamos que você compile offline usando o compilador de linha de comando Fxc.exe ou use a API [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) .</span><span class="sxs-lookup"><span data-stu-id="5ff63-105">Instead of using this legacy function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="5ff63-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5ff63-106">Syntax</span></span>


```C++
HRESULT D3DXCompileShaderFromResource(
  _In_        HMODULE             hSrcModule,
  _In_        LPCSTR              pSrcResource,
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



## <a name="parameters"></a><span data-ttu-id="5ff63-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5ff63-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ff63-108">*hSrcModule* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5ff63-108">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ff63-109">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5ff63-109">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5ff63-110">Identificador para um módulo que contém a descrição do efeito.</span><span class="sxs-lookup"><span data-stu-id="5ff63-110">Handle to a module containing the effect description.</span></span> <span data-ttu-id="5ff63-111">Se esse parâmetro for **NULL**, o módulo atual será usado.</span><span class="sxs-lookup"><span data-stu-id="5ff63-111">If this parameter is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="5ff63-112">*pSrcResource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5ff63-112">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ff63-113">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5ff63-113">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5ff63-114">Ponteiro para uma cadeia de caracteres que especifica o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="5ff63-114">Pointer to a string that specifies the resource name.</span></span>

</dd> <dt>

<span data-ttu-id="5ff63-115">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5ff63-115">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ff63-116">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="5ff63-116">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="5ff63-117">Uma matriz terminada **nula** opcional de estruturas [**D3DXMACRO**](d3dxmacro.md) .</span><span class="sxs-lookup"><span data-stu-id="5ff63-117">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="5ff63-118">Esse valor pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="5ff63-118">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5ff63-119">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5ff63-119">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ff63-120">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="5ff63-120">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="5ff63-121">Ponteiro de interface opcional, [**ID3DXInclude**](id3dxinclude.md), a ser usado para manipulação de \# diretivas include.</span><span class="sxs-lookup"><span data-stu-id="5ff63-121">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="5ff63-122">Se esse valor for **NULL**, \# inclusões será respeitado durante a compilação de um arquivo ou ocorrerá um erro quando compilado de um recurso ou memória.</span><span class="sxs-lookup"><span data-stu-id="5ff63-122">If this value is **NULL**, \#includes will either be honored when compiling from a file, or will error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="5ff63-123">*pFunctionName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5ff63-123">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ff63-124">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5ff63-124">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5ff63-125">Ponteiro para a função de ponto de entrada do sombreador onde a execução começa.</span><span class="sxs-lookup"><span data-stu-id="5ff63-125">Pointer to the shader entry point function where execution begins.</span></span>

</dd> <dt>

<span data-ttu-id="5ff63-126">*pProfile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5ff63-126">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ff63-127">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5ff63-127">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5ff63-128">Ponteiro para um perfil de sombreador que determina o conjunto de instruções do sombreador.</span><span class="sxs-lookup"><span data-stu-id="5ff63-128">Pointer to a shader profile which determines the shader instruction set.</span></span> <span data-ttu-id="5ff63-129">Consulte [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) ou [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) para obter uma lista dos perfis disponíveis.</span><span class="sxs-lookup"><span data-stu-id="5ff63-129">See [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) or [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) for a list of the profiles available.</span></span>

</dd> <dt>

<span data-ttu-id="5ff63-130">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="5ff63-130">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ff63-131">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5ff63-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5ff63-132">Opções de compilação identificadas por vários sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="5ff63-132">Compile options identified by various flags.</span></span> <span data-ttu-id="5ff63-133">O compilador do Direct3D 10 HLSL agora é o padrão.</span><span class="sxs-lookup"><span data-stu-id="5ff63-133">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="5ff63-134">Consulte [D3DXSHADER flags](d3dxshader-flags.md) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="5ff63-134">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="5ff63-135">*ppShader* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5ff63-135">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ff63-136">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="5ff63-136">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="5ff63-137">Retorna um buffer que contém o sombreador criado.</span><span class="sxs-lookup"><span data-stu-id="5ff63-137">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="5ff63-138">Esse buffer contém o código de sombreador compilado, bem como qualquer informação de tabela de depuração e símbolo inserida.</span><span class="sxs-lookup"><span data-stu-id="5ff63-138">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="5ff63-139">*ppErrorMsgs* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5ff63-139">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ff63-140">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="5ff63-140">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="5ff63-141">Retorna um buffer que contém uma lista de erros e avisos que foram encontrados durante a compilação.</span><span class="sxs-lookup"><span data-stu-id="5ff63-141">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="5ff63-142">Essas são as mesmas mensagens que o depurador exibe ao serem executados no modo de depuração.</span><span class="sxs-lookup"><span data-stu-id="5ff63-142">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="5ff63-143">Esse valor pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="5ff63-143">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5ff63-144">*ppConstantTable* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5ff63-144">*ppConstantTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ff63-145">Tipo: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span><span class="sxs-lookup"><span data-stu-id="5ff63-145">Type: **[**LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span></span>

<span data-ttu-id="5ff63-146">Retorna uma interface [**ID3DXConstantTable**](id3dxconstanttable.md) , que pode ser usada para acessar constantes de sombreador.</span><span class="sxs-lookup"><span data-stu-id="5ff63-146">Returns an [**ID3DXConstantTable**](id3dxconstanttable.md) interface, which can be used to access shader constants.</span></span> <span data-ttu-id="5ff63-147">Esse valor pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="5ff63-147">This value can be **NULL**.</span></span> <span data-ttu-id="5ff63-148">Se você compilar seu aplicativo como grande reconhecimento de endereço (ou seja, usar a opção de vinculador/LARGEADDRESSAWARE para tratar endereços maiores que 2 GB), não poderá usar esse parâmetro e deve defini-lo como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="5ff63-148">If you compile your application as large address aware (that is, you use the /LARGEADDRESSAWARE linker option to handle addresses larger than 2 GB), you cannot use this parameter and must set it to **NULL**.</span></span> <span data-ttu-id="5ff63-149">Em vez disso, você deve usar a função [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) para recuperar a tabela de constante de sombreador que está inserida dentro do sombreador.</span><span class="sxs-lookup"><span data-stu-id="5ff63-149">Instead, you must use the [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) function to retrieve the shader-constant table that is embedded inside the shader.</span></span> <span data-ttu-id="5ff63-150">Nesta chamada **D3DXGetShaderConstantTableEx** , você deve passar o sinalizador **D3DXCONSTTABLE \_ LARGEADDRESSAWARE** para o parâmetro *flags* para especificar o acesso a até 4 GB de espaço de endereço virtual.</span><span class="sxs-lookup"><span data-stu-id="5ff63-150">In this **D3DXGetShaderConstantTableEx** call, you must pass the **D3DXCONSTTABLE\_LARGEADDRESSAWARE** flag to the *Flags* parameter to specify to access up to 4 GB of virtual address space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ff63-151">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5ff63-151">Return value</span></span>

<span data-ttu-id="5ff63-152">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5ff63-152">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5ff63-153">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5ff63-153">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5ff63-154">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="5ff63-154">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ff63-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ff63-155">Requirements</span></span>



| <span data-ttu-id="5ff63-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ff63-156">Requirement</span></span> | <span data-ttu-id="5ff63-157">Valor</span><span class="sxs-lookup"><span data-stu-id="5ff63-157">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ff63-158">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ff63-158">Header</span></span><br/>  | <dl> <span data-ttu-id="5ff63-159"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ff63-159"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="5ff63-160">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5ff63-160">Library</span></span><br/> | <dl> <span data-ttu-id="5ff63-161"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5ff63-161"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="5ff63-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="5ff63-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ff63-163">Funções de sombreador</span><span class="sxs-lookup"><span data-stu-id="5ff63-163">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="5ff63-164">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="5ff63-164">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="5ff63-165">**D3DXCompileShaderFromFile**</span><span class="sxs-lookup"><span data-stu-id="5ff63-165">**D3DXCompileShaderFromFile**</span></span>](d3dxcompileshaderfromfile.md)
</dt> </dl>

 

 
