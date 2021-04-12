---
description: Crie um efeito a partir de um recurso.
ms.assetid: 239a3b14-9eea-4a0f-96b5-3959b7be3e19
title: Função D3DX10CreateEffectFromResource (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateEffectFromResource
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 6c5f7b7805e126f02c2658ddce6ec5029978de53
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298669"
---
# <a name="d3dx10createeffectfromresource-function"></a><span data-ttu-id="9eaf3-103">Função D3DX10CreateEffectFromResource</span><span class="sxs-lookup"><span data-stu-id="9eaf3-103">D3DX10CreateEffectFromResource function</span></span>

<span data-ttu-id="9eaf3-104">Crie um efeito a partir de um recurso.</span><span class="sxs-lookup"><span data-stu-id="9eaf3-104">Create an effect from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="9eaf3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9eaf3-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateEffectFromResource(
  _In_        HMODULE            hModule,
  _In_        LPCTSTR            pResourceName,
  _In_        LPCTSTR            pSrcFileName,
  _In_  const D3D10_SHADER_MACRO *pDefines,
  _In_        ID3D10Include      *pInclude,
  _In_        LPCSTR             pProfile,
  _In_        UINT               HLSLFlags,
  _In_        UINT               FXFlags,
  _In_        ID3D10Device       *pDevice,
  _In_        ID3D10EffectPool   *pEffectPool,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Effect       **ppEffect,
  _Out_       ID3D10Blob         **ppErrors,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="9eaf3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9eaf3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9eaf3-107">*HMODULE* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9eaf3-107">*hModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9eaf3-108">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9eaf3-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9eaf3-109">Um identificador para o módulo de recurso que contém o efeito.</span><span class="sxs-lookup"><span data-stu-id="9eaf3-109">A handle to the resource module containing the effect.</span></span> <span data-ttu-id="9eaf3-110">HMODULE pode ser obtido com a [função GetModuleHandle](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span><span class="sxs-lookup"><span data-stu-id="9eaf3-110">HMODULE can be obtained with [GetModuleHandle Function](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="9eaf3-111">*origem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9eaf3-111">*pResourceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9eaf3-112">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9eaf3-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9eaf3-113">Nome do recurso no hModule.</span><span class="sxs-lookup"><span data-stu-id="9eaf3-113">Name of the resource in hModule.</span></span> <span data-ttu-id="9eaf3-114">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="9eaf3-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="9eaf3-115">Caso contrário, o tipo de dados será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="9eaf3-115">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="9eaf3-116">*pSrcFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9eaf3-116">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9eaf3-117">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9eaf3-117">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9eaf3-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="9eaf3-118">Optional.</span></span> <span data-ttu-id="9eaf3-119">Nome do arquivo de efeito, que é usado somente para mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="9eaf3-119">Effect file name, which is used for error messages only.</span></span> <span data-ttu-id="9eaf3-120">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="9eaf3-120">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9eaf3-121">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9eaf3-121">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9eaf3-122">Tipo: **\* [**macro const \_ D3D \_ Shader**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)**</span><span class="sxs-lookup"><span data-stu-id="9eaf3-122">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="9eaf3-123">Uma matriz de macros de sombreador terminada em nulo (consulte a [**\_ \_ macro do sombreador do D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); Defina como **NULL** para não especificar nenhuma macro.</span><span class="sxs-lookup"><span data-stu-id="9eaf3-123">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="9eaf3-124">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9eaf3-124">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9eaf3-125">Tipo: **[ **ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="9eaf3-125">Type: **[**ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span></span>

<span data-ttu-id="9eaf3-126">Um ponteiro para uma interface de inclusão (consulte a [**interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="9eaf3-126">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="9eaf3-127">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="9eaf3-127">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9eaf3-128">*pProfile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9eaf3-128">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9eaf3-129">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9eaf3-129">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9eaf3-130">Uma cadeia de caracteres que especifica o [perfil do sombreador](../direct3dhlsl/dx-graphics-hlsl-models.md)ou o modelo do sombreador.</span><span class="sxs-lookup"><span data-stu-id="9eaf3-130">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md), or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="9eaf3-131">*HLSLFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9eaf3-131">*HLSLFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9eaf3-132">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9eaf3-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9eaf3-133">HLSL opções de compilação (consulte as [ \_ constantes do sombreador d3d10](d3d10-shader.md)).</span><span class="sxs-lookup"><span data-stu-id="9eaf3-133">HLSL compile options (see [D3D10\_SHADER Constants](d3d10-shader.md)).</span></span>

</dd> <dt>

<span data-ttu-id="9eaf3-134">*FXFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9eaf3-134">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9eaf3-135">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9eaf3-135">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9eaf3-136">Opções de compilação de efeito (consulte [sinalizadores de compilação e efeito](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="9eaf3-136">Effect compile options (see [Compile and Effect Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="9eaf3-137">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9eaf3-137">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9eaf3-138">Tipo: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="9eaf3-138">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="9eaf3-139">Um ponteiro para o dispositivo (consulte a [**interface ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) que usará os recursos.</span><span class="sxs-lookup"><span data-stu-id="9eaf3-139">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="9eaf3-140">*pEffectPool* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9eaf3-140">*pEffectPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9eaf3-141">Tipo: **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***</span><span class="sxs-lookup"><span data-stu-id="9eaf3-141">Type: **[**ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***</span></span>

<span data-ttu-id="9eaf3-142">Ponteiro para um pool de efeitos (consulte a [**interface ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) para compartilhar variáveis entre efeitos.</span><span class="sxs-lookup"><span data-stu-id="9eaf3-142">Pointer to an effect pool (see [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) for sharing variables between effects.</span></span>

</dd> <dt>

<span data-ttu-id="9eaf3-143">*pPump* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9eaf3-143">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9eaf3-144">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="9eaf3-144">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="9eaf3-145">Um ponteiro para uma interface de bombeamento de thread (consulte a [**interface ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="9eaf3-145">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="9eaf3-146">Use **NULL** para especificar que essa função não deve retornar até que seja concluída.</span><span class="sxs-lookup"><span data-stu-id="9eaf3-146">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="9eaf3-147">*ppEffect* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9eaf3-147">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9eaf3-148">Tipo: **[ **ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)\*\***</span><span class="sxs-lookup"><span data-stu-id="9eaf3-148">Type: **[**ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)\*\***</span></span>

<span data-ttu-id="9eaf3-149">Endereço de um ponteiro para o efeito (consulte a [**interface ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)) que é criada.</span><span class="sxs-lookup"><span data-stu-id="9eaf3-149">Address of a pointer to the effect (see [**ID3D10Effect Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)) that is created.</span></span>

</dd> <dt>

<span data-ttu-id="9eaf3-150">*ppErrors* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9eaf3-150">*ppErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9eaf3-151">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="9eaf3-151">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="9eaf3-152">O endereço de um ponteiro para a memória (consulte a [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) que contém erros de compilação de efeito, se houver algum.</span><span class="sxs-lookup"><span data-stu-id="9eaf3-152">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="9eaf3-153">*pHResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9eaf3-153">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9eaf3-154">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="9eaf3-154">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="9eaf3-155">Um ponteiro para o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="9eaf3-155">A pointer to the return value.</span></span> <span data-ttu-id="9eaf3-156">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="9eaf3-156">May be **NULL**.</span></span> <span data-ttu-id="9eaf3-157">Se *pPump* não for **NULL**, *pHResult* deverá ser um local de memória válido até que a execução assíncrona seja concluída.</span><span class="sxs-lookup"><span data-stu-id="9eaf3-157">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9eaf3-158">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9eaf3-158">Return value</span></span>

<span data-ttu-id="9eaf3-159">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9eaf3-159">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9eaf3-160">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="9eaf3-160">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9eaf3-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9eaf3-161">Requirements</span></span>



| <span data-ttu-id="9eaf3-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="9eaf3-162">Requirement</span></span> | <span data-ttu-id="9eaf3-163">Valor</span><span class="sxs-lookup"><span data-stu-id="9eaf3-163">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9eaf3-164">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9eaf3-164">Header</span></span><br/> | <dl> <span data-ttu-id="9eaf3-165"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="9eaf3-165"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9eaf3-166">Confira também</span><span class="sxs-lookup"><span data-stu-id="9eaf3-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9eaf3-167">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="9eaf3-167">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
