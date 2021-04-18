---
description: Crie um efeito a partir de uma descrição de efeito ASCII ou binário. Essa função é uma versão estendida do D3DXCreateEffectFromFile que permite que um aplicativo controle quais parâmetros são ignorados pelo sistema de efeitos.
ms.assetid: 963caa1e-bc1a-4d4b-bdb1-50b17d8b4132
title: Função D3DXCreateEffectFromFileEx (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectFromFileEx
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b3d97c5aa23dd0711cfb00585e5b8ba7d410fc02
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105769636"
---
# <a name="d3dxcreateeffectfromfileex-function"></a><span data-ttu-id="deba4-104">Função D3DXCreateEffectFromFileEx</span><span class="sxs-lookup"><span data-stu-id="deba4-104">D3DXCreateEffectFromFileEx function</span></span>

<span data-ttu-id="deba4-105">Crie um efeito a partir de uma descrição de efeito ASCII ou binário.</span><span class="sxs-lookup"><span data-stu-id="deba4-105">Create an effect from an ASCII or binary effect description.</span></span> <span data-ttu-id="deba4-106">Essa função é uma versão estendida do [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md) que permite que um aplicativo controle quais parâmetros são ignorados pelo sistema de efeitos.</span><span class="sxs-lookup"><span data-stu-id="deba4-106">This function is an extended version of [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md) that allows an application to control which parameters are ignored by the effects system.</span></span>

## <a name="syntax"></a><span data-ttu-id="deba4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="deba4-107">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectFromFileEx(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        LPCTSTR           pSrcFile,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        LPCSTR            pSkipConstants,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a><span data-ttu-id="deba4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="deba4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="deba4-109">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="deba4-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deba4-110">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="deba4-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="deba4-111">Ponteiro para o dispositivo que criará o efeito.</span><span class="sxs-lookup"><span data-stu-id="deba4-111">Pointer to the device that will create the effect.</span></span> <span data-ttu-id="deba4-112">Consulte [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="deba4-112">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> <dt>

<span data-ttu-id="deba4-113">*pSrcFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="deba4-113">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deba4-114">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="deba4-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="deba4-115">Ponteiro para o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="deba4-115">Pointer to the filename.</span></span> <span data-ttu-id="deba4-116">Esse parâmetro dá suporte a cadeias de caracteres Unicode e ANSI.</span><span class="sxs-lookup"><span data-stu-id="deba4-116">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="deba4-117">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="deba4-117">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="deba4-118">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="deba4-118">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deba4-119">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="deba4-119">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="deba4-120">Matriz opcional terminada por nulo de definições de macro de pré-processador.</span><span class="sxs-lookup"><span data-stu-id="deba4-120">Optional NULL-terminated array of preprocessor macro definitions.</span></span> <span data-ttu-id="deba4-121">Consulte [**D3DXMACRO**](d3dxmacro.md).</span><span class="sxs-lookup"><span data-stu-id="deba4-121">See [**D3DXMACRO**](d3dxmacro.md).</span></span>

</dd> <dt>

<span data-ttu-id="deba4-122">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="deba4-122">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deba4-123">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="deba4-123">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="deba4-124">Ponteiro de interface opcional, [**ID3DXInclude**](id3dxinclude.md), a ser usado para manipulação de \# diretivas include.</span><span class="sxs-lookup"><span data-stu-id="deba4-124">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="deba4-125">Se esse valor for **NULL**, \# incluirá que será respeitado durante a compilação de um arquivo ou causará um erro quando compilado de um recurso ou memória.</span><span class="sxs-lookup"><span data-stu-id="deba4-125">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="deba4-126">*pSkipConstants* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="deba4-126">*pSkipConstants* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deba4-127">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="deba4-127">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="deba4-128">Uma cadeia de parâmetros de efeito que será ignorada pelo sistema de efeito.</span><span class="sxs-lookup"><span data-stu-id="deba4-128">A string of effect parameters that will be ignored by the effect system.</span></span> <span data-ttu-id="deba4-129">A cadeia de caracteres deve ser terminada em **nulo** e precisa conter o nome de cada constante gerenciada por aplicativo, separada por um ponto-e-vírgula.</span><span class="sxs-lookup"><span data-stu-id="deba4-129">The string must be **NULL** terminated, and needs to contain the name of each application-managed constant separated by a semicolon.</span></span>

</dd> <dt>

<span data-ttu-id="deba4-130">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="deba4-130">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deba4-131">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="deba4-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="deba4-132">Se *pSrcFile* contiver um efeito de texto, os sinalizadores poderão ser uma combinação de sinalizadores [D3DXSHADER](d3dxshader-flags.md) e sinalizadores [D3DXFX](d3dxfx.md) ; caso contrário, *pSrcFile* conterá um efeito binário e os únicos sinalizadores honrados serão sinalizadores D3DXFX.</span><span class="sxs-lookup"><span data-stu-id="deba4-132">If *pSrcFile* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *pSrcFile* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="deba4-133">O compilador do Direct3D 10 HLSL agora é o padrão.</span><span class="sxs-lookup"><span data-stu-id="deba4-133">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="deba4-134">Confira [ferramenta de compilador de efeito](../direct3dtools/fxc.md) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="deba4-134">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="deba4-135">*pPool* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="deba4-135">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deba4-136">Tipo: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="deba4-136">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="deba4-137">Ponteiro para um objeto [**ID3DXEffectPool**](id3dxeffectpool.md) a ser usado para parâmetros compartilhados.</span><span class="sxs-lookup"><span data-stu-id="deba4-137">Pointer to a [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="deba4-138">Se esse valor for **NULL**, nenhum parâmetro será compartilhado.</span><span class="sxs-lookup"><span data-stu-id="deba4-138">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="deba4-139">*ppEffect* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="deba4-139">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="deba4-140">Tipo: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="deba4-140">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="deba4-141">Retorna um ponteiro para um buffer que contém o efeito compilado.</span><span class="sxs-lookup"><span data-stu-id="deba4-141">Returns a pointer to a buffer containing the compiled effect.</span></span> <span data-ttu-id="deba4-142">Consulte [**ID3DXEffect**](id3dxeffect.md).</span><span class="sxs-lookup"><span data-stu-id="deba4-142">See [**ID3DXEffect**](id3dxeffect.md).</span></span>

</dd> <dt>

<span data-ttu-id="deba4-143">*ppCompilationErrors* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="deba4-143">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="deba4-144">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="deba4-144">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="deba4-145">Retorna um ponteiro para um buffer que contém uma lista de erros de compilação.</span><span class="sxs-lookup"><span data-stu-id="deba4-145">Returns a pointer to a buffer containing a listing of compile errors.</span></span> <span data-ttu-id="deba4-146">Consulte [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="deba4-146">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="deba4-147">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="deba4-147">Return value</span></span>

<span data-ttu-id="deba4-148">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="deba4-148">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="deba4-149">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="deba4-149">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="deba4-150">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="deba4-150">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="deba4-151">Comentários</span><span class="sxs-lookup"><span data-stu-id="deba4-151">Remarks</span></span>

<span data-ttu-id="deba4-152">Essa função é uma versão estendida do [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md) que permite que um aplicativo especifique quais constantes de efeito serão gerenciadas pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="deba4-152">This function is an extended version of [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md) that allows an application to specify which effect constants will be managed by the application.</span></span> <span data-ttu-id="deba4-153">Uma constante que é gerenciada pelo aplicativo é ignorada pelo sistema de efeitos.</span><span class="sxs-lookup"><span data-stu-id="deba4-153">A constant that is managed by the application is ignored by the effects system.</span></span> <span data-ttu-id="deba4-154">Ou seja, o aplicativo é responsável por inicializar a constante, bem como salvar e restaurar seu estado sempre que apropriado.</span><span class="sxs-lookup"><span data-stu-id="deba4-154">That is, the application is responsible for initializing the constant as well as saving and restoring its state whenever appropriate.</span></span>

<span data-ttu-id="deba4-155">Essa função verifica cada constante em pSkipConstants para ver que:</span><span class="sxs-lookup"><span data-stu-id="deba4-155">This function checks each constant in pSkipConstants to see that:</span></span>

-   <span data-ttu-id="deba4-156">Ele está associado a um registro constante.</span><span class="sxs-lookup"><span data-stu-id="deba4-156">It is bound to a constant register.</span></span>
-   <span data-ttu-id="deba4-157">Ele só é usado no código do sombreador HLSL.</span><span class="sxs-lookup"><span data-stu-id="deba4-157">It is only used in HLSL shader code.</span></span>

<span data-ttu-id="deba4-158">Se uma constante for nomeada na cadeia de caracteres que não está presente no efeito, ela será ignorada.</span><span class="sxs-lookup"><span data-stu-id="deba4-158">If a constant is named in the string that is not present in the effect, it is ignored.</span></span>

<span data-ttu-id="deba4-159">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="deba4-159">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="deba4-160">Caso contrário, o tipo de dados LPCTSTR será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="deba4-160">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="deba4-161">A configuração do compilador também determina a versão da função.</span><span class="sxs-lookup"><span data-stu-id="deba4-161">The compiler setting also determines the function version.</span></span> <span data-ttu-id="deba4-162">Se o Unicode for definido, a chamada de função será resolvida como D3DXCreateEffectFromFileW.</span><span class="sxs-lookup"><span data-stu-id="deba4-162">If Unicode is defined, the function call resolves to D3DXCreateEffectFromFileW.</span></span> <span data-ttu-id="deba4-163">Caso contrário, a chamada de função é resolvida como D3DXCreateEffectFromFileA porque as cadeias de caracteres ANSI estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="deba4-163">Otherwise, the function call resolves to D3DXCreateEffectFromFileA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="deba4-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="deba4-164">Requirements</span></span>



| <span data-ttu-id="deba4-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="deba4-165">Requirement</span></span> | <span data-ttu-id="deba4-166">Valor</span><span class="sxs-lookup"><span data-stu-id="deba4-166">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="deba4-167">parâmetro</span><span class="sxs-lookup"><span data-stu-id="deba4-167">Header</span></span><br/>  | <dl> <span data-ttu-id="deba4-168"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="deba4-168"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="deba4-169">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="deba4-169">Library</span></span><br/> | <dl> <span data-ttu-id="deba4-170"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="deba4-170"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="deba4-171">Confira também</span><span class="sxs-lookup"><span data-stu-id="deba4-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="deba4-172">Funções de efeito</span><span class="sxs-lookup"><span data-stu-id="deba4-172">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="deba4-173">**D3DXCreateEffectEx**</span><span class="sxs-lookup"><span data-stu-id="deba4-173">**D3DXCreateEffectEx**</span></span>](d3dxcreateeffectex.md)
</dt> <dt>

[<span data-ttu-id="deba4-174">**D3DXCreateEffectFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="deba4-174">**D3DXCreateEffectFromResourceEx**</span></span>](d3dxcreateeffectfromresourceex.md)
</dt> </dl>

 

 
