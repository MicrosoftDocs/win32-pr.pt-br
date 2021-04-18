---
description: Crie um pool de efeitos a partir de um recurso.
ms.assetid: 594ab788-fd96-4ea9-ad93-ef02fefa5d61
title: Função D3DX10CreateEffectPoolFromResource (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateEffectPoolFromResource
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 1fccc9c399a4573440318b92d1157738589da8a4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105802150"
---
# <a name="d3dx10createeffectpoolfromresource-function"></a><span data-ttu-id="60e73-103">Função D3DX10CreateEffectPoolFromResource</span><span class="sxs-lookup"><span data-stu-id="60e73-103">D3DX10CreateEffectPoolFromResource function</span></span>

<span data-ttu-id="60e73-104">Crie um pool de efeitos a partir de um recurso.</span><span class="sxs-lookup"><span data-stu-id="60e73-104">Create an effect pool from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="60e73-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="60e73-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateEffectPoolFromResource(
  _In_        HMODULE            hModule,
  _In_        LPCTSTR            pResourceName,
  _In_        LPCTSTR            pSrcFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        ID3D10Include      *pInclude,
  _In_        LPCSTR             pProfile,
  _In_        UINT               HLSLFlags,
  _In_        UINT               FXFlags,
  _In_        ID3D10Device       *pDevice,
  _In_        ID3DX10ThreadPump  *pPump,
  _In_        ID3D10EffectPool   **ppEffectPool,
  _In_        ID3D10Blob         **ppErrors,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="60e73-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="60e73-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60e73-107">*HMODULE* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="60e73-107">*hModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60e73-108">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="60e73-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="60e73-109">Um identificador para o módulo de recurso que contém o efeito.</span><span class="sxs-lookup"><span data-stu-id="60e73-109">A handle to the resource module containing the effect.</span></span> <span data-ttu-id="60e73-110">HMODULE pode ser obtido com a [função GetModuleHandle](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span><span class="sxs-lookup"><span data-stu-id="60e73-110">HMODULE can be obtained with [GetModuleHandle Function](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="60e73-111">*origem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="60e73-111">*pResourceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60e73-112">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="60e73-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="60e73-113">O nome do recurso em hModule.</span><span class="sxs-lookup"><span data-stu-id="60e73-113">The name of the resource in hModule.</span></span> <span data-ttu-id="60e73-114">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="60e73-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="60e73-115">Caso contrário, o tipo de dados será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="60e73-115">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="60e73-116">*pSrcFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="60e73-116">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60e73-117">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="60e73-117">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="60e73-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="60e73-118">Optional.</span></span> <span data-ttu-id="60e73-119">Nome do arquivo de efeito, que é usado somente para mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="60e73-119">Effect file name, which is used for error messages only.</span></span> <span data-ttu-id="60e73-120">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="60e73-120">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="60e73-121">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="60e73-121">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60e73-122">Tipo: **\* [**macro const \_ D3D \_ Shader**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)**</span><span class="sxs-lookup"><span data-stu-id="60e73-122">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="60e73-123">Uma matriz de macros de sombreador terminada em nulo (consulte a [**\_ \_ macro do sombreador do D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); Defina como **NULL** para não especificar nenhuma macro.</span><span class="sxs-lookup"><span data-stu-id="60e73-123">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="60e73-124">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="60e73-124">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60e73-125">Tipo: **[ **ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="60e73-125">Type: **[**ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span></span>

<span data-ttu-id="60e73-126">Um ponteiro para uma interface de inclusão (consulte a [**interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="60e73-126">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="60e73-127">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="60e73-127">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="60e73-128">*pProfile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="60e73-128">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60e73-129">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="60e73-129">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="60e73-130">Uma cadeia de caracteres que especifica o [perfil do sombreador](../direct3dhlsl/dx-graphics-hlsl-models.md)ou o modelo do sombreador.</span><span class="sxs-lookup"><span data-stu-id="60e73-130">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md), or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="60e73-131">*HLSLFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="60e73-131">*HLSLFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60e73-132">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="60e73-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="60e73-133">HLSL opções de compilação (consulte as [ \_ constantes do sombreador d3d10](d3d10-shader.md)).</span><span class="sxs-lookup"><span data-stu-id="60e73-133">HLSL compile options (see [D3D10\_SHADER Constants](d3d10-shader.md)).</span></span>

</dd> <dt>

<span data-ttu-id="60e73-134">*FXFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="60e73-134">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60e73-135">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="60e73-135">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="60e73-136">Opções de compilação de efeito (consulte [sinalizadores de compilação e efeito](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="60e73-136">Effect compile options (see [Compile and Effect Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="60e73-137">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="60e73-137">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60e73-138">Tipo: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="60e73-138">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="60e73-139">Um ponteiro para o dispositivo (consulte a [**interface ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) que usará os recursos.</span><span class="sxs-lookup"><span data-stu-id="60e73-139">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="60e73-140">*pPump* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="60e73-140">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60e73-141">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="60e73-141">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="60e73-142">Um ponteiro para uma interface de bombeamento de thread (consulte a [**interface ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="60e73-142">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="60e73-143">Use **NULL** para especificar que essa função não deve retornar até que seja concluída.</span><span class="sxs-lookup"><span data-stu-id="60e73-143">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="60e73-144">*ppEffectPool* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="60e73-144">*ppEffectPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60e73-145">Tipo: **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\*\***</span><span class="sxs-lookup"><span data-stu-id="60e73-145">Type: **[**ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\*\***</span></span>

<span data-ttu-id="60e73-146">O endereço de um ponteiro para o pool de efeitos (consulte a [**interface ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)).</span><span class="sxs-lookup"><span data-stu-id="60e73-146">The address of a pointer to the effect pool (see [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)).</span></span>

</dd> <dt>

<span data-ttu-id="60e73-147">*ppErrors* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="60e73-147">*ppErrors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60e73-148">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="60e73-148">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="60e73-149">O endereço de um ponteiro para a memória (consulte a [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) que contém erros de compilação de efeito, se houver algum.</span><span class="sxs-lookup"><span data-stu-id="60e73-149">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="60e73-150">*pHResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="60e73-150">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60e73-151">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="60e73-151">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="60e73-152">Um ponteiro para o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="60e73-152">A pointer to the return value.</span></span> <span data-ttu-id="60e73-153">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="60e73-153">May be **NULL**.</span></span> <span data-ttu-id="60e73-154">Se *pPump* não for **NULL**, *pHResult* deverá ser um local de memória válido até que a execução assíncrona seja concluída.</span><span class="sxs-lookup"><span data-stu-id="60e73-154">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60e73-155">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="60e73-155">Return value</span></span>

<span data-ttu-id="60e73-156">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="60e73-156">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="60e73-157">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="60e73-157">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="60e73-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60e73-158">Requirements</span></span>



| <span data-ttu-id="60e73-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="60e73-159">Requirement</span></span> | <span data-ttu-id="60e73-160">Valor</span><span class="sxs-lookup"><span data-stu-id="60e73-160">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="60e73-161">parâmetro</span><span class="sxs-lookup"><span data-stu-id="60e73-161">Header</span></span><br/> | <dl> <span data-ttu-id="60e73-162"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="60e73-162"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60e73-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="60e73-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60e73-164">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="60e73-164">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
