---
description: Função D3DXCreateEffectCompiler – cria um compilador de efeito a partir de uma descrição de efeito ASCII.
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
ms.openlocfilehash: 38ab58ed15609d468d25f4406353448e4fd6adb4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115764"
---
# <a name="d3dxcreateeffectcompiler-function"></a><span data-ttu-id="c88c1-103">Função D3DXCreateEffectCompiler</span><span class="sxs-lookup"><span data-stu-id="c88c1-103">D3DXCreateEffectCompiler function</span></span>

<span data-ttu-id="c88c1-104">Cria um compilador de efeito a partir de uma descrição de efeito ASCII.</span><span class="sxs-lookup"><span data-stu-id="c88c1-104">Creates an effect compiler from an ASCII effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="c88c1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c88c1-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="c88c1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c88c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c88c1-107">*pSrcData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c88c1-107">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c88c1-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c88c1-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c88c1-109">Ponteiro para um buffer que contém uma descrição de efeito.</span><span class="sxs-lookup"><span data-stu-id="c88c1-109">Pointer to a buffer containing an effect description.</span></span>

</dd> <dt>

<span data-ttu-id="c88c1-110">*SrcDataLen* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c88c1-110">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c88c1-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c88c1-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c88c1-112">Comprimento, em bytes, dos dados de efeito.</span><span class="sxs-lookup"><span data-stu-id="c88c1-112">Length, in bytes, of the effect data.</span></span>

</dd> <dt>

<span data-ttu-id="c88c1-113">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c88c1-113">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c88c1-114">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="c88c1-114">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="c88c1-115">Uma matriz opcional com terminação **nula** de estruturas [**D3DXMACRO**](d3dxmacro.md) que descrevem as definições de pré-processador.</span><span class="sxs-lookup"><span data-stu-id="c88c1-115">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="c88c1-116">Esse valor pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="c88c1-116">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c88c1-117">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c88c1-117">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c88c1-118">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="c88c1-118">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="c88c1-119">Ponteiro de interface opcional, [**ID3DXInclude**](id3dxinclude.md), a ser usado para manipulação de \# diretivas include.</span><span class="sxs-lookup"><span data-stu-id="c88c1-119">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="c88c1-120">Se esse valor for **NULL**, \# incluirá que será respeitado durante a compilação de um arquivo ou causará um erro quando compilado de um recurso ou memória.</span><span class="sxs-lookup"><span data-stu-id="c88c1-120">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="c88c1-121">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="c88c1-121">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c88c1-122">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c88c1-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c88c1-123">Opções de compilação identificadas por vários sinalizadores (consulte [sinalizadores D3DXSHADER](d3dxshader-flags.md)).</span><span class="sxs-lookup"><span data-stu-id="c88c1-123">Compile options identified by various flags (see [D3DXSHADER Flags](d3dxshader-flags.md)).</span></span> <span data-ttu-id="c88c1-124">O compilador do Direct3D 10 HLSL agora é o padrão.</span><span class="sxs-lookup"><span data-stu-id="c88c1-124">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="c88c1-125">Confira [ferramenta de compilador de efeito](../direct3dtools/fxc.md) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="c88c1-125">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="c88c1-126">*ppEffectCompiler* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c88c1-126">*ppEffectCompiler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c88c1-127">Tipo: **[ **LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span><span class="sxs-lookup"><span data-stu-id="c88c1-127">Type: **[**LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span></span>

<span data-ttu-id="c88c1-128">Endereço de um ponteiro para uma interface [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) que contém o compilador de efeito.</span><span class="sxs-lookup"><span data-stu-id="c88c1-128">Address of a pointer to an [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) interface containing the effect compiler.</span></span>

</dd> <dt>

<span data-ttu-id="c88c1-129">*ppParseErrors* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c88c1-129">*ppParseErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c88c1-130">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="c88c1-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="c88c1-131">Endereço de um ponteiro para uma interface [**ID3DXBuffer**](id3dxbuffer.md) que contém as mensagens de erro ocorridas durante a compilação.</span><span class="sxs-lookup"><span data-stu-id="c88c1-131">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface containing any error messages that occurred during compilation.</span></span> <span data-ttu-id="c88c1-132">Esse parâmetro pode ser definido como **nulo** para ignorar mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="c88c1-132">This parameter can be set to **NULL** to ignore error messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c88c1-133">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c88c1-133">Return value</span></span>

<span data-ttu-id="c88c1-134">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c88c1-134">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c88c1-135">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c88c1-135">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c88c1-136">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="c88c1-136">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="c88c1-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c88c1-137">Requirements</span></span>



| <span data-ttu-id="c88c1-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="c88c1-138">Requirement</span></span> | <span data-ttu-id="c88c1-139">Valor</span><span class="sxs-lookup"><span data-stu-id="c88c1-139">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c88c1-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c88c1-140">Header</span></span><br/>  | <dl> <span data-ttu-id="c88c1-141"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c88c1-141"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="c88c1-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c88c1-142">Library</span></span><br/> | <dl> <span data-ttu-id="c88c1-143"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c88c1-143"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c88c1-144">Consulte também</span><span class="sxs-lookup"><span data-stu-id="c88c1-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c88c1-145">Funções de efeito</span><span class="sxs-lookup"><span data-stu-id="c88c1-145">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="c88c1-146">**D3DXCreateEffectCompilerFromFile**</span><span class="sxs-lookup"><span data-stu-id="c88c1-146">**D3DXCreateEffectCompilerFromFile**</span></span>](d3dxcreateeffectcompilerfromfile.md)
</dt> <dt>

[<span data-ttu-id="c88c1-147">**D3DXCreateEffectCompilerFromResource**</span><span class="sxs-lookup"><span data-stu-id="c88c1-147">**D3DXCreateEffectCompilerFromResource**</span></span>](d3dxcreateeffectcompilerfromresource.md)
</dt> </dl>

 

 
