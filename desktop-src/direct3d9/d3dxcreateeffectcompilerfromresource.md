---
description: Cria um ID3DXEffectCompiler a partir de uma descrição de efeito ASCII.
ms.assetid: 041e0a3f-3dc6-4cc3-8380-d4a79a3f647a
title: Função D3DXCreateEffectCompilerFromResource (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectCompilerFromResource
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 1a3dabe0a2690c84e125af6d321397cbe3765f83
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173051"
---
# <a name="d3dxcreateeffectcompilerfromresource-function"></a><span data-ttu-id="0bdab-103">Função D3DXCreateEffectCompilerFromResource</span><span class="sxs-lookup"><span data-stu-id="0bdab-103">D3DXCreateEffectCompilerFromResource function</span></span>

<span data-ttu-id="0bdab-104">Cria um [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) a partir de uma descrição de efeito ASCII.</span><span class="sxs-lookup"><span data-stu-id="0bdab-104">Creates an [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) from an ASCII effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bdab-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0bdab-105">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectCompilerFromResource(
  _In_        HMODULE              hSrcModule,
  _In_        LPCTSTR              pSrcResource,
  _In_  const D3DXMACRO            *pDefines,
  _In_        LPD3DXINCLUDE        pInclude,
  _In_        DWORD                Flags,
  _Out_       LPD3DXEFFECTCOMPILER *ppEffectCompiler,
  _Out_       LPD3DXBUFFER         *ppParseErrors
);
```



## <a name="parameters"></a><span data-ttu-id="0bdab-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0bdab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bdab-107">*hSrcModule* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0bdab-107">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bdab-108">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0bdab-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0bdab-109">Identificador para um módulo que contém a descrição do efeito.</span><span class="sxs-lookup"><span data-stu-id="0bdab-109">Handle to a module containing the effect description.</span></span> <span data-ttu-id="0bdab-110">Se esse parâmetro for **NULL**, o módulo atual será usado.</span><span class="sxs-lookup"><span data-stu-id="0bdab-110">If this parameter is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="0bdab-111">*pSrcResource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0bdab-111">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bdab-112">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0bdab-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0bdab-113">Ponteiro para o recurso.</span><span class="sxs-lookup"><span data-stu-id="0bdab-113">Pointer to the resource.</span></span> <span data-ttu-id="0bdab-114">Esse parâmetro dá suporte a cadeias de caracteres Unicode e ANSI.</span><span class="sxs-lookup"><span data-stu-id="0bdab-114">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="0bdab-115">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="0bdab-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="0bdab-116">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0bdab-116">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bdab-117">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="0bdab-117">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="0bdab-118">Uma matriz opcional com terminação **nula** de estruturas [**D3DXMACRO**](d3dxmacro.md) que descrevem as definições de pré-processador.</span><span class="sxs-lookup"><span data-stu-id="0bdab-118">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="0bdab-119">Esse valor pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="0bdab-119">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0bdab-120">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0bdab-120">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bdab-121">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="0bdab-121">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="0bdab-122">Ponteiro de interface opcional, [**ID3DXInclude**](id3dxinclude.md), a ser usado para manipulação de \# diretivas include.</span><span class="sxs-lookup"><span data-stu-id="0bdab-122">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="0bdab-123">Se esse valor for **NULL**, \# incluirá que será respeitado durante a compilação de um arquivo ou causará um erro quando compilado de um recurso ou memória.</span><span class="sxs-lookup"><span data-stu-id="0bdab-123">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="0bdab-124">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="0bdab-124">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bdab-125">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0bdab-125">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0bdab-126">Opções de compilação identificadas por vários sinalizadores (consulte [sinalizadores D3DXSHADER](d3dxshader-flags.md)).</span><span class="sxs-lookup"><span data-stu-id="0bdab-126">Compile options identified by various flags (see [D3DXSHADER Flags](d3dxshader-flags.md)).</span></span> <span data-ttu-id="0bdab-127">O compilador do Direct3D 10 HLSL agora é o padrão.</span><span class="sxs-lookup"><span data-stu-id="0bdab-127">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="0bdab-128">Confira [ferramenta de compilador de efeito](../direct3dtools/fxc.md) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="0bdab-128">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="0bdab-129">*ppEffectCompiler* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0bdab-129">*ppEffectCompiler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0bdab-130">Tipo: **[ **LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span><span class="sxs-lookup"><span data-stu-id="0bdab-130">Type: **[**LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span></span>

<span data-ttu-id="0bdab-131">Endereço de um ponteiro para uma interface [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) , que contém o compilador de efeito.</span><span class="sxs-lookup"><span data-stu-id="0bdab-131">Address of a pointer to an [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) interface, containing the effect compiler.</span></span>

</dd> <dt>

<span data-ttu-id="0bdab-132">*ppParseErrors* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0bdab-132">*ppParseErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0bdab-133">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="0bdab-133">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="0bdab-134">Endereço de um ponteiro para uma interface [**ID3DXBuffer**](id3dxbuffer.md) , contendo todas as mensagens de erro ocorridas durante a compilação.</span><span class="sxs-lookup"><span data-stu-id="0bdab-134">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, containing any error messages that occurred during compilation.</span></span> <span data-ttu-id="0bdab-135">Esse parâmetro pode ser definido como **nulo** para ignorar mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="0bdab-135">This parameter can be set to **NULL** to ignore error messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bdab-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0bdab-136">Return value</span></span>

<span data-ttu-id="0bdab-137">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0bdab-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0bdab-138">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0bdab-138">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0bdab-139">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="0bdab-139">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bdab-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="0bdab-140">Remarks</span></span>

<span data-ttu-id="0bdab-141">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="0bdab-141">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="0bdab-142">Caso contrário, o tipo de dados LPCTSTR será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="0bdab-142">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="0bdab-143">A configuração do compilador também determina a versão da função.</span><span class="sxs-lookup"><span data-stu-id="0bdab-143">The compiler setting also determines the function version.</span></span> <span data-ttu-id="0bdab-144">Se o Unicode for definido, a chamada de função será resolvida como D3DXCreateEffectCompilerFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="0bdab-144">If Unicode is defined, the function call resolves to D3DXCreateEffectCompilerFromResourceW.</span></span> <span data-ttu-id="0bdab-145">Caso contrário, a chamada de função é resolvida como D3DXCreateEffectCompilerFromResourceA porque as cadeias de caracteres ANSI estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="0bdab-145">Otherwise, the function call resolves to D3DXCreateEffectCompilerFromResourceA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bdab-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0bdab-146">Requirements</span></span>



| <span data-ttu-id="0bdab-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="0bdab-147">Requirement</span></span> | <span data-ttu-id="0bdab-148">Valor</span><span class="sxs-lookup"><span data-stu-id="0bdab-148">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bdab-149">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0bdab-149">Header</span></span><br/>  | <dl> <span data-ttu-id="0bdab-150"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="0bdab-150"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="0bdab-151">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0bdab-151">Library</span></span><br/> | <dl> <span data-ttu-id="0bdab-152"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0bdab-152"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0bdab-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="0bdab-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bdab-154">Funções de efeito</span><span class="sxs-lookup"><span data-stu-id="0bdab-154">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="0bdab-155">**D3DXCreateEffectCompiler**</span><span class="sxs-lookup"><span data-stu-id="0bdab-155">**D3DXCreateEffectCompiler**</span></span>](d3dxcreateeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="0bdab-156">**D3DXCreateEffectCompilerFromFile**</span><span class="sxs-lookup"><span data-stu-id="0bdab-156">**D3DXCreateEffectCompilerFromFile**</span></span>](d3dxcreateeffectcompilerfromfile.md)
</dt> </dl>

 

 
