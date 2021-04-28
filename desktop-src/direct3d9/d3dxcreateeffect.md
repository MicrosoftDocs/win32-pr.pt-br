---
description: Função D3DXCreateEffect – crie um efeito de uma descrição de efeito ASCII ou binário.
ms.assetid: 1cbd91f2-3cda-4770-a3c5-b1e6702628d1
title: Função D3DXCreateEffect (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffect
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6821375dfc672d4937c335cf85dab12ba31b726c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115774"
---
# <a name="d3dxcreateeffect-function"></a><span data-ttu-id="6eb0e-103">Função D3DXCreateEffect</span><span class="sxs-lookup"><span data-stu-id="6eb0e-103">D3DXCreateEffect function</span></span>

<span data-ttu-id="6eb0e-104">Crie um efeito a partir de uma descrição de efeito ASCII ou binário.</span><span class="sxs-lookup"><span data-stu-id="6eb0e-104">Create an effect from an ASCII or binary effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="6eb0e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6eb0e-105">Syntax</span></span>


```C++
HRESULT D3DXCreateEffect(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        LPCVOID           pSrcData,
  _In_        UINT              SrcDataLen,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a><span data-ttu-id="6eb0e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6eb0e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6eb0e-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6eb0e-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6eb0e-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="6eb0e-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="6eb0e-109">Ponteiro para o dispositivo que criará o efeito.</span><span class="sxs-lookup"><span data-stu-id="6eb0e-109">Pointer to the device that will create the effect.</span></span> <span data-ttu-id="6eb0e-110">Consulte [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="6eb0e-110">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> <dt>

<span data-ttu-id="6eb0e-111">*pSrcData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6eb0e-111">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6eb0e-112">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6eb0e-112">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6eb0e-113">Ponteiro para um buffer que contém uma descrição de efeito.</span><span class="sxs-lookup"><span data-stu-id="6eb0e-113">Pointer to a buffer containing an effect description.</span></span>

</dd> <dt>

<span data-ttu-id="6eb0e-114">*SrcDataLen* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6eb0e-114">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6eb0e-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6eb0e-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6eb0e-116">Comprimento dos dados de efeito, em bytes.</span><span class="sxs-lookup"><span data-stu-id="6eb0e-116">Length of the effect data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="6eb0e-117">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6eb0e-117">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6eb0e-118">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="6eb0e-118">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="6eb0e-119">Uma matriz opcional com terminação **nula** de estruturas [**D3DXMACRO**](d3dxmacro.md) que descrevem as definições de pré-processador.</span><span class="sxs-lookup"><span data-stu-id="6eb0e-119">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="6eb0e-120">Esse valor pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="6eb0e-120">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6eb0e-121">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6eb0e-121">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6eb0e-122">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="6eb0e-122">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="6eb0e-123">Ponteiro de interface opcional, [**ID3DXInclude**](id3dxinclude.md), a ser usado para manipulação de \# diretivas include.</span><span class="sxs-lookup"><span data-stu-id="6eb0e-123">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="6eb0e-124">Se esse valor for **NULL**, \# incluirá que será respeitado durante a compilação de um arquivo ou causará um erro quando compilado de um recurso ou memória.</span><span class="sxs-lookup"><span data-stu-id="6eb0e-124">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="6eb0e-125">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="6eb0e-125">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6eb0e-126">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6eb0e-126">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6eb0e-127">Se *pSrcData* contiver um efeito de texto, os sinalizadores poderão ser uma combinação de sinalizadores [D3DXSHADER](d3dxshader-flags.md) e sinalizadores [D3DXFX](d3dxfx.md) ; caso contrário, *pSrcData* conterá um efeito binário e os únicos sinalizadores honrados serão sinalizadores D3DXFX.</span><span class="sxs-lookup"><span data-stu-id="6eb0e-127">If *pSrcData* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *pSrcData* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="6eb0e-128">O compilador do Direct3D 10 HLSL agora é o padrão.</span><span class="sxs-lookup"><span data-stu-id="6eb0e-128">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="6eb0e-129">Confira [ferramenta de compilador de efeito](../direct3dtools/fxc.md) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="6eb0e-129">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="6eb0e-130">*pPool* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6eb0e-130">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6eb0e-131">Tipo: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="6eb0e-131">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="6eb0e-132">Ponteiro para um objeto [**ID3DXEffectPool**](id3dxeffectpool.md) a ser usado para parâmetros compartilhados.</span><span class="sxs-lookup"><span data-stu-id="6eb0e-132">Pointer to a [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="6eb0e-133">Se esse valor for **NULL**, nenhum parâmetro será compartilhado.</span><span class="sxs-lookup"><span data-stu-id="6eb0e-133">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="6eb0e-134">*ppEffect* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6eb0e-134">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6eb0e-135">Tipo: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="6eb0e-135">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="6eb0e-136">Retorna um ponteiro para uma interface [**ID3DXEffect**](id3dxeffect.md) .</span><span class="sxs-lookup"><span data-stu-id="6eb0e-136">Returns a pointer to an [**ID3DXEffect**](id3dxeffect.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="6eb0e-137">*ppCompilationErrors* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6eb0e-137">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6eb0e-138">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="6eb0e-138">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="6eb0e-139">Retorna um buffer que contém uma lista de erros de compilação.</span><span class="sxs-lookup"><span data-stu-id="6eb0e-139">Returns a buffer containing a listing of compile errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6eb0e-140">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="6eb0e-140">Return value</span></span>

<span data-ttu-id="6eb0e-141">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6eb0e-141">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6eb0e-142">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6eb0e-142">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6eb0e-143">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="6eb0e-143">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="6eb0e-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6eb0e-144">Requirements</span></span>



| <span data-ttu-id="6eb0e-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="6eb0e-145">Requirement</span></span> | <span data-ttu-id="6eb0e-146">Valor</span><span class="sxs-lookup"><span data-stu-id="6eb0e-146">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6eb0e-147">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6eb0e-147">Header</span></span><br/>  | <dl> <span data-ttu-id="6eb0e-148"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="6eb0e-148"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="6eb0e-149">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6eb0e-149">Library</span></span><br/> | <dl> <span data-ttu-id="6eb0e-150"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6eb0e-150"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="6eb0e-151">Consulte também</span><span class="sxs-lookup"><span data-stu-id="6eb0e-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6eb0e-152">Funções de efeito</span><span class="sxs-lookup"><span data-stu-id="6eb0e-152">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="6eb0e-153">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="6eb0e-153">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="6eb0e-154">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="6eb0e-154">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
