---
description: Observação em vez de usar essa função herdada, recomendamos que você use a API D3DPreprocess. Crie um sombreador de um recurso sem compilá-lo.
ms.assetid: ca93e208-7627-4bf5-ab83-d4e906e149eb
title: Função D3DX10PreprocessShaderFromResource (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10PreprocessShaderFromResource
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 81a9f272cb0769d4313a4375f98bdc25b9e403e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104371026"
---
# <a name="d3dx10preprocessshaderfromresource-function"></a><span data-ttu-id="6a937-104">Função D3DX10PreprocessShaderFromResource</span><span class="sxs-lookup"><span data-stu-id="6a937-104">D3DX10PreprocessShaderFromResource function</span></span>

> [!Note]  
> <span data-ttu-id="6a937-105">Em vez de usar essa função herdada, recomendamos que você use a API [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="6a937-105">Instead of using this legacy function, we recommend that you use the [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API.</span></span>

 

<span data-ttu-id="6a937-106">Crie um sombreador de um recurso sem compilá-lo.</span><span class="sxs-lookup"><span data-stu-id="6a937-106">Create a shader from a resource without compiling it.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a937-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6a937-107">Syntax</span></span>


```C++
HRESULT D3DX10PreprocessShaderFromResource(
  _In_        HMODULE            hModule,
  _In_        LPCTSTR            pResourceName,
  _In_        LPCTSTR            pSrcFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="6a937-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6a937-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a937-109">*HMODULE* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6a937-109">*hModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a937-110">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a937-110">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a937-111">Identificador para o módulo de recurso que contém o sombreador.</span><span class="sxs-lookup"><span data-stu-id="6a937-111">Handle to the resource module containing the shader.</span></span> <span data-ttu-id="6a937-112">HMODULE pode ser obtido com a [função GetModuleHandle](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span><span class="sxs-lookup"><span data-stu-id="6a937-112">HMODULE can be obtained with [GetModuleHandle Function](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="6a937-113">*origem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6a937-113">*pResourceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a937-114">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a937-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a937-115">O nome do recurso no lado hModule que contém o sombreador.</span><span class="sxs-lookup"><span data-stu-id="6a937-115">The name of the resource in side hModule containing the shader.</span></span> <span data-ttu-id="6a937-116">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="6a937-116">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="6a937-117">Caso contrário, o tipo de dados será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="6a937-117">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="6a937-118">*pSrcFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6a937-118">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a937-119">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a937-119">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a937-120">Opcional.</span><span class="sxs-lookup"><span data-stu-id="6a937-120">Optional.</span></span> <span data-ttu-id="6a937-121">Nome do arquivo de efeito, que é usado somente para mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="6a937-121">Effect file name, which is used for error messages only.</span></span> <span data-ttu-id="6a937-122">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="6a937-122">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6a937-123">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6a937-123">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a937-124">Tipo: **\* [**macro const \_ D3D \_ Shader**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)**</span><span class="sxs-lookup"><span data-stu-id="6a937-124">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="6a937-125">Uma matriz de macros de sombreador terminada em nulo (consulte a [**\_ \_ macro do sombreador do D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); Defina como **NULL** para não especificar nenhuma macro.</span><span class="sxs-lookup"><span data-stu-id="6a937-125">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="6a937-126">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6a937-126">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a937-127">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="6a937-127">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="6a937-128">Um ponteiro para uma interface de inclusão (consulte a [**interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); Defina como **NULL** para especificar que não há nenhum arquivo de inclusão.</span><span class="sxs-lookup"><span data-stu-id="6a937-128">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="6a937-129">*pPump* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6a937-129">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a937-130">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="6a937-130">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="6a937-131">Um ponteiro para uma interface de bombeamento de thread (consulte a [**interface ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="6a937-131">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="6a937-132">Use **NULL** para especificar que essa função não deve retornar até que seja concluída.</span><span class="sxs-lookup"><span data-stu-id="6a937-132">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="6a937-133">*ppShaderText* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6a937-133">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a937-134">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="6a937-134">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="6a937-135">Um ponteiro para memória (consulte a [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) que contém o sombreador não compilado.</span><span class="sxs-lookup"><span data-stu-id="6a937-135">A pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains the uncompiled shader.</span></span>

</dd> <dt>

<span data-ttu-id="6a937-136">*ppErrorMsgs* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6a937-136">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a937-137">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="6a937-137">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="6a937-138">O endereço de um ponteiro para a memória (consulte a [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) que contém erros de criação de efeito, se houver.</span><span class="sxs-lookup"><span data-stu-id="6a937-138">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect-creation errors, if any occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a937-139">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6a937-139">Return value</span></span>

<span data-ttu-id="6a937-140">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6a937-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6a937-141">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="6a937-141">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6a937-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a937-142">Requirements</span></span>



| <span data-ttu-id="6a937-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a937-143">Requirement</span></span> | <span data-ttu-id="6a937-144">Valor</span><span class="sxs-lookup"><span data-stu-id="6a937-144">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6a937-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6a937-145">Header</span></span><br/>  | <dl> <span data-ttu-id="6a937-146"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a937-146"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="6a937-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6a937-147">Library</span></span><br/> | <dl> <span data-ttu-id="6a937-148"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a937-148"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a937-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="6a937-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a937-150">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="6a937-150">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
