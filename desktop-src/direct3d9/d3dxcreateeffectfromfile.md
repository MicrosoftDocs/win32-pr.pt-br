---
description: Função D3DXCreateEffectFromFile – crie um efeito de uma descrição de efeito ASCII ou binário.
ms.assetid: b5868ba3-0869-46f7-804f-3103358a3ef5
title: Função D3DXCreateEffectFromFile (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectFromFile
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d8b2afdd1e8008bc8e03efa670e5a4b37b6dc9f8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094314"
---
# <a name="d3dxcreateeffectfromfile-function"></a><span data-ttu-id="93ff1-103">Função D3DXCreateEffectFromFile</span><span class="sxs-lookup"><span data-stu-id="93ff1-103">D3DXCreateEffectFromFile function</span></span>

<span data-ttu-id="93ff1-104">Crie um efeito a partir de uma descrição de efeito ASCII ou binário.</span><span class="sxs-lookup"><span data-stu-id="93ff1-104">Create an effect from an ASCII or binary effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="93ff1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="93ff1-105">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectFromFile(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        LPCTSTR           pSrcFile,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a><span data-ttu-id="93ff1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="93ff1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93ff1-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="93ff1-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93ff1-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="93ff1-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="93ff1-109">Ponteiro para o dispositivo que criará o efeito.</span><span class="sxs-lookup"><span data-stu-id="93ff1-109">Pointer to the device that will create the effect.</span></span> <span data-ttu-id="93ff1-110">Consulte [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="93ff1-110">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-111">*pSrcFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="93ff1-111">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93ff1-112">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="93ff1-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="93ff1-113">Ponteiro para o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="93ff1-113">Pointer to the filename.</span></span> <span data-ttu-id="93ff1-114">Esse parâmetro dá suporte a cadeias de caracteres Unicode e ANSI.</span><span class="sxs-lookup"><span data-stu-id="93ff1-114">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="93ff1-115">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="93ff1-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-116">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="93ff1-116">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93ff1-117">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="93ff1-117">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="93ff1-118">Matriz opcional terminada por nulo de definições de macro de pré-processador.</span><span class="sxs-lookup"><span data-stu-id="93ff1-118">Optional NULL-terminated array of preprocessor macro definitions.</span></span> <span data-ttu-id="93ff1-119">Consulte [**D3DXMACRO**](d3dxmacro.md).</span><span class="sxs-lookup"><span data-stu-id="93ff1-119">See [**D3DXMACRO**](d3dxmacro.md).</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-120">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="93ff1-120">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93ff1-121">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="93ff1-121">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="93ff1-122">Ponteiro de interface opcional, [**ID3DXInclude**](id3dxinclude.md), a ser usado para manipulação de \# diretivas include.</span><span class="sxs-lookup"><span data-stu-id="93ff1-122">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="93ff1-123">Se esse valor for **NULL**, \# incluirá que será respeitado durante a compilação de um arquivo ou causará um erro quando compilado de um recurso ou memória.</span><span class="sxs-lookup"><span data-stu-id="93ff1-123">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-124">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="93ff1-124">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93ff1-125">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="93ff1-125">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="93ff1-126">Se *pSrcFile* contiver um efeito de texto, os sinalizadores poderão ser uma combinação de sinalizadores [D3DXSHADER](d3dxshader-flags.md) e sinalizadores [D3DXFX](d3dxfx.md) ; caso contrário, *pSrcFile* conterá um efeito binário e os únicos sinalizadores honrados serão sinalizadores D3DXFX.</span><span class="sxs-lookup"><span data-stu-id="93ff1-126">If *pSrcFile* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *pSrcFile* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="93ff1-127">O compilador do Direct3D 10 HLSL agora é o padrão.</span><span class="sxs-lookup"><span data-stu-id="93ff1-127">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="93ff1-128">Confira [ferramenta de compilador de efeito](../direct3dtools/fxc.md) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="93ff1-128">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-129">*pPool* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="93ff1-129">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93ff1-130">Tipo: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="93ff1-130">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="93ff1-131">Ponteiro para um objeto [**ID3DXEffectPool**](id3dxeffectpool.md) a ser usado para parâmetros compartilhados.</span><span class="sxs-lookup"><span data-stu-id="93ff1-131">Pointer to a [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="93ff1-132">Se esse valor for **NULL**, nenhum parâmetro será compartilhado.</span><span class="sxs-lookup"><span data-stu-id="93ff1-132">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-133">*ppEffect* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="93ff1-133">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="93ff1-134">Tipo: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="93ff1-134">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="93ff1-135">Retorna um ponteiro para um buffer que contém o efeito compilado.</span><span class="sxs-lookup"><span data-stu-id="93ff1-135">Returns a pointer to a buffer containing the compiled effect.</span></span> <span data-ttu-id="93ff1-136">Consulte [**ID3DXEffect**](id3dxeffect.md).</span><span class="sxs-lookup"><span data-stu-id="93ff1-136">See [**ID3DXEffect**](id3dxeffect.md).</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-137">*ppCompilationErrors* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="93ff1-137">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="93ff1-138">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="93ff1-138">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="93ff1-139">Retorna um ponteiro para um buffer que contém uma lista de erros de compilação.</span><span class="sxs-lookup"><span data-stu-id="93ff1-139">Returns a pointer to a buffer containing a listing of compile errors.</span></span> <span data-ttu-id="93ff1-140">Consulte [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="93ff1-140">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93ff1-141">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="93ff1-141">Return value</span></span>

<span data-ttu-id="93ff1-142">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="93ff1-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="93ff1-143">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="93ff1-143">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="93ff1-144">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="93ff1-144">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="93ff1-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="93ff1-145">Remarks</span></span>

<span data-ttu-id="93ff1-146">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="93ff1-146">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="93ff1-147">Caso contrário, o tipo de dados LPCTSTR será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="93ff1-147">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="93ff1-148">A configuração do compilador também determina a versão da função.</span><span class="sxs-lookup"><span data-stu-id="93ff1-148">The compiler setting also determines the function version.</span></span> <span data-ttu-id="93ff1-149">Se o Unicode for definido, a chamada de função será resolvida como D3DXCreateEffectFromFileW.</span><span class="sxs-lookup"><span data-stu-id="93ff1-149">If Unicode is defined, the function call resolves to D3DXCreateEffectFromFileW.</span></span> <span data-ttu-id="93ff1-150">Caso contrário, a chamada de função é resolvida como D3DXCreateEffectFromFileA porque as cadeias de caracteres ANSI estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="93ff1-150">Otherwise, the function call resolves to D3DXCreateEffectFromFileA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="93ff1-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93ff1-151">Requirements</span></span>



| <span data-ttu-id="93ff1-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="93ff1-152">Requirement</span></span> | <span data-ttu-id="93ff1-153">Valor</span><span class="sxs-lookup"><span data-stu-id="93ff1-153">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="93ff1-154">parâmetro</span><span class="sxs-lookup"><span data-stu-id="93ff1-154">Header</span></span><br/>  | <dl> <span data-ttu-id="93ff1-155"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="93ff1-155"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="93ff1-156">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="93ff1-156">Library</span></span><br/> | <dl> <span data-ttu-id="93ff1-157"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="93ff1-157"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="93ff1-158">Consulte também</span><span class="sxs-lookup"><span data-stu-id="93ff1-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93ff1-159">Funções de efeito</span><span class="sxs-lookup"><span data-stu-id="93ff1-159">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="93ff1-160">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="93ff1-160">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="93ff1-161">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="93ff1-161">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
