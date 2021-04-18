---
description: Crie um pool de efeitos a partir de um efeito na memória.
ms.assetid: 634bcb23-a73f-4493-b805-e2aa5420fa2a
title: Função D3DX10CreateEffectPoolFromMemory (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateEffectPoolFromMemory
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 7dc93b7e73f336e75432debfe9bde6659ea4707c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105794008"
---
# <a name="d3dx10createeffectpoolfrommemory-function"></a><span data-ttu-id="0db7d-103">Função D3DX10CreateEffectPoolFromMemory</span><span class="sxs-lookup"><span data-stu-id="0db7d-103">D3DX10CreateEffectPoolFromMemory function</span></span>

<span data-ttu-id="0db7d-104">Crie um pool de efeitos a partir de um efeito na memória.</span><span class="sxs-lookup"><span data-stu-id="0db7d-104">Create an effect pool from an effect in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="0db7d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0db7d-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateEffectPoolFromMemory(
  _In_        LPCVOID            pData,
  _In_        SIZE_T             DataLength,
  _In_        LPCSTR             pSrcFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        ID3D10Include      *pInclude,
  _In_        LPCSTR             pProfile,
  _In_        UINT               HLSLFlags,
  _In_        UINT               FXFlags,
  _In_        ID3D10Device       *pDevice,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10EffectPool   **ppEffectPool,
  _Out_       ID3D10Blob         **ppErrors,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="0db7d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0db7d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0db7d-107">*pData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0db7d-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0db7d-108">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0db7d-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0db7d-109">Um ponteiro para o efeito.</span><span class="sxs-lookup"><span data-stu-id="0db7d-109">A pointer to the effect.</span></span>

</dd> <dt>

<span data-ttu-id="0db7d-110">*Comprimento* \[ de um no\]</span><span class="sxs-lookup"><span data-stu-id="0db7d-110">*DataLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0db7d-111">Tipo: **[ **tamanho \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0db7d-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0db7d-112">O tamanho do efeito.</span><span class="sxs-lookup"><span data-stu-id="0db7d-112">The size of the effect.</span></span>

</dd> <dt>

<span data-ttu-id="0db7d-113">*pSrcFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0db7d-113">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0db7d-114">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0db7d-114">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0db7d-115">O nome do arquivo de efeito.</span><span class="sxs-lookup"><span data-stu-id="0db7d-115">The name of the effect file.</span></span>

</dd> <dt>

<span data-ttu-id="0db7d-116">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0db7d-116">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0db7d-117">Tipo: **\* [**macro const \_ D3D \_ Shader**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)**</span><span class="sxs-lookup"><span data-stu-id="0db7d-117">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="0db7d-118">Uma matriz de macros de sombreador terminada em nulo (consulte a [**\_ \_ macro do sombreador do D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); Defina como **NULL** para não especificar nenhuma macro.</span><span class="sxs-lookup"><span data-stu-id="0db7d-118">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="0db7d-119">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0db7d-119">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0db7d-120">Tipo: **[ **ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="0db7d-120">Type: **[**ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span></span>

<span data-ttu-id="0db7d-121">Um ponteiro para uma interface de inclusão (consulte a [**interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="0db7d-121">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="0db7d-122">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="0db7d-122">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0db7d-123">*pProfile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0db7d-123">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0db7d-124">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0db7d-124">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0db7d-125">Uma cadeia de caracteres que especifica o [perfil do sombreador](../direct3dhlsl/dx-graphics-hlsl-models.md)ou o modelo do sombreador.</span><span class="sxs-lookup"><span data-stu-id="0db7d-125">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md), or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="0db7d-126">*HLSLFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0db7d-126">*HLSLFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0db7d-127">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0db7d-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0db7d-128">HLSL opções de compilação (consulte as [ \_ constantes do sombreador d3d10](d3d10-shader.md)).</span><span class="sxs-lookup"><span data-stu-id="0db7d-128">HLSL compile options (see [D3D10\_SHADER Constants](d3d10-shader.md)).</span></span>

</dd> <dt>

<span data-ttu-id="0db7d-129">*FXFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0db7d-129">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0db7d-130">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0db7d-130">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0db7d-131">Opções de compilação de efeito (consulte [sinalizadores de compilação e efeito](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="0db7d-131">Effect compile options (see [Compile and Effect Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="0db7d-132">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0db7d-132">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0db7d-133">Tipo: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="0db7d-133">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="0db7d-134">Um ponteiro para o dispositivo (consulte a [**interface ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) que usará os recursos.</span><span class="sxs-lookup"><span data-stu-id="0db7d-134">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="0db7d-135">*pPump* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0db7d-135">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0db7d-136">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="0db7d-136">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="0db7d-137">Um ponteiro para uma interface de bombeamento de thread (consulte a [**interface ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="0db7d-137">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="0db7d-138">Use **NULL** para especificar que essa função não deve retornar até que seja concluída.</span><span class="sxs-lookup"><span data-stu-id="0db7d-138">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="0db7d-139">*ppEffectPool* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0db7d-139">*ppEffectPool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0db7d-140">Tipo: **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\*\***</span><span class="sxs-lookup"><span data-stu-id="0db7d-140">Type: **[**ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\*\***</span></span>

<span data-ttu-id="0db7d-141">O endereço de um ponteiro para o pool de efeitos (consulte a [**interface ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)).</span><span class="sxs-lookup"><span data-stu-id="0db7d-141">The address of a pointer to the effect pool (see [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)).</span></span>

</dd> <dt>

<span data-ttu-id="0db7d-142">*ppErrors* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0db7d-142">*ppErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0db7d-143">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="0db7d-143">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="0db7d-144">O endereço de um ponteiro para a memória (consulte a [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) que contém erros de compilação de efeito, se houver algum.</span><span class="sxs-lookup"><span data-stu-id="0db7d-144">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="0db7d-145">*pHResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0db7d-145">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0db7d-146">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="0db7d-146">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="0db7d-147">Um ponteiro para o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="0db7d-147">A pointer to the return value.</span></span> <span data-ttu-id="0db7d-148">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="0db7d-148">May be **NULL**.</span></span> <span data-ttu-id="0db7d-149">Se *pPump* não for **NULL**, *pHResult* deverá ser um local de memória válido até que a execução assíncrona seja concluída.</span><span class="sxs-lookup"><span data-stu-id="0db7d-149">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0db7d-150">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0db7d-150">Return value</span></span>

<span data-ttu-id="0db7d-151">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0db7d-151">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0db7d-152">Retorna um dos seguintes [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="0db7d-152">Returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0db7d-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0db7d-153">Requirements</span></span>



| <span data-ttu-id="0db7d-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="0db7d-154">Requirement</span></span> | <span data-ttu-id="0db7d-155">Valor</span><span class="sxs-lookup"><span data-stu-id="0db7d-155">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0db7d-156">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0db7d-156">Header</span></span><br/> | <dl> <span data-ttu-id="0db7d-157"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="0db7d-157"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0db7d-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="0db7d-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0db7d-159">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="0db7d-159">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
