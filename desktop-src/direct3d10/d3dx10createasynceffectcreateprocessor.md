---
description: Crie um pool de efeitos de forma assíncrona.
ms.assetid: 50c55751-26de-4002-9a89-8e5ab59dda79
title: Função D3DX10CreateAsyncEffectCreateProcessor (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncEffectCreateProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 573efc51214031afe66f6cfd552bbda634d15142
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105791307"
---
# <a name="d3dx10createasynceffectcreateprocessor-function"></a><span data-ttu-id="71e6b-103">Função D3DX10CreateAsyncEffectCreateProcessor</span><span class="sxs-lookup"><span data-stu-id="71e6b-103">D3DX10CreateAsyncEffectCreateProcessor function</span></span>

<span data-ttu-id="71e6b-104">Crie um pool de efeitos de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="71e6b-104">Create an effect pool asynchronously.</span></span>

## <a name="syntax"></a><span data-ttu-id="71e6b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="71e6b-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncEffectCreateProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags,
  _In_        UINT                 FXFlags,
  _In_        ID3D10Device         *pDevice,
  _In_        ID3D10EffectPool     *pPool,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="71e6b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="71e6b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71e6b-107">*pFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="71e6b-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71e6b-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="71e6b-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="71e6b-109">Uma cadeia de caracteres que contém o nome de arquivo de efeito.</span><span class="sxs-lookup"><span data-stu-id="71e6b-109">A string that contains the effect filename.</span></span>

</dd> <dt>

<span data-ttu-id="71e6b-110">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="71e6b-110">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71e6b-111">Tipo: **\* [**macro const \_ D3D \_ Shader**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)**</span><span class="sxs-lookup"><span data-stu-id="71e6b-111">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="71e6b-112">Uma matriz de macros de sombreador terminada em nulo (consulte a [**\_ \_ macro do sombreador do D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); Defina como **NULL** para não especificar nenhuma macro.</span><span class="sxs-lookup"><span data-stu-id="71e6b-112">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="71e6b-113">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="71e6b-113">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71e6b-114">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="71e6b-114">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="71e6b-115">Um ponteiro para uma interface de inclusão (consulte a [**interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); Defina como **NULL** para especificar que não há nenhum arquivo de inclusão.</span><span class="sxs-lookup"><span data-stu-id="71e6b-115">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="71e6b-116">*pProfile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="71e6b-116">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71e6b-117">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="71e6b-117">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="71e6b-118">Uma cadeia de caracteres que especifica o [perfil do sombreador](../direct3dhlsl/dx-graphics-hlsl-models.md) ou o modelo de sombreador.</span><span class="sxs-lookup"><span data-stu-id="71e6b-118">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md) or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="71e6b-119">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="71e6b-119">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71e6b-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="71e6b-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="71e6b-121">HLSL opções de compilação (consulte os [sinalizadores de sombreador](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="71e6b-121">HLSL compile options (see [Shader Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="71e6b-122">*FXFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="71e6b-122">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71e6b-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="71e6b-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="71e6b-124">Opções de compilação de efeito (consulte [sinalizadores de compilação e efeito](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="71e6b-124">Effect compile options (see [Compile and Effect Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="71e6b-125">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="71e6b-125">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71e6b-126">Tipo: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="71e6b-126">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="71e6b-127">Um ponteiro para o dispositivo (consulte a [**interface ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) que usará os recursos.</span><span class="sxs-lookup"><span data-stu-id="71e6b-127">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="71e6b-128">*pPool* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="71e6b-128">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71e6b-129">Tipo: **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***</span><span class="sxs-lookup"><span data-stu-id="71e6b-129">Type: **[**ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***</span></span>

<span data-ttu-id="71e6b-130">Um ponteiro para um pool de efeitos (consulte a [**interface ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) para compartilhar variáveis entre efeitos.</span><span class="sxs-lookup"><span data-stu-id="71e6b-130">A pointer to an effect pool (see [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) for sharing variables between effects.</span></span>

</dd> <dt>

<span data-ttu-id="71e6b-131">*ppErrorBuffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="71e6b-131">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71e6b-132">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="71e6b-132">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="71e6b-133">O endereço de um ponteiro para a memória (consulte a [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) que contém erros de compilação de efeito, se houver algum.</span><span class="sxs-lookup"><span data-stu-id="71e6b-133">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="71e6b-134">*ppProcessor* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="71e6b-134">*ppProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71e6b-135">Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="71e6b-135">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="71e6b-136">O endereço de um ponteiro para o processador de dados assíncronos (consulte a [**interface ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="71e6b-136">The address of a pointer to the asynchronous-data processor (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71e6b-137">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="71e6b-137">Return value</span></span>

<span data-ttu-id="71e6b-138">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="71e6b-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="71e6b-139">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="71e6b-139">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="71e6b-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71e6b-140">Requirements</span></span>



| <span data-ttu-id="71e6b-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="71e6b-141">Requirement</span></span> | <span data-ttu-id="71e6b-142">Valor</span><span class="sxs-lookup"><span data-stu-id="71e6b-142">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="71e6b-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="71e6b-143">Header</span></span><br/> | <dl> <span data-ttu-id="71e6b-144"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="71e6b-144"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71e6b-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="71e6b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71e6b-146">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="71e6b-146">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
