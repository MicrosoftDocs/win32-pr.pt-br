---
description: Crie um processador de dados assíncronos para um pool de memória.
ms.assetid: 3985a5e5-492e-4003-9d10-6e34620de69f
title: Função D3DX10CreateAsyncEffectPoolCreateProcessor (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncEffectPoolCreateProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 32e7c60f28a823c624b3866a8cdd46db659f8a49
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173060"
---
# <a name="d3dx10createasynceffectpoolcreateprocessor-function"></a><span data-ttu-id="a50e0-103">Função D3DX10CreateAsyncEffectPoolCreateProcessor</span><span class="sxs-lookup"><span data-stu-id="a50e0-103">D3DX10CreateAsyncEffectPoolCreateProcessor function</span></span>

<span data-ttu-id="a50e0-104">Crie um processador de dados assíncronos para um pool de memória.</span><span class="sxs-lookup"><span data-stu-id="a50e0-104">Create an asynchronous-data processor for a memory pool.</span></span>

## <a name="syntax"></a><span data-ttu-id="a50e0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a50e0-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncEffectPoolCreateProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags,
  _In_        UINT                 FXFlags,
  _In_        ID3D10Device         *pDevice,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="a50e0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a50e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a50e0-107">*pFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a50e0-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a50e0-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a50e0-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a50e0-109">Uma cadeia de caracteres que contém o nome de arquivo de efeito.</span><span class="sxs-lookup"><span data-stu-id="a50e0-109">A string that contains the effect filename.</span></span>

</dd> <dt>

<span data-ttu-id="a50e0-110">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a50e0-110">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a50e0-111">Tipo: **\* [**macro const \_ D3D \_ Shader**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)**</span><span class="sxs-lookup"><span data-stu-id="a50e0-111">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="a50e0-112">Uma matriz de macros de sombreador terminada em nulo (consulte a [**\_ \_ macro do sombreador do D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); Defina como **NULL** para não especificar nenhuma macro.</span><span class="sxs-lookup"><span data-stu-id="a50e0-112">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="a50e0-113">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a50e0-113">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a50e0-114">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="a50e0-114">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="a50e0-115">Um ponteiro para uma interface de inclusão (consulte a [**interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); Defina como **NULL** para especificar que não há nenhum arquivo de inclusão.</span><span class="sxs-lookup"><span data-stu-id="a50e0-115">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="a50e0-116">*pProfile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a50e0-116">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a50e0-117">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a50e0-117">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a50e0-118">Uma cadeia de caracteres que especifica o [perfil do sombreador](../direct3dhlsl/dx-graphics-hlsl-models.md) ou o modelo de sombreador.</span><span class="sxs-lookup"><span data-stu-id="a50e0-118">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md) or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="a50e0-119">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="a50e0-119">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a50e0-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a50e0-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a50e0-121">HLSL opções de compilação (consulte os [sinalizadores de sombreador](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="a50e0-121">HLSL compile options (see [Shader Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="a50e0-122">*FXFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a50e0-122">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a50e0-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a50e0-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a50e0-124">Opções de compilação de efeito (consulte [sinalizadores de compilação e efeito](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="a50e0-124">Effect compile options (see [Compile and Effect Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="a50e0-125">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a50e0-125">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a50e0-126">Tipo: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="a50e0-126">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="a50e0-127">Um ponteiro para o dispositivo (consulte a [**interface ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) que usará os recursos.</span><span class="sxs-lookup"><span data-stu-id="a50e0-127">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="a50e0-128">*ppErrorBuffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a50e0-128">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a50e0-129">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="a50e0-129">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="a50e0-130">O endereço de um ponteiro para a memória (consulte a [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) que contém erros de compilação de efeito, se houver algum.</span><span class="sxs-lookup"><span data-stu-id="a50e0-130">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="a50e0-131">*ppDataProcessor* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a50e0-131">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a50e0-132">Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="a50e0-132">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="a50e0-133">Endereço de um ponteiro para um buffer que contém o processador de dados criado (consulte a [**interface ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="a50e0-133">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a50e0-134">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a50e0-134">Return value</span></span>

<span data-ttu-id="a50e0-135">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a50e0-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a50e0-136">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="a50e0-136">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a50e0-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a50e0-137">Requirements</span></span>



| <span data-ttu-id="a50e0-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="a50e0-138">Requirement</span></span> | <span data-ttu-id="a50e0-139">Valor</span><span class="sxs-lookup"><span data-stu-id="a50e0-139">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a50e0-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a50e0-140">Header</span></span><br/> | <dl> <span data-ttu-id="a50e0-141"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="a50e0-141"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a50e0-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="a50e0-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a50e0-143">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="a50e0-143">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
