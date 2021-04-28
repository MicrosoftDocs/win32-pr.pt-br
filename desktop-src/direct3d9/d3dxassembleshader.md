---
description: Função D3DXAssembleShader – montar um sombreador.
ms.assetid: 24c3dcae-9397-4856-b072-0ae340157bf9
title: Função D3DXAssembleShader (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXAssembleShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 891281ebc3db970ca61132fe49ba98531ca1d879
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116044"
---
# <a name="d3dxassembleshader-function"></a><span data-ttu-id="28324-103">Função D3DXAssembleShader</span><span class="sxs-lookup"><span data-stu-id="28324-103">D3DXAssembleShader function</span></span>

<span data-ttu-id="28324-104">Monte um sombreador.</span><span class="sxs-lookup"><span data-stu-id="28324-104">Assemble a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="28324-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="28324-105">Syntax</span></span>


```C++
HRESULT D3DXAssembleShader(
  _In_        LPCSTR        pSrcData,
  _In_        UINT          SrcDataLen,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _In_        DWORD         Flags,
  _Out_       LPD3DXBUFFER  *ppShader,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="28324-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="28324-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28324-107">*pSrcData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="28324-107">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28324-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="28324-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="28324-109">Ponteiro para um buffer de memória que contém os dados do sombreador.</span><span class="sxs-lookup"><span data-stu-id="28324-109">Pointer to a memory buffer that contains the shader data.</span></span>

</dd> <dt>

<span data-ttu-id="28324-110">*SrcDataLen* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="28324-110">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28324-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="28324-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="28324-112">Comprimento dos dados de efeito, em bytes.</span><span class="sxs-lookup"><span data-stu-id="28324-112">Length of the effect data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="28324-113">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="28324-113">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28324-114">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="28324-114">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="28324-115">Uma matriz terminada **nula** opcional de estruturas [**D3DXMACRO**](d3dxmacro.md) .</span><span class="sxs-lookup"><span data-stu-id="28324-115">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="28324-116">Esse valor pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="28324-116">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="28324-117">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="28324-117">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28324-118">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="28324-118">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="28324-119">Ponteiro de interface opcional, [**ID3DXInclude**](id3dxinclude.md), a ser usado para manipulação de \# diretivas include.</span><span class="sxs-lookup"><span data-stu-id="28324-119">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="28324-120">Se esse valor for **NULL**, \# incluirá que será respeitado durante a compilação de um arquivo ou causará um erro quando compilado de um recurso ou memória.</span><span class="sxs-lookup"><span data-stu-id="28324-120">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="28324-121">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="28324-121">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28324-122">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="28324-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="28324-123">Opções de compilação identificadas por vários sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="28324-123">Compile options identified by various flags.</span></span> <span data-ttu-id="28324-124">O compilador do Direct3D 10 HLSL agora é o padrão.</span><span class="sxs-lookup"><span data-stu-id="28324-124">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="28324-125">Consulte [D3DXSHADER flags](d3dxshader-flags.md) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="28324-125">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="28324-126">*ppShader* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="28324-126">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28324-127">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="28324-127">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="28324-128">Retorna um buffer que contém o sombreador criado.</span><span class="sxs-lookup"><span data-stu-id="28324-128">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="28324-129">Esse buffer contém o código de sombreador compilado, bem como qualquer informação de tabela de depuração e símbolo inserida.</span><span class="sxs-lookup"><span data-stu-id="28324-129">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="28324-130">*ppErrorMsgs* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="28324-130">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28324-131">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="28324-131">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="28324-132">Retorna um buffer que contém uma lista de erros e avisos que foram encontrados durante a compilação.</span><span class="sxs-lookup"><span data-stu-id="28324-132">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="28324-133">Essas são as mesmas mensagens que o depurador exibe ao serem executados no modo de depuração.</span><span class="sxs-lookup"><span data-stu-id="28324-133">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="28324-134">Esse valor pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="28324-134">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28324-135">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="28324-135">Return value</span></span>

<span data-ttu-id="28324-136">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="28324-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="28324-137">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="28324-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="28324-138">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="28324-138">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="28324-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28324-139">Requirements</span></span>



| <span data-ttu-id="28324-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="28324-140">Requirement</span></span> | <span data-ttu-id="28324-141">Valor</span><span class="sxs-lookup"><span data-stu-id="28324-141">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="28324-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="28324-142">Header</span></span><br/>  | <dl> <span data-ttu-id="28324-143"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="28324-143"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="28324-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="28324-144">Library</span></span><br/> | <dl> <span data-ttu-id="28324-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="28324-145"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="28324-146">Consulte também</span><span class="sxs-lookup"><span data-stu-id="28324-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28324-147">Funções de sombreador</span><span class="sxs-lookup"><span data-stu-id="28324-147">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="28324-148">**D3DXAssembleShaderFromFile**</span><span class="sxs-lookup"><span data-stu-id="28324-148">**D3DXAssembleShaderFromFile**</span></span>](d3dxassembleshaderfromfile.md)
</dt> <dt>

[<span data-ttu-id="28324-149">**D3DXAssembleShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="28324-149">**D3DXAssembleShaderFromResource**</span></span>](d3dxassembleshaderfromresource.md)
</dt> </dl>

 

 
