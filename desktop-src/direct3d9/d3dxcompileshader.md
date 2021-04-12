---
description: Compilar um arquivo de sombreador.
ms.assetid: 9b19ab67-d5d5-482d-b3fe-ce20b64d7ad8
title: Função D3DXCompileShader (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCompileShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 65dd9f74280abe7ee2fe427a4772b14b88742e97
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298595"
---
# <a name="d3dxcompileshader-function"></a><span data-ttu-id="485da-103">Função D3DXCompileShader</span><span class="sxs-lookup"><span data-stu-id="485da-103">D3DXCompileShader function</span></span>

<span data-ttu-id="485da-104">Compilar um arquivo de sombreador.</span><span class="sxs-lookup"><span data-stu-id="485da-104">Compile a shader file.</span></span>

> [!Note]  
> <span data-ttu-id="485da-105">Em vez de usar essa função herdada, recomendamos que você compile offline usando o compilador de linha de comando Fxc.exe ou use a API [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) .</span><span class="sxs-lookup"><span data-stu-id="485da-105">Instead of using this legacy function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="485da-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="485da-106">Syntax</span></span>


```C++
HRESULT D3DXCompileShader(
  _In_        LPCSTR              pSrcData,
  _In_        UINT                srcDataLen,
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



## <a name="parameters"></a><span data-ttu-id="485da-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="485da-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="485da-108">*pSrcData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="485da-108">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="485da-109">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="485da-109">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="485da-110">Ponteiro para uma cadeia de caracteres que contém o sombreador.</span><span class="sxs-lookup"><span data-stu-id="485da-110">Pointer to a string that contains the shader.</span></span>

</dd> <dt>

<span data-ttu-id="485da-111">*srcDataLen* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="485da-111">*srcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="485da-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="485da-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="485da-113">Comprimento dos dados em bytes.</span><span class="sxs-lookup"><span data-stu-id="485da-113">Length of the data in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="485da-114">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="485da-114">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="485da-115">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="485da-115">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="485da-116">Uma matriz terminada **nula** opcional de estruturas [**D3DXMACRO**](d3dxmacro.md) .</span><span class="sxs-lookup"><span data-stu-id="485da-116">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="485da-117">Esse valor pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="485da-117">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="485da-118">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="485da-118">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="485da-119">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="485da-119">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="485da-120">Ponteiro de interface opcional, [**ID3DXInclude**](id3dxinclude.md), a ser usado para manipulação de \# diretivas include.</span><span class="sxs-lookup"><span data-stu-id="485da-120">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="485da-121">Se esse valor for **NULL**, \# incluirá que será respeitado durante a compilação de um arquivo ou causará um erro quando compilado de um recurso ou memória.</span><span class="sxs-lookup"><span data-stu-id="485da-121">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="485da-122">*pFunctionName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="485da-122">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="485da-123">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="485da-123">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="485da-124">Ponteiro para uma cadeia de caracteres que contém o nome da função de ponto de entrada do sombreador onde a execução começa.</span><span class="sxs-lookup"><span data-stu-id="485da-124">Pointer to a string that contains the name of the shader entry point function where execution begins.</span></span>

</dd> <dt>

<span data-ttu-id="485da-125">*pProfile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="485da-125">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="485da-126">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="485da-126">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="485da-127">Ponteiro para um perfil de sombreador que determina o conjunto de instruções do sombreador.</span><span class="sxs-lookup"><span data-stu-id="485da-127">Pointer to a shader profile which determines the shader instruction set.</span></span> <span data-ttu-id="485da-128">Consulte [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) ou [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) para obter uma lista dos perfis disponíveis.</span><span class="sxs-lookup"><span data-stu-id="485da-128">See [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) or [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) for a list of the profiles available.</span></span>

</dd> <dt>

<span data-ttu-id="485da-129">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="485da-129">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="485da-130">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="485da-130">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="485da-131">Opções de compilação identificadas por vários sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="485da-131">Compile options identified by various flags.</span></span> <span data-ttu-id="485da-132">O compilador do Direct3D 10 HLSL agora é o padrão.</span><span class="sxs-lookup"><span data-stu-id="485da-132">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="485da-133">Consulte [D3DXSHADER flags](d3dxshader-flags.md) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="485da-133">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="485da-134">*ppShader* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="485da-134">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="485da-135">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="485da-135">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="485da-136">Retorna um buffer que contém o sombreador criado.</span><span class="sxs-lookup"><span data-stu-id="485da-136">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="485da-137">Esse buffer contém o código de sombreador compilado, bem como qualquer informação de tabela de depuração e símbolo inserida.</span><span class="sxs-lookup"><span data-stu-id="485da-137">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="485da-138">*ppErrorMsgs* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="485da-138">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="485da-139">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="485da-139">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="485da-140">Retorna um buffer que contém uma lista de erros e avisos que foram encontrados durante a compilação.</span><span class="sxs-lookup"><span data-stu-id="485da-140">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="485da-141">Essas são as mesmas mensagens que o depurador exibe ao serem executados no modo de depuração.</span><span class="sxs-lookup"><span data-stu-id="485da-141">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="485da-142">Esse valor pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="485da-142">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="485da-143">*ppConstantTable* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="485da-143">*ppConstantTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="485da-144">Tipo: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span><span class="sxs-lookup"><span data-stu-id="485da-144">Type: **[**LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span></span>

<span data-ttu-id="485da-145">Retorna uma interface [**ID3DXConstantTable**](id3dxconstanttable.md) , que pode ser usada para acessar constantes de sombreador.</span><span class="sxs-lookup"><span data-stu-id="485da-145">Returns an [**ID3DXConstantTable**](id3dxconstanttable.md) interface, which can be used to access shader constants.</span></span> <span data-ttu-id="485da-146">Esse valor pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="485da-146">This value can be **NULL**.</span></span> <span data-ttu-id="485da-147">Se você compilar seu aplicativo como grande reconhecimento de endereço (ou seja, usar a opção de vinculador/LARGEADDRESSAWARE para tratar endereços maiores que 2 GB), não poderá usar esse parâmetro e deve defini-lo como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="485da-147">If you compile your application as large address aware (that is, you use the /LARGEADDRESSAWARE linker option to handle addresses larger than 2 GB), you cannot use this parameter and must set it to **NULL**.</span></span> <span data-ttu-id="485da-148">Em vez disso, você deve usar a função [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) para recuperar a tabela de constante de sombreador que está inserida dentro do sombreador.</span><span class="sxs-lookup"><span data-stu-id="485da-148">Instead, you must use the [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) function to retrieve the shader-constant table that is embedded inside the shader.</span></span> <span data-ttu-id="485da-149">Nesta chamada **D3DXGetShaderConstantTableEx** , você deve passar o sinalizador **D3DXCONSTTABLE \_ LARGEADDRESSAWARE** para o parâmetro *flags* para especificar o acesso a até 4 GB de espaço de endereço virtual.</span><span class="sxs-lookup"><span data-stu-id="485da-149">In this **D3DXGetShaderConstantTableEx** call, you must pass the **D3DXCONSTTABLE\_LARGEADDRESSAWARE** flag to the *Flags* parameter to specify to access up to 4 GB of virtual address space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="485da-150">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="485da-150">Return value</span></span>

<span data-ttu-id="485da-151">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="485da-151">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="485da-152">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="485da-152">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="485da-153">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="485da-153">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="485da-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="485da-154">Requirements</span></span>



| <span data-ttu-id="485da-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="485da-155">Requirement</span></span> | <span data-ttu-id="485da-156">Valor</span><span class="sxs-lookup"><span data-stu-id="485da-156">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="485da-157">parâmetro</span><span class="sxs-lookup"><span data-stu-id="485da-157">Header</span></span><br/>  | <dl> <span data-ttu-id="485da-158"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="485da-158"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="485da-159">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="485da-159">Library</span></span><br/> | <dl> <span data-ttu-id="485da-160"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="485da-160"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="485da-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="485da-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="485da-162">Funções de sombreador</span><span class="sxs-lookup"><span data-stu-id="485da-162">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="485da-163">**D3DXCompileShaderFromFile**</span><span class="sxs-lookup"><span data-stu-id="485da-163">**D3DXCompileShaderFromFile**</span></span>](d3dxcompileshaderfromfile.md)
</dt> <dt>

[<span data-ttu-id="485da-164">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="485da-164">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
