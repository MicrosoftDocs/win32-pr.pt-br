---
description: Cria um compilador de efeito a partir de uma descrição de efeito ASCII.
ms.assetid: 87438a1e-4149-42ef-aa7a-9f0549eb7982
title: Função D3DXCreateEffectCompilerFromFile (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectCompilerFromFile
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: fe27683078f77d7d444bd3a763fc326e749f7517
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105785959"
---
# <a name="d3dxcreateeffectcompilerfromfile-function"></a><span data-ttu-id="1e3c1-103">Função D3DXCreateEffectCompilerFromFile</span><span class="sxs-lookup"><span data-stu-id="1e3c1-103">D3DXCreateEffectCompilerFromFile function</span></span>

<span data-ttu-id="1e3c1-104">Cria um compilador de efeito a partir de uma descrição de efeito ASCII.</span><span class="sxs-lookup"><span data-stu-id="1e3c1-104">Creates an effect compiler from an ASCII effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e3c1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1e3c1-105">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectCompilerFromFile(
  _In_        LPCTSTR              pSrcFile,
  _In_  const D3DXMACRO            *pDefines,
  _In_        LPD3DXINCLUDE        pInclude,
  _In_        DWORD                Flags,
  _Out_       LPD3DXEFFECTCOMPILER *ppEffectCompiler,
  _Out_       LPD3DXBUFFER         *ppParseErrors
);
```



## <a name="parameters"></a><span data-ttu-id="1e3c1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1e3c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e3c1-107">*pSrcFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1e3c1-107">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e3c1-108">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1e3c1-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1e3c1-109">Ponteiro para o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="1e3c1-109">Pointer to the filename.</span></span> <span data-ttu-id="1e3c1-110">Esse parâmetro dá suporte a cadeias de caracteres Unicode e ANSI.</span><span class="sxs-lookup"><span data-stu-id="1e3c1-110">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="1e3c1-111">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="1e3c1-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1e3c1-112">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1e3c1-112">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e3c1-113">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="1e3c1-113">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="1e3c1-114">Uma matriz opcional com terminação **nula** de estruturas [**D3DXMACRO**](d3dxmacro.md) que descrevem as definições de pré-processador.</span><span class="sxs-lookup"><span data-stu-id="1e3c1-114">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="1e3c1-115">Esse valor pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="1e3c1-115">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1e3c1-116">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1e3c1-116">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e3c1-117">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="1e3c1-117">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="1e3c1-118">Ponteiro de interface opcional, [**ID3DXInclude**](id3dxinclude.md), a ser usado para manipulação de \# diretivas include.</span><span class="sxs-lookup"><span data-stu-id="1e3c1-118">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="1e3c1-119">Se esse valor for **NULL**, \# incluirá que será respeitado durante a compilação de um arquivo ou causará um erro quando compilado de um recurso ou memória.</span><span class="sxs-lookup"><span data-stu-id="1e3c1-119">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="1e3c1-120">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="1e3c1-120">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e3c1-121">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1e3c1-121">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1e3c1-122">Opções de compilação identificadas por vários sinalizadores (consulte [sinalizadores D3DXSHADER](d3dxshader-flags.md)).</span><span class="sxs-lookup"><span data-stu-id="1e3c1-122">Compile options identified by various flags (see [D3DXSHADER Flags](d3dxshader-flags.md)).</span></span> <span data-ttu-id="1e3c1-123">O compilador do Direct3D 10 HLSL agora é o padrão.</span><span class="sxs-lookup"><span data-stu-id="1e3c1-123">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="1e3c1-124">Confira [ferramenta de compilador de efeito](../direct3dtools/fxc.md) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="1e3c1-124">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="1e3c1-125">*ppEffectCompiler* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1e3c1-125">*ppEffectCompiler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e3c1-126">Tipo: **[ **LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span><span class="sxs-lookup"><span data-stu-id="1e3c1-126">Type: **[**LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span></span>

<span data-ttu-id="1e3c1-127">Endereço de um ponteiro para uma interface [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) , que contém o compilador de efeito.</span><span class="sxs-lookup"><span data-stu-id="1e3c1-127">Address of a pointer to an [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) interface, containing the effect compiler.</span></span>

</dd> <dt>

<span data-ttu-id="1e3c1-128">*ppParseErrors* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1e3c1-128">*ppParseErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e3c1-129">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="1e3c1-129">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="1e3c1-130">Endereço de um ponteiro para uma interface [**ID3DXBuffer**](id3dxbuffer.md) , contendo todas as mensagens de erro ocorridas durante a compilação.</span><span class="sxs-lookup"><span data-stu-id="1e3c1-130">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, containing any error messages that occurred during compilation.</span></span> <span data-ttu-id="1e3c1-131">Esse parâmetro pode ser definido como **nulo** para ignorar mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="1e3c1-131">This parameter can be set to **NULL** to ignore error messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e3c1-132">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1e3c1-132">Return value</span></span>

<span data-ttu-id="1e3c1-133">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1e3c1-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1e3c1-134">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1e3c1-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1e3c1-135">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="1e3c1-135">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e3c1-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="1e3c1-136">Remarks</span></span>

<span data-ttu-id="1e3c1-137">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="1e3c1-137">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="1e3c1-138">Caso contrário, o tipo de dados LPCTSTR será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="1e3c1-138">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="1e3c1-139">A configuração do compilador também determina a versão da função.</span><span class="sxs-lookup"><span data-stu-id="1e3c1-139">The compiler setting also determines the function version.</span></span> <span data-ttu-id="1e3c1-140">Se o Unicode for definido, a chamada de função será resolvida como D3DXCreateEffectCompilerFromFileW.</span><span class="sxs-lookup"><span data-stu-id="1e3c1-140">If Unicode is defined, the function call resolves to D3DXCreateEffectCompilerFromFileW.</span></span> <span data-ttu-id="1e3c1-141">Caso contrário, a chamada de função é resolvida como D3DXCreateEffectCompilerFromFileA porque as cadeias de caracteres ANSI estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="1e3c1-141">Otherwise, the function call resolves to D3DXCreateEffectCompilerFromFileA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e3c1-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e3c1-142">Requirements</span></span>



| <span data-ttu-id="1e3c1-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e3c1-143">Requirement</span></span> | <span data-ttu-id="1e3c1-144">Valor</span><span class="sxs-lookup"><span data-stu-id="1e3c1-144">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e3c1-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1e3c1-145">Header</span></span><br/>  | <dl> <span data-ttu-id="1e3c1-146"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e3c1-146"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="1e3c1-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1e3c1-147">Library</span></span><br/> | <dl> <span data-ttu-id="1e3c1-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1e3c1-148"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="1e3c1-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="1e3c1-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e3c1-150">Funções de efeito</span><span class="sxs-lookup"><span data-stu-id="1e3c1-150">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="1e3c1-151">**D3DXCreateEffectCompiler**</span><span class="sxs-lookup"><span data-stu-id="1e3c1-151">**D3DXCreateEffectCompiler**</span></span>](d3dxcreateeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="1e3c1-152">**D3DXCreateEffectCompilerFromResource**</span><span class="sxs-lookup"><span data-stu-id="1e3c1-152">**D3DXCreateEffectCompilerFromResource**</span></span>](d3dxcreateeffectcompilerfromresource.md)
</dt> </dl>

 

 
