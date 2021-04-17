---
description: Crie um efeito da memória.
ms.assetid: 6903a695-bb87-45fe-9913-25beeaf17233
title: Função D3DX10CreateEffectFromMemory (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateEffectFromMemory
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 03cbbc70e633f8289f99e094602cb1a912b711c5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105782452"
---
# <a name="d3dx10createeffectfrommemory-function"></a><span data-ttu-id="c20e2-103">Função D3DX10CreateEffectFromMemory</span><span class="sxs-lookup"><span data-stu-id="c20e2-103">D3DX10CreateEffectFromMemory function</span></span>

<span data-ttu-id="c20e2-104">Crie um efeito da memória.</span><span class="sxs-lookup"><span data-stu-id="c20e2-104">Create an effect from memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="c20e2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c20e2-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateEffectFromMemory(
  _In_        LPCVOID            pData,
  _In_        SIZE_T             DataLength,
  _In_        LPCSTR             pSrcFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
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



## <a name="parameters"></a><span data-ttu-id="c20e2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c20e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c20e2-107">*pData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c20e2-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c20e2-108">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c20e2-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c20e2-109">Ponteiro para o efeito na memória.</span><span class="sxs-lookup"><span data-stu-id="c20e2-109">Pointer to the effect in memory.</span></span>

</dd> <dt>

<span data-ttu-id="c20e2-110">*Comprimento* \[ de um no\]</span><span class="sxs-lookup"><span data-stu-id="c20e2-110">*DataLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c20e2-111">Tipo: **[ **tamanho \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c20e2-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c20e2-112">Tamanho do efeito na memória.</span><span class="sxs-lookup"><span data-stu-id="c20e2-112">Size of the effect in memory.</span></span>

</dd> <dt>

<span data-ttu-id="c20e2-113">*pSrcFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c20e2-113">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c20e2-114">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c20e2-114">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c20e2-115">Nome do arquivo de efeito na memória.</span><span class="sxs-lookup"><span data-stu-id="c20e2-115">Name of the effect file in memory.</span></span>

</dd> <dt>

<span data-ttu-id="c20e2-116">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c20e2-116">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c20e2-117">Tipo: **\* [**macro const \_ D3D \_ Shader**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)**</span><span class="sxs-lookup"><span data-stu-id="c20e2-117">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="c20e2-118">Uma matriz de macros de sombreador terminada em nulo (consulte a [**\_ \_ macro do sombreador do D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); Defina como **NULL** para não especificar nenhuma macro.</span><span class="sxs-lookup"><span data-stu-id="c20e2-118">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="c20e2-119">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c20e2-119">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c20e2-120">Tipo: **[ **ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="c20e2-120">Type: **[**ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span></span>

<span data-ttu-id="c20e2-121">Um ponteiro para uma interface de inclusão (consulte a [**interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="c20e2-121">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="c20e2-122">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c20e2-122">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c20e2-123">*pProfile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c20e2-123">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c20e2-124">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c20e2-124">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c20e2-125">Uma cadeia de caracteres que especifica o [perfil do sombreador](../direct3dhlsl/dx-graphics-hlsl-models.md)ou o modelo do sombreador.</span><span class="sxs-lookup"><span data-stu-id="c20e2-125">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md), or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="c20e2-126">*HLSLFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c20e2-126">*HLSLFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c20e2-127">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c20e2-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c20e2-128">HLSL opções de compilação (consulte as [ \_ constantes do sombreador d3d10](d3d10-shader.md)).</span><span class="sxs-lookup"><span data-stu-id="c20e2-128">HLSL compile options (see [D3D10\_SHADER Constants](d3d10-shader.md)).</span></span>

</dd> <dt>

<span data-ttu-id="c20e2-129">*FXFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c20e2-129">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c20e2-130">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c20e2-130">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c20e2-131">Opções de compilação de efeito (consulte [ \_ constantes de efeito de d3d10](d3d10-effect.md)).</span><span class="sxs-lookup"><span data-stu-id="c20e2-131">Effect compile options (see [D3D10\_EFFECT Constants](d3d10-effect.md)).</span></span>

</dd> <dt>

<span data-ttu-id="c20e2-132">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c20e2-132">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c20e2-133">Tipo: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="c20e2-133">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="c20e2-134">Um ponteiro para o dispositivo (consulte a [**interface ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) que usará os recursos.</span><span class="sxs-lookup"><span data-stu-id="c20e2-134">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="c20e2-135">*pEffectPool* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c20e2-135">*pEffectPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c20e2-136">Tipo: **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***</span><span class="sxs-lookup"><span data-stu-id="c20e2-136">Type: **[**ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***</span></span>

<span data-ttu-id="c20e2-137">Ponteiro para um pool de efeitos (consulte a [**interface ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) para compartilhar variáveis entre efeitos.</span><span class="sxs-lookup"><span data-stu-id="c20e2-137">Pointer to an effect pool (see [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) for sharing variables between effects.</span></span>

</dd> <dt>

<span data-ttu-id="c20e2-138">*pPump* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c20e2-138">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c20e2-139">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="c20e2-139">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="c20e2-140">Um ponteiro para uma interface de bombeamento de thread (consulte a [**interface ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="c20e2-140">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="c20e2-141">Use **NULL** para especificar que essa função não deve retornar até que seja concluída.</span><span class="sxs-lookup"><span data-stu-id="c20e2-141">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="c20e2-142">*ppEffect* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c20e2-142">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c20e2-143">Tipo: **[ **ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)\*\***</span><span class="sxs-lookup"><span data-stu-id="c20e2-143">Type: **[**ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)\*\***</span></span>

<span data-ttu-id="c20e2-144">Endereço de um ponteiro para o efeito (consulte a [**interface ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)) que é criada.</span><span class="sxs-lookup"><span data-stu-id="c20e2-144">Address of a pointer to the effect (see [**ID3D10Effect Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)) that is created.</span></span>

</dd> <dt>

<span data-ttu-id="c20e2-145">*ppErrors* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c20e2-145">*ppErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c20e2-146">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="c20e2-146">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="c20e2-147">O endereço de um ponteiro para a memória (consulte a [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) que contém erros de compilação de efeito, se houver algum.</span><span class="sxs-lookup"><span data-stu-id="c20e2-147">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="c20e2-148">*pHResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c20e2-148">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c20e2-149">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="c20e2-149">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="c20e2-150">Um ponteiro para o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="c20e2-150">A pointer to the return value.</span></span> <span data-ttu-id="c20e2-151">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c20e2-151">May be **NULL**.</span></span> <span data-ttu-id="c20e2-152">Se *pPump* não for **NULL**, *pHResult* deverá ser um local de memória válido até que a execução assíncrona seja concluída.</span><span class="sxs-lookup"><span data-stu-id="c20e2-152">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c20e2-153">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c20e2-153">Return value</span></span>

<span data-ttu-id="c20e2-154">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c20e2-154">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c20e2-155">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="c20e2-155">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c20e2-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c20e2-156">Requirements</span></span>



| <span data-ttu-id="c20e2-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="c20e2-157">Requirement</span></span> | <span data-ttu-id="c20e2-158">Valor</span><span class="sxs-lookup"><span data-stu-id="c20e2-158">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c20e2-159">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c20e2-159">Header</span></span><br/> | <dl> <span data-ttu-id="c20e2-160"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="c20e2-160"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c20e2-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="c20e2-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c20e2-162">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="c20e2-162">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
