---
description: Função D3DXCreateEffectFromResource – crie um efeito de uma descrição de efeito ASCII ou binário.
ms.assetid: 8385512c-e93d-4c07-b353-87717eb58bcd
title: Função D3DXCreateEffectFromResource (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectFromResource
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f2a84d2da1f3ca88a117c0150e7b27485838c300
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107684"
---
# <a name="d3dxcreateeffectfromresource-function"></a><span data-ttu-id="7661e-103">Função D3DXCreateEffectFromResource</span><span class="sxs-lookup"><span data-stu-id="7661e-103">D3DXCreateEffectFromResource function</span></span>

<span data-ttu-id="7661e-104">Crie um efeito a partir de uma descrição de efeito ASCII ou binário.</span><span class="sxs-lookup"><span data-stu-id="7661e-104">Create an effect from an ASCII or binary effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="7661e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7661e-105">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectFromResource(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        HMODULE           hSrcModule,
  _In_        LPCTSTR           pSrcResource,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a><span data-ttu-id="7661e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7661e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7661e-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7661e-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7661e-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="7661e-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="7661e-109">Ponteiro para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7661e-109">Pointer to the device.</span></span>

</dd> <dt>

<span data-ttu-id="7661e-110">*hSrcModule* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7661e-110">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7661e-111">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7661e-111">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7661e-112">Identificador para um módulo que contém a descrição do efeito.</span><span class="sxs-lookup"><span data-stu-id="7661e-112">Handle to a module containing the effect description.</span></span> <span data-ttu-id="7661e-113">Se esse parâmetro for **NULL**, o módulo atual será usado.</span><span class="sxs-lookup"><span data-stu-id="7661e-113">If this parameter is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="7661e-114">*pSrcResource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7661e-114">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7661e-115">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7661e-115">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7661e-116">Ponteiro para o recurso.</span><span class="sxs-lookup"><span data-stu-id="7661e-116">Pointer to the resource.</span></span> <span data-ttu-id="7661e-117">Esse parâmetro dá suporte a cadeias de caracteres Unicode e ANSI.</span><span class="sxs-lookup"><span data-stu-id="7661e-117">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="7661e-118">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="7661e-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="7661e-119">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7661e-119">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7661e-120">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="7661e-120">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="7661e-121">Uma matriz opcional com terminação **nula** de estruturas [**D3DXMACRO**](d3dxmacro.md) que descrevem as definições de pré-processador.</span><span class="sxs-lookup"><span data-stu-id="7661e-121">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="7661e-122">Esse valor pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="7661e-122">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7661e-123">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7661e-123">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7661e-124">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="7661e-124">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="7661e-125">Ponteiro de interface opcional, [**ID3DXInclude**](id3dxinclude.md), a ser usado para manipulação de \# diretivas include.</span><span class="sxs-lookup"><span data-stu-id="7661e-125">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="7661e-126">Se esse valor for **NULL**, \# incluirá que será respeitado durante a compilação de um arquivo ou causará um erro quando compilado de um recurso ou memória.</span><span class="sxs-lookup"><span data-stu-id="7661e-126">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="7661e-127">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="7661e-127">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7661e-128">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7661e-128">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7661e-129">Se *hSrcModule* contiver um efeito de texto, os sinalizadores poderão ser uma combinação de sinalizadores [D3DXSHADER](d3dxshader-flags.md) e sinalizadores [D3DXFX](d3dxfx.md) ; caso contrário, *hSrcModule* conterá um efeito binário e os únicos sinalizadores honrados serão sinalizadores D3DXFX.</span><span class="sxs-lookup"><span data-stu-id="7661e-129">If *hSrcModule* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *hSrcModule* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="7661e-130">O compilador do Direct3D 10 HLSL agora é o padrão.</span><span class="sxs-lookup"><span data-stu-id="7661e-130">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="7661e-131">Confira [ferramenta de compilador de efeito](../direct3dtools/fxc.md) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="7661e-131">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="7661e-132">*pPool* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7661e-132">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7661e-133">Tipo: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="7661e-133">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="7661e-134">Ponteiro para um objeto [**ID3DXEffectPool**](id3dxeffectpool.md) a ser usado para parâmetros compartilhados.</span><span class="sxs-lookup"><span data-stu-id="7661e-134">Pointer to a [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="7661e-135">Se esse valor for **NULL**, nenhum parâmetro será compartilhado.</span><span class="sxs-lookup"><span data-stu-id="7661e-135">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="7661e-136">*ppEffect* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7661e-136">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7661e-137">Tipo: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="7661e-137">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="7661e-138">Retorna um buffer que contém o efeito compilado.</span><span class="sxs-lookup"><span data-stu-id="7661e-138">Returns a buffer containing the compiled effect.</span></span>

</dd> <dt>

<span data-ttu-id="7661e-139">*ppCompilationErrors* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7661e-139">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7661e-140">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="7661e-140">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="7661e-141">Retorna um buffer que contém uma lista de erros de compilação.</span><span class="sxs-lookup"><span data-stu-id="7661e-141">Returns a buffer containing a listing of compile errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7661e-142">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="7661e-142">Return value</span></span>

<span data-ttu-id="7661e-143">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7661e-143">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7661e-144">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7661e-144">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7661e-145">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="7661e-145">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="7661e-146">Comentários</span><span class="sxs-lookup"><span data-stu-id="7661e-146">Remarks</span></span>

<span data-ttu-id="7661e-147">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="7661e-147">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="7661e-148">Caso contrário, o tipo de dados LPCTSTR será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="7661e-148">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="7661e-149">A configuração do compilador também determina a versão da função.</span><span class="sxs-lookup"><span data-stu-id="7661e-149">The compiler setting also determines the function version.</span></span> <span data-ttu-id="7661e-150">Se o Unicode for definido, a chamada de função será resolvida como D3DXCreateEffectFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="7661e-150">If Unicode is defined, the function call resolves to D3DXCreateEffectFromResourceW.</span></span> <span data-ttu-id="7661e-151">Caso contrário, a chamada de função é resolvida como D3DXCreateEffectFromResourceA porque as cadeias de caracteres ANSI estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="7661e-151">Otherwise, the function call resolves to D3DXCreateEffectFromResourceA because ANSI strings are being used.</span></span>

<span data-ttu-id="7661e-152">D3DXCreateEffectFromResource carrega dados de um recurso do tipo RT \_ RCDATA.</span><span class="sxs-lookup"><span data-stu-id="7661e-152">D3DXCreateEffectFromResource loads data from a resource of type RT\_RCDATA.</span></span> <span data-ttu-id="7661e-153">Consulte o MSDN para obter mais informações sobre os recursos do Windows.</span><span class="sxs-lookup"><span data-stu-id="7661e-153">See MSDN for more information about Windows resources.</span></span>

## <a name="requirements"></a><span data-ttu-id="7661e-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7661e-154">Requirements</span></span>



| <span data-ttu-id="7661e-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="7661e-155">Requirement</span></span> | <span data-ttu-id="7661e-156">Valor</span><span class="sxs-lookup"><span data-stu-id="7661e-156">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7661e-157">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7661e-157">Header</span></span><br/>  | <dl> <span data-ttu-id="7661e-158"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="7661e-158"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="7661e-159">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7661e-159">Library</span></span><br/> | <dl> <span data-ttu-id="7661e-160"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7661e-160"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7661e-161">Consulte também</span><span class="sxs-lookup"><span data-stu-id="7661e-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7661e-162">Funções de efeito</span><span class="sxs-lookup"><span data-stu-id="7661e-162">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="7661e-163">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="7661e-163">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="7661e-164">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="7661e-164">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
