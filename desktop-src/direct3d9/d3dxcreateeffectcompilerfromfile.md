---
description: Função D3DXCreateEffectCompilerFromFile – cria um compilador de efeito a partir de uma descrição de efeito ASCII.
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
ms.openlocfilehash: 0c054b31b1ab70d1378c794be13058204b994ee2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087974"
---
# <a name="d3dxcreateeffectcompilerfromfile-function"></a><span data-ttu-id="7e88e-103">Função D3DXCreateEffectCompilerFromFile</span><span class="sxs-lookup"><span data-stu-id="7e88e-103">D3DXCreateEffectCompilerFromFile function</span></span>

<span data-ttu-id="7e88e-104">Cria um compilador de efeito a partir de uma descrição de efeito ASCII.</span><span class="sxs-lookup"><span data-stu-id="7e88e-104">Creates an effect compiler from an ASCII effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e88e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7e88e-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="7e88e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7e88e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e88e-107">*pSrcFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7e88e-107">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e88e-108">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7e88e-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7e88e-109">Ponteiro para o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="7e88e-109">Pointer to the filename.</span></span> <span data-ttu-id="7e88e-110">Esse parâmetro dá suporte a cadeias de caracteres Unicode e ANSI.</span><span class="sxs-lookup"><span data-stu-id="7e88e-110">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="7e88e-111">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="7e88e-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="7e88e-112">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7e88e-112">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e88e-113">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="7e88e-113">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="7e88e-114">Uma matriz opcional com terminação **nula** de estruturas [**D3DXMACRO**](d3dxmacro.md) que descrevem as definições de pré-processador.</span><span class="sxs-lookup"><span data-stu-id="7e88e-114">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="7e88e-115">Esse valor pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="7e88e-115">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7e88e-116">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7e88e-116">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e88e-117">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="7e88e-117">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="7e88e-118">Ponteiro de interface opcional, [**ID3DXInclude**](id3dxinclude.md), a ser usado para manipulação de \# diretivas include.</span><span class="sxs-lookup"><span data-stu-id="7e88e-118">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="7e88e-119">Se esse valor for **NULL**, \# incluirá que será respeitado durante a compilação de um arquivo ou causará um erro quando compilado de um recurso ou memória.</span><span class="sxs-lookup"><span data-stu-id="7e88e-119">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="7e88e-120">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="7e88e-120">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e88e-121">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7e88e-121">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7e88e-122">Opções de compilação identificadas por vários sinalizadores (consulte [sinalizadores D3DXSHADER](d3dxshader-flags.md)).</span><span class="sxs-lookup"><span data-stu-id="7e88e-122">Compile options identified by various flags (see [D3DXSHADER Flags](d3dxshader-flags.md)).</span></span> <span data-ttu-id="7e88e-123">O compilador do Direct3D 10 HLSL agora é o padrão.</span><span class="sxs-lookup"><span data-stu-id="7e88e-123">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="7e88e-124">Confira [ferramenta de compilador de efeito](../direct3dtools/fxc.md) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="7e88e-124">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="7e88e-125">*ppEffectCompiler* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7e88e-125">*ppEffectCompiler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7e88e-126">Tipo: **[ **LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span><span class="sxs-lookup"><span data-stu-id="7e88e-126">Type: **[**LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span></span>

<span data-ttu-id="7e88e-127">Endereço de um ponteiro para uma interface [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) , que contém o compilador de efeito.</span><span class="sxs-lookup"><span data-stu-id="7e88e-127">Address of a pointer to an [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) interface, containing the effect compiler.</span></span>

</dd> <dt>

<span data-ttu-id="7e88e-128">*ppParseErrors* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7e88e-128">*ppParseErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7e88e-129">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="7e88e-129">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="7e88e-130">Endereço de um ponteiro para uma interface [**ID3DXBuffer**](id3dxbuffer.md) , contendo todas as mensagens de erro ocorridas durante a compilação.</span><span class="sxs-lookup"><span data-stu-id="7e88e-130">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, containing any error messages that occurred during compilation.</span></span> <span data-ttu-id="7e88e-131">Esse parâmetro pode ser definido como **nulo** para ignorar mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="7e88e-131">This parameter can be set to **NULL** to ignore error messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e88e-132">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="7e88e-132">Return value</span></span>

<span data-ttu-id="7e88e-133">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7e88e-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7e88e-134">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7e88e-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7e88e-135">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="7e88e-135">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e88e-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="7e88e-136">Remarks</span></span>

<span data-ttu-id="7e88e-137">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="7e88e-137">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="7e88e-138">Caso contrário, o tipo de dados LPCTSTR será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="7e88e-138">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="7e88e-139">A configuração do compilador também determina a versão da função.</span><span class="sxs-lookup"><span data-stu-id="7e88e-139">The compiler setting also determines the function version.</span></span> <span data-ttu-id="7e88e-140">Se o Unicode for definido, a chamada de função será resolvida como D3DXCreateEffectCompilerFromFileW.</span><span class="sxs-lookup"><span data-stu-id="7e88e-140">If Unicode is defined, the function call resolves to D3DXCreateEffectCompilerFromFileW.</span></span> <span data-ttu-id="7e88e-141">Caso contrário, a chamada de função é resolvida como D3DXCreateEffectCompilerFromFileA porque as cadeias de caracteres ANSI estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="7e88e-141">Otherwise, the function call resolves to D3DXCreateEffectCompilerFromFileA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e88e-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e88e-142">Requirements</span></span>



| <span data-ttu-id="7e88e-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e88e-143">Requirement</span></span> | <span data-ttu-id="7e88e-144">Valor</span><span class="sxs-lookup"><span data-stu-id="7e88e-144">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e88e-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7e88e-145">Header</span></span><br/>  | <dl> <span data-ttu-id="7e88e-146"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e88e-146"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="7e88e-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7e88e-147">Library</span></span><br/> | <dl> <span data-ttu-id="7e88e-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7e88e-148"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7e88e-149">Consulte também</span><span class="sxs-lookup"><span data-stu-id="7e88e-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e88e-150">Funções de efeito</span><span class="sxs-lookup"><span data-stu-id="7e88e-150">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="7e88e-151">**D3DXCreateEffectCompiler**</span><span class="sxs-lookup"><span data-stu-id="7e88e-151">**D3DXCreateEffectCompiler**</span></span>](d3dxcreateeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="7e88e-152">**D3DXCreateEffectCompilerFromResource**</span><span class="sxs-lookup"><span data-stu-id="7e88e-152">**D3DXCreateEffectCompilerFromResource**</span></span>](d3dxcreateeffectcompilerfromresource.md)
</dt> </dl>

 

 
