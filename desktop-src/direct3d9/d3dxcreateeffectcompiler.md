---
description: Cria um compilador de efeito a partir de uma descrição de efeito ASCII.
ms.assetid: 96e883f4-4055-4b8b-940a-164bbf893af4
title: Função D3DXCreateEffectCompiler (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectCompiler
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 513b11ba12abe05126c122f8bc9bfcfa978df3fa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664083"
---
# <a name="d3dxcreateeffectcompiler-function"></a><span data-ttu-id="b1cd5-103">Função D3DXCreateEffectCompiler</span><span class="sxs-lookup"><span data-stu-id="b1cd5-103">D3DXCreateEffectCompiler function</span></span>

<span data-ttu-id="b1cd5-104">Cria um compilador de efeito a partir de uma descrição de efeito ASCII.</span><span class="sxs-lookup"><span data-stu-id="b1cd5-104">Creates an effect compiler from an ASCII effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1cd5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b1cd5-105">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectCompiler(
  _In_        LPCSTR               pSrcData,
  _In_        UINT                 SrcDataLen,
  _In_  const D3DXMACRO            *pDefines,
  _In_        LPD3DXINCLUDE        pInclude,
  _In_        DWORD                Flags,
  _Out_       LPD3DXEFFECTCOMPILER *ppEffectCompiler,
  _Out_       LPD3DXBUFFER         *ppParseErrors
);
```



## <a name="parameters"></a><span data-ttu-id="b1cd5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b1cd5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1cd5-107">*pSrcData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b1cd5-107">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1cd5-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b1cd5-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b1cd5-109">Ponteiro para um buffer que contém uma descrição de efeito.</span><span class="sxs-lookup"><span data-stu-id="b1cd5-109">Pointer to a buffer containing an effect description.</span></span>

</dd> <dt>

<span data-ttu-id="b1cd5-110">*SrcDataLen* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b1cd5-110">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1cd5-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b1cd5-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b1cd5-112">Comprimento, em bytes, dos dados de efeito.</span><span class="sxs-lookup"><span data-stu-id="b1cd5-112">Length, in bytes, of the effect data.</span></span>

</dd> <dt>

<span data-ttu-id="b1cd5-113">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b1cd5-113">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1cd5-114">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="b1cd5-114">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="b1cd5-115">Uma matriz opcional com terminação **nula** de estruturas [**D3DXMACRO**](d3dxmacro.md) que descrevem as definições de pré-processador.</span><span class="sxs-lookup"><span data-stu-id="b1cd5-115">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="b1cd5-116">Esse valor pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="b1cd5-116">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b1cd5-117">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b1cd5-117">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1cd5-118">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="b1cd5-118">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="b1cd5-119">Ponteiro de interface opcional, [**ID3DXInclude**](id3dxinclude.md), a ser usado para manipulação de \# diretivas include.</span><span class="sxs-lookup"><span data-stu-id="b1cd5-119">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="b1cd5-120">Se esse valor for **NULL**, \# incluirá que será respeitado durante a compilação de um arquivo ou causará um erro quando compilado de um recurso ou memória.</span><span class="sxs-lookup"><span data-stu-id="b1cd5-120">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="b1cd5-121">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="b1cd5-121">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1cd5-122">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b1cd5-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b1cd5-123">Opções de compilação identificadas por vários sinalizadores (consulte [sinalizadores D3DXSHADER](d3dxshader-flags.md)).</span><span class="sxs-lookup"><span data-stu-id="b1cd5-123">Compile options identified by various flags (see [D3DXSHADER Flags](d3dxshader-flags.md)).</span></span> <span data-ttu-id="b1cd5-124">O compilador do Direct3D 10 HLSL agora é o padrão.</span><span class="sxs-lookup"><span data-stu-id="b1cd5-124">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="b1cd5-125">Confira [ferramenta de compilador de efeito](../direct3dtools/fxc.md) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="b1cd5-125">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="b1cd5-126">*ppEffectCompiler* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b1cd5-126">*ppEffectCompiler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1cd5-127">Tipo: **[ **LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span><span class="sxs-lookup"><span data-stu-id="b1cd5-127">Type: **[**LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span></span>

<span data-ttu-id="b1cd5-128">Endereço de um ponteiro para uma interface [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) que contém o compilador de efeito.</span><span class="sxs-lookup"><span data-stu-id="b1cd5-128">Address of a pointer to an [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) interface containing the effect compiler.</span></span>

</dd> <dt>

<span data-ttu-id="b1cd5-129">*ppParseErrors* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b1cd5-129">*ppParseErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1cd5-130">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="b1cd5-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="b1cd5-131">Endereço de um ponteiro para uma interface [**ID3DXBuffer**](id3dxbuffer.md) que contém as mensagens de erro ocorridas durante a compilação.</span><span class="sxs-lookup"><span data-stu-id="b1cd5-131">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface containing any error messages that occurred during compilation.</span></span> <span data-ttu-id="b1cd5-132">Esse parâmetro pode ser definido como **nulo** para ignorar mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="b1cd5-132">This parameter can be set to **NULL** to ignore error messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1cd5-133">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b1cd5-133">Return value</span></span>

<span data-ttu-id="b1cd5-134">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b1cd5-134">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b1cd5-135">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b1cd5-135">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b1cd5-136">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="b1cd5-136">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1cd5-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1cd5-137">Requirements</span></span>



| <span data-ttu-id="b1cd5-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1cd5-138">Requirement</span></span> | <span data-ttu-id="b1cd5-139">Valor</span><span class="sxs-lookup"><span data-stu-id="b1cd5-139">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1cd5-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b1cd5-140">Header</span></span><br/>  | <dl> <span data-ttu-id="b1cd5-141"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1cd5-141"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="b1cd5-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b1cd5-142">Library</span></span><br/> | <dl> <span data-ttu-id="b1cd5-143"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b1cd5-143"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b1cd5-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="b1cd5-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1cd5-145">Funções de efeito</span><span class="sxs-lookup"><span data-stu-id="b1cd5-145">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="b1cd5-146">**D3DXCreateEffectCompilerFromFile**</span><span class="sxs-lookup"><span data-stu-id="b1cd5-146">**D3DXCreateEffectCompilerFromFile**</span></span>](d3dxcreateeffectcompilerfromfile.md)
</dt> <dt>

[<span data-ttu-id="b1cd5-147">**D3DXCreateEffectCompilerFromResource**</span><span class="sxs-lookup"><span data-stu-id="b1cd5-147">**D3DXCreateEffectCompilerFromResource**</span></span>](d3dxcreateeffectcompilerfromresource.md)
</dt> </dl>

 

 
