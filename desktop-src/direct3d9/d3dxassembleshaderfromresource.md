---
description: Função D3DXAssembleShaderFromResource – montar um sombreador.
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
ms.openlocfilehash: 78df978201df37269b7d33058effc16eadc9d16f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116013"
---
# <a name="d3dxassembleshaderfromresource-function"></a><span data-ttu-id="ec2c7-103">Função D3DXAssembleShaderFromResource</span><span class="sxs-lookup"><span data-stu-id="ec2c7-103">D3DXAssembleShaderFromResource function</span></span>

<span data-ttu-id="ec2c7-104">Monte um sombreador.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-104">Assemble a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec2c7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ec2c7-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="ec2c7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ec2c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec2c7-107">*hSrcModule* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ec2c7-107">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec2c7-108">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ec2c7-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ec2c7-109">Identificador para um módulo que contém a descrição do efeito.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-109">Handle to a module containing the effect description.</span></span> <span data-ttu-id="ec2c7-110">Se esse parâmetro for **NULL**, o módulo atual será usado.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-110">If this parameter is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="ec2c7-111">*pSrcResource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ec2c7-111">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec2c7-112">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ec2c7-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ec2c7-113">Ponteiro para uma cadeia de caracteres que especifica o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-113">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="ec2c7-114">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="ec2c7-115">Caso contrário, o tipo de dados String será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-115">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="ec2c7-116">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ec2c7-117">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ec2c7-117">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec2c7-118">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="ec2c7-118">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="ec2c7-119">Uma matriz terminada **nula** opcional de estruturas [**D3DXMACRO**](d3dxmacro.md) .</span><span class="sxs-lookup"><span data-stu-id="ec2c7-119">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="ec2c7-120">Esse valor pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-120">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ec2c7-121">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ec2c7-121">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec2c7-122">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="ec2c7-122">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="ec2c7-123">Ponteiro de interface opcional, [**ID3DXInclude**](id3dxinclude.md), a ser usado para manipulação de \# diretivas include.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-123">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="ec2c7-124">Se esse valor for **NULL**, \# incluirá que será respeitado durante a compilação de um arquivo ou causará um erro quando compilado de um recurso ou memória.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-124">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="ec2c7-125">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="ec2c7-125">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec2c7-126">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ec2c7-126">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ec2c7-127">Opções de compilação identificadas por vários sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-127">Compile options identified by various flags.</span></span> <span data-ttu-id="ec2c7-128">O compilador do Direct3D 10 HLSL agora é o padrão.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-128">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="ec2c7-129">Consulte [D3DXSHADER flags](d3dxshader-flags.md) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-129">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="ec2c7-130">*ppShader* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ec2c7-130">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ec2c7-131">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="ec2c7-131">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="ec2c7-132">Retorna um buffer que contém o sombreador criado.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-132">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="ec2c7-133">Esse buffer contém o código de sombreador compilado, bem como qualquer informação de tabela de depuração e símbolo inserida.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-133">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="ec2c7-134">*ppErrorMsgs* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ec2c7-134">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ec2c7-135">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="ec2c7-135">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="ec2c7-136">Retorna um buffer que contém uma lista de erros e avisos que foram encontrados durante a compilação.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-136">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="ec2c7-137">Essas são as mesmas mensagens que o depurador exibe ao serem executados no modo de depuração.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-137">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="ec2c7-138">Esse valor pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-138">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec2c7-139">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="ec2c7-139">Return value</span></span>

<span data-ttu-id="ec2c7-140">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ec2c7-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ec2c7-141">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-141">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ec2c7-142">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-142">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec2c7-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="ec2c7-143">Remarks</span></span>

<span data-ttu-id="ec2c7-144">A configuração do compilador também determina a versão da função.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-144">The compiler setting also determines the function version.</span></span> <span data-ttu-id="ec2c7-145">Se o Unicode for definido, a chamada de função será resolvida como D3DXAssembleShaderFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-145">If Unicode is defined, the function call resolves to D3DXAssembleShaderFromResourceW.</span></span> <span data-ttu-id="ec2c7-146">Caso contrário, a chamada de função é resolvida como D3DXAssembleShaderFromResourceA porque as cadeias de caracteres ANSI estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-146">Otherwise, the function call resolves to D3DXAssembleShaderFromResourceA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec2c7-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec2c7-147">Requirements</span></span>



| <span data-ttu-id="ec2c7-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec2c7-148">Requirement</span></span> | <span data-ttu-id="ec2c7-149">Valor</span><span class="sxs-lookup"><span data-stu-id="ec2c7-149">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec2c7-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ec2c7-150">Header</span></span><br/>  | <dl> <span data-ttu-id="ec2c7-151"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec2c7-151"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="ec2c7-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ec2c7-152">Library</span></span><br/> | <dl> <span data-ttu-id="ec2c7-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ec2c7-153"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ec2c7-154">Consulte também</span><span class="sxs-lookup"><span data-stu-id="ec2c7-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec2c7-155">Funções de sombreador</span><span class="sxs-lookup"><span data-stu-id="ec2c7-155">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="ec2c7-156">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="ec2c7-156">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="ec2c7-157">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="ec2c7-157">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
