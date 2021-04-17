---
description: Cria um efeito a partir de uma descrição de efeito ASCII ou binário. Essa função é uma versão estendida do D3DXCreateEffect que permite que um aplicativo controle quais parâmetros são ignorados pelo sistema de efeitos.
ms.assetid: b08f727e-6061-4e78-8243-08c4ccab342d
title: Função D3DXCreateEffectEx (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectEx
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 979b09f852e692b4c25414607f79cd8792342755
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105766550"
---
# <a name="d3dxcreateeffectex-function"></a><span data-ttu-id="ce739-104">Função D3DXCreateEffectEx</span><span class="sxs-lookup"><span data-stu-id="ce739-104">D3DXCreateEffectEx function</span></span>

<span data-ttu-id="ce739-105">Cria um efeito a partir de uma descrição de efeito ASCII ou binário.</span><span class="sxs-lookup"><span data-stu-id="ce739-105">Creates an effect from an ASCII or binary effect description.</span></span> <span data-ttu-id="ce739-106">Essa função é uma versão estendida do [**D3DXCreateEffect**](d3dxcreateeffect.md) que permite que um aplicativo controle quais parâmetros são ignorados pelo sistema de efeitos.</span><span class="sxs-lookup"><span data-stu-id="ce739-106">This function is an extended version of [**D3DXCreateEffect**](d3dxcreateeffect.md) that allows an application to control which parameters are ignored by the effects system.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce739-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ce739-107">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectEx(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        LPCVOID           pSrcData,
  _In_        UINT              SrcDataLen,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        LPCSTR            pSkipConstants,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a><span data-ttu-id="ce739-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce739-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce739-109">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ce739-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce739-110">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="ce739-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="ce739-111">Ponteiro para o dispositivo que criará o efeito.</span><span class="sxs-lookup"><span data-stu-id="ce739-111">Pointer to the device that will create the effect.</span></span> <span data-ttu-id="ce739-112">Consulte [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="ce739-112">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> <dt>

<span data-ttu-id="ce739-113">*pSrcData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ce739-113">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce739-114">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ce739-114">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ce739-115">Ponteiro para um buffer que contém uma descrição de efeito.</span><span class="sxs-lookup"><span data-stu-id="ce739-115">Pointer to a buffer containing an effect description.</span></span>

</dd> <dt>

<span data-ttu-id="ce739-116">*SrcDataLen* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ce739-116">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce739-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ce739-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ce739-118">Comprimento dos dados de efeito, em bytes.</span><span class="sxs-lookup"><span data-stu-id="ce739-118">Length of the effect data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ce739-119">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ce739-119">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce739-120">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="ce739-120">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="ce739-121">Uma matriz opcional com terminação **nula** de estruturas [**D3DXMACRO**](d3dxmacro.md) que descrevem as definições de pré-processador.</span><span class="sxs-lookup"><span data-stu-id="ce739-121">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="ce739-122">Esse valor pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="ce739-122">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ce739-123">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ce739-123">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce739-124">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="ce739-124">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="ce739-125">Ponteiro de interface opcional, [**ID3DXInclude**](id3dxinclude.md), a ser usado para manipulação de \# diretivas include.</span><span class="sxs-lookup"><span data-stu-id="ce739-125">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="ce739-126">Se esse valor for **NULL**, \# incluirá que será respeitado durante a compilação de um arquivo ou causará um erro quando compilado de um recurso ou memória.</span><span class="sxs-lookup"><span data-stu-id="ce739-126">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="ce739-127">*pSkipConstants* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ce739-127">*pSkipConstants* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce739-128">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ce739-128">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ce739-129">Uma cadeia de parâmetros de efeito que será ignorada pelo sistema de efeito.</span><span class="sxs-lookup"><span data-stu-id="ce739-129">A string of effect parameters that will be ignored by the effect system.</span></span> <span data-ttu-id="ce739-130">A cadeia de caracteres deve ser terminada em **nulo** e precisa conter o nome de cada constante gerenciada por aplicativo, separada por um ponto-e-vírgula.</span><span class="sxs-lookup"><span data-stu-id="ce739-130">The string must be **NULL** terminated, and needs to contain the name of each application-managed constant separated by a semicolon.</span></span>

</dd> <dt>

<span data-ttu-id="ce739-131">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="ce739-131">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce739-132">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ce739-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ce739-133">Se *pSrcData* contiver um efeito de texto, os sinalizadores poderão ser uma combinação de sinalizadores [D3DXSHADER](d3dxshader-flags.md) e sinalizadores [D3DXFX](d3dxfx.md) ; caso contrário, *pSrcData* conterá um efeito binário e os únicos sinalizadores honrados serão sinalizadores D3DXFX.</span><span class="sxs-lookup"><span data-stu-id="ce739-133">If *pSrcData* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *pSrcData* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="ce739-134">O compilador do Direct3D 10 HLSL agora é o padrão.</span><span class="sxs-lookup"><span data-stu-id="ce739-134">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="ce739-135">Confira [ferramenta de compilador de efeito](../direct3dtools/fxc.md) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="ce739-135">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="ce739-136">*pPool* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ce739-136">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce739-137">Tipo: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="ce739-137">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="ce739-138">Ponteiro para um objeto [**ID3DXEffectPool**](id3dxeffectpool.md) a ser usado para parâmetros compartilhados.</span><span class="sxs-lookup"><span data-stu-id="ce739-138">Pointer to an [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="ce739-139">Se esse valor for **NULL**, nenhum parâmetro será compartilhado.</span><span class="sxs-lookup"><span data-stu-id="ce739-139">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="ce739-140">*ppEffect* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ce739-140">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce739-141">Tipo: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="ce739-141">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="ce739-142">Retorna um ponteiro para uma interface [**ID3DXEffect**](id3dxeffect.md) .</span><span class="sxs-lookup"><span data-stu-id="ce739-142">Returns a pointer to an [**ID3DXEffect**](id3dxeffect.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="ce739-143">*ppCompilationErrors* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ce739-143">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce739-144">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="ce739-144">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="ce739-145">Retorna um buffer que contém uma lista de erros de compilação.</span><span class="sxs-lookup"><span data-stu-id="ce739-145">Returns a buffer containing a list of compile errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce739-146">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ce739-146">Return value</span></span>

<span data-ttu-id="ce739-147">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ce739-147">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ce739-148">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ce739-148">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ce739-149">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="ce739-149">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce739-150">Comentários</span><span class="sxs-lookup"><span data-stu-id="ce739-150">Remarks</span></span>

<span data-ttu-id="ce739-151">Essa função é uma versão estendida do [**D3DXCreateEffect**](d3dxcreateeffect.md) que permite que um aplicativo especifique quais constantes de efeito serão gerenciadas pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ce739-151">This function is an extended version of [**D3DXCreateEffect**](d3dxcreateeffect.md) that allows an application to specify which effect constants will be managed by the application.</span></span> <span data-ttu-id="ce739-152">Uma constante que é gerenciada pelo aplicativo é ignorada pelo sistema de efeitos.</span><span class="sxs-lookup"><span data-stu-id="ce739-152">A constant that is managed by the application is ignored by the effects system.</span></span> <span data-ttu-id="ce739-153">Ou seja, o aplicativo é responsável por inicializar a constante, bem como salvar e restaurar seu estado sempre que apropriado.</span><span class="sxs-lookup"><span data-stu-id="ce739-153">That is, the application is responsible for initializing the constant as well as saving and restoring its state whenever appropriate.</span></span>

<span data-ttu-id="ce739-154">Essa função verifica cada constante em pSkipConstants para ver que:</span><span class="sxs-lookup"><span data-stu-id="ce739-154">This function checks each constant in pSkipConstants to see that:</span></span>

-   <span data-ttu-id="ce739-155">Ele está associado a um registro constante.</span><span class="sxs-lookup"><span data-stu-id="ce739-155">It is bound to a constant register.</span></span>
-   <span data-ttu-id="ce739-156">Ele só é usado no código do sombreador HLSL.</span><span class="sxs-lookup"><span data-stu-id="ce739-156">It is only used in HLSL shader code.</span></span>

<span data-ttu-id="ce739-157">Se uma constante for nomeada na cadeia de caracteres que não está presente no efeito, ela será ignorada.</span><span class="sxs-lookup"><span data-stu-id="ce739-157">If a constant is named in the string that is not present in the effect, it is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce739-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce739-158">Requirements</span></span>



| <span data-ttu-id="ce739-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce739-159">Requirement</span></span> | <span data-ttu-id="ce739-160">Valor</span><span class="sxs-lookup"><span data-stu-id="ce739-160">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce739-161">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ce739-161">Header</span></span><br/>  | <dl> <span data-ttu-id="ce739-162"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce739-162"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="ce739-163">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ce739-163">Library</span></span><br/> | <dl> <span data-ttu-id="ce739-164"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce739-164"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ce739-165">Confira também</span><span class="sxs-lookup"><span data-stu-id="ce739-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce739-166">Funções de efeito</span><span class="sxs-lookup"><span data-stu-id="ce739-166">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="ce739-167">**D3DXCreateEffectFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="ce739-167">**D3DXCreateEffectFromFileEx**</span></span>](d3dxcreateeffectfromfileex.md)
</dt> <dt>

[<span data-ttu-id="ce739-168">**D3DXCreateEffectFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="ce739-168">**D3DXCreateEffectFromResourceEx**</span></span>](d3dxcreateeffectfromresourceex.md)
</dt> </dl>

 

 
