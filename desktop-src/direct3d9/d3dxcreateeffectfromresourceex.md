---
description: Crie um efeito a partir de uma descrição de efeito ASCII ou binário. Esta é uma versão estendida do D3DXCreateEffectFromResource que permite que um aplicativo controle quais parâmetros são ignorados pelo sistema de efeitos.
ms.assetid: 5937bdb1-750a-41f8-a49d-3643427f3e3c
title: Função D3DXCreateEffectFromResourceEx (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectFromResourceEx
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d0ae7a0ee43f93019f3c4c1f6145b3d8aa0e4367
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105788623"
---
# <a name="d3dxcreateeffectfromresourceex-function"></a><span data-ttu-id="357b5-104">Função D3DXCreateEffectFromResourceEx</span><span class="sxs-lookup"><span data-stu-id="357b5-104">D3DXCreateEffectFromResourceEx function</span></span>

<span data-ttu-id="357b5-105">Crie um efeito a partir de uma descrição de efeito ASCII ou binário.</span><span class="sxs-lookup"><span data-stu-id="357b5-105">Create an effect from an ASCII or binary effect description.</span></span> <span data-ttu-id="357b5-106">Esta é uma versão estendida do [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md) que permite que um aplicativo controle quais parâmetros são ignorados pelo sistema de efeitos.</span><span class="sxs-lookup"><span data-stu-id="357b5-106">This is an extended version of [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md) that allows an application to control which parameters are ignored by the effects system.</span></span>

## <a name="syntax"></a><span data-ttu-id="357b5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="357b5-107">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectFromResourceEx(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        HMODULE           hSrcModule,
  _In_        LPCTSTR           pSrcResource,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        LPCSTR            pSkipConstants,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a><span data-ttu-id="357b5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="357b5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="357b5-109">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="357b5-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="357b5-110">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="357b5-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="357b5-111">Ponteiro para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="357b5-111">Pointer to the device.</span></span>

</dd> <dt>

<span data-ttu-id="357b5-112">*hSrcModule* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="357b5-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="357b5-113">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="357b5-113">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="357b5-114">Identificador para um módulo que contém a descrição do efeito.</span><span class="sxs-lookup"><span data-stu-id="357b5-114">Handle to a module containing the effect description.</span></span> <span data-ttu-id="357b5-115">Se esse parâmetro for **NULL**, o módulo atual será usado.</span><span class="sxs-lookup"><span data-stu-id="357b5-115">If this parameter is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="357b5-116">*pSrcResource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="357b5-116">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="357b5-117">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="357b5-117">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="357b5-118">Ponteiro para o recurso.</span><span class="sxs-lookup"><span data-stu-id="357b5-118">Pointer to the resource.</span></span> <span data-ttu-id="357b5-119">Esse parâmetro dá suporte a cadeias de caracteres Unicode e ANSI.</span><span class="sxs-lookup"><span data-stu-id="357b5-119">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="357b5-120">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="357b5-120">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="357b5-121">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="357b5-121">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="357b5-122">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="357b5-122">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="357b5-123">Uma matriz opcional com terminação **nula** de estruturas [**D3DXMACRO**](d3dxmacro.md) que descrevem as definições de pré-processador.</span><span class="sxs-lookup"><span data-stu-id="357b5-123">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="357b5-124">Esse valor pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="357b5-124">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="357b5-125">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="357b5-125">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="357b5-126">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="357b5-126">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="357b5-127">Ponteiro de interface opcional, [**ID3DXInclude**](id3dxinclude.md), a ser usado para manipulação de \# diretivas include.</span><span class="sxs-lookup"><span data-stu-id="357b5-127">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="357b5-128">Se esse valor for **NULL**, \# incluirá que será respeitado durante a compilação de um arquivo ou causará um erro quando compilado de um recurso ou memória.</span><span class="sxs-lookup"><span data-stu-id="357b5-128">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="357b5-129">*pSkipConstants* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="357b5-129">*pSkipConstants* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="357b5-130">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="357b5-130">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="357b5-131">Uma cadeia de parâmetros de efeito que será ignorada pelo sistema de efeito.</span><span class="sxs-lookup"><span data-stu-id="357b5-131">A string of effect parameters that will be ignored by the effect system.</span></span> <span data-ttu-id="357b5-132">A cadeia de caracteres deve ser terminada em **nulo** e precisa conter o nome de cada constante gerenciada por aplicativo, separada por um ponto-e-vírgula.</span><span class="sxs-lookup"><span data-stu-id="357b5-132">The string must be **NULL** terminated, and needs to contain the name of each application-managed constant separated by a semicolon.</span></span>

</dd> <dt>

<span data-ttu-id="357b5-133">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="357b5-133">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="357b5-134">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="357b5-134">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="357b5-135">Se *pSrcResource* contiver um efeito de texto, os sinalizadores poderão ser uma combinação de sinalizadores [D3DXSHADER](d3dxshader-flags.md) e sinalizadores [D3DXFX](d3dxfx.md) ; caso contrário, *pSrcResource* conterá um efeito binário e os únicos sinalizadores honrados serão sinalizadores D3DXFX.</span><span class="sxs-lookup"><span data-stu-id="357b5-135">If *pSrcResource* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *pSrcResource* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="357b5-136">O compilador do Direct3D 10 HLSL agora é o padrão.</span><span class="sxs-lookup"><span data-stu-id="357b5-136">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="357b5-137">Confira [ferramenta de compilador de efeito](../direct3dtools/fxc.md) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="357b5-137">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="357b5-138">*pPool* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="357b5-138">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="357b5-139">Tipo: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="357b5-139">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="357b5-140">Ponteiro para um objeto [**ID3DXEffectPool**](id3dxeffectpool.md) a ser usado para parâmetros compartilhados.</span><span class="sxs-lookup"><span data-stu-id="357b5-140">Pointer to an [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="357b5-141">Se esse valor for **NULL**, nenhum parâmetro será compartilhado.</span><span class="sxs-lookup"><span data-stu-id="357b5-141">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="357b5-142">*ppEffect* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="357b5-142">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="357b5-143">Tipo: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="357b5-143">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="357b5-144">Retorna um buffer que contém o efeito compilado.</span><span class="sxs-lookup"><span data-stu-id="357b5-144">Returns a buffer containing the compiled effect.</span></span>

</dd> <dt>

<span data-ttu-id="357b5-145">*ppCompilationErrors* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="357b5-145">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="357b5-146">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="357b5-146">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="357b5-147">Retorna um buffer que contém uma lista de erros de compilação.</span><span class="sxs-lookup"><span data-stu-id="357b5-147">Returns a buffer containing a listing of compile errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="357b5-148">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="357b5-148">Return value</span></span>

<span data-ttu-id="357b5-149">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="357b5-149">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="357b5-150">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="357b5-150">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="357b5-151">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="357b5-151">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="357b5-152">Comentários</span><span class="sxs-lookup"><span data-stu-id="357b5-152">Remarks</span></span>

<span data-ttu-id="357b5-153">Essa função é uma versão estendida do [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md) que permite que um aplicativo especifique quais constantes de efeito serão gerenciadas pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="357b5-153">This function is an extended version of [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md) that allows an application to specify which effect constants will be managed by the application.</span></span> <span data-ttu-id="357b5-154">Uma constante que é gerenciada pelo aplicativo é ignorada pelo sistema de efeitos.</span><span class="sxs-lookup"><span data-stu-id="357b5-154">A constant that is managed by the application is ignored by the effects system.</span></span> <span data-ttu-id="357b5-155">Ou seja, o aplicativo é responsável por inicializar a constante, bem como salvar e restaurar seu estado sempre que apropriado.</span><span class="sxs-lookup"><span data-stu-id="357b5-155">That is, the application is responsible for initializing the constant as well as saving and restoring its state whenever appropriate.</span></span>

<span data-ttu-id="357b5-156">Essa função verifica cada constante em pSkipConstants para ver que:</span><span class="sxs-lookup"><span data-stu-id="357b5-156">This function checks each constant in pSkipConstants to see that:</span></span>

-   <span data-ttu-id="357b5-157">Ele está associado a um registro constante.</span><span class="sxs-lookup"><span data-stu-id="357b5-157">It is bound to a constant register.</span></span>
-   <span data-ttu-id="357b5-158">Ele só é usado no código do sombreador HLSL.</span><span class="sxs-lookup"><span data-stu-id="357b5-158">It is only used in HLSL shader code.</span></span>

<span data-ttu-id="357b5-159">Se uma constante for nomeada na cadeia de caracteres que não está presente no efeito, ela será ignorada.</span><span class="sxs-lookup"><span data-stu-id="357b5-159">If a constant is named in the string that is not present in the effect, it is ignored.</span></span>

<span data-ttu-id="357b5-160">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="357b5-160">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="357b5-161">Caso contrário, o tipo de dados LPCTSTR será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="357b5-161">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="357b5-162">A configuração do compilador também determina a versão da função.</span><span class="sxs-lookup"><span data-stu-id="357b5-162">The compiler setting also determines the function version.</span></span> <span data-ttu-id="357b5-163">Se o Unicode for definido, a chamada de função será resolvida como D3DXCreateEffectFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="357b5-163">If Unicode is defined, the function call resolves to D3DXCreateEffectFromResourceW.</span></span> <span data-ttu-id="357b5-164">Caso contrário, a chamada de função é resolvida como D3DXCreateEffectFromResourceA porque as cadeias de caracteres ANSI estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="357b5-164">Otherwise, the function call resolves to D3DXCreateEffectFromResourceA because ANSI strings are being used.</span></span>

<span data-ttu-id="357b5-165">D3DXCreateEffectFromResource carrega dados de um recurso do tipo RT \_ RCDATA.</span><span class="sxs-lookup"><span data-stu-id="357b5-165">D3DXCreateEffectFromResource loads data from a resource of type RT\_RCDATA.</span></span> <span data-ttu-id="357b5-166">Consulte o MSDN para obter mais informações sobre os recursos do Windows.</span><span class="sxs-lookup"><span data-stu-id="357b5-166">See MSDN for more information about Windows resources.</span></span>

## <a name="requirements"></a><span data-ttu-id="357b5-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="357b5-167">Requirements</span></span>



| <span data-ttu-id="357b5-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="357b5-168">Requirement</span></span> | <span data-ttu-id="357b5-169">Valor</span><span class="sxs-lookup"><span data-stu-id="357b5-169">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="357b5-170">parâmetro</span><span class="sxs-lookup"><span data-stu-id="357b5-170">Header</span></span><br/>  | <dl> <span data-ttu-id="357b5-171"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="357b5-171"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="357b5-172">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="357b5-172">Library</span></span><br/> | <dl> <span data-ttu-id="357b5-173"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="357b5-173"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="357b5-174">Confira também</span><span class="sxs-lookup"><span data-stu-id="357b5-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="357b5-175">Funções de efeito</span><span class="sxs-lookup"><span data-stu-id="357b5-175">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="357b5-176">**D3DXCreateEffectEx**</span><span class="sxs-lookup"><span data-stu-id="357b5-176">**D3DXCreateEffectEx**</span></span>](d3dxcreateeffectex.md)
</dt> <dt>

[<span data-ttu-id="357b5-177">**D3DXCreateEffectFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="357b5-177">**D3DXCreateEffectFromFileEx**</span></span>](d3dxcreateeffectfromfileex.md)
</dt> </dl>

 

 
