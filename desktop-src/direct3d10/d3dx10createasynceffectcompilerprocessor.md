---
description: Crie um processador de dados assíncronos para um efeito.
ms.assetid: 90a0dcd1-e495-4068-9f28-e2645370b984
title: Função D3DX10CreateAsyncEffectCompilerProcessor (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncEffectCompilerProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 9e1e5716228537d505adc4f48179ec7027b57198
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105772657"
---
# <a name="d3dx10createasynceffectcompilerprocessor-function"></a><span data-ttu-id="c3441-103">Função D3DX10CreateAsyncEffectCompilerProcessor</span><span class="sxs-lookup"><span data-stu-id="c3441-103">D3DX10CreateAsyncEffectCompilerProcessor function</span></span>

<span data-ttu-id="c3441-104">Crie um processador de dados assíncronos para um efeito.</span><span class="sxs-lookup"><span data-stu-id="c3441-104">Create an asynchronous-data processor for an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3441-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c3441-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncEffectCompilerProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        UINT                 Flags,
  _In_        UINT                 FXFlags,
  _Out_       ID3D10Blob           **ppCompiledShader,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="c3441-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c3441-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3441-107">*pFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c3441-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3441-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c3441-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c3441-109">Uma cadeia de caracteres que contém o nome de arquivo de efeito.</span><span class="sxs-lookup"><span data-stu-id="c3441-109">A string that contains the effect filename.</span></span>

</dd> <dt>

<span data-ttu-id="c3441-110">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c3441-110">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3441-111">Tipo: **\* [**macro const \_ D3D \_ Shader**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)**</span><span class="sxs-lookup"><span data-stu-id="c3441-111">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="c3441-112">Uma matriz de macros de sombreador terminada em nulo (consulte a [**\_ \_ macro do sombreador do D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); Defina como **NULL** para não especificar nenhuma macro.</span><span class="sxs-lookup"><span data-stu-id="c3441-112">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="c3441-113">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c3441-113">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3441-114">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="c3441-114">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="c3441-115">Um ponteiro para uma interface de inclusão (consulte a [**interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="c3441-115">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="c3441-116">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c3441-116">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c3441-117">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="c3441-117">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3441-118">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c3441-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c3441-119">[HLSL opções de compilação](d3d10-graphics-reference-effect-constants.md).</span><span class="sxs-lookup"><span data-stu-id="c3441-119">[HLSL compile options](d3d10-graphics-reference-effect-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3441-120">*FXFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c3441-120">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3441-121">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c3441-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c3441-122">[Opções de compilação de efeito](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="c3441-122">[Effect compile options](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="c3441-123">*ppCompiledShader* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c3441-123">*ppCompiledShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3441-124">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="c3441-124">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="c3441-125">Endereço de um ponteiro para o buffer (consulte a [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) que contém o efeito compilado.</span><span class="sxs-lookup"><span data-stu-id="c3441-125">Address of a pointer to buffer (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains the compiled effect.</span></span>

</dd> <dt>

<span data-ttu-id="c3441-126">*ppErrorBuffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c3441-126">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3441-127">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="c3441-127">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="c3441-128">Endereço de um ponteiro para um buffer (consulte a [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) que contém erros de compilação.</span><span class="sxs-lookup"><span data-stu-id="c3441-128">Address of a pointer to a buffer (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains compile errors.</span></span>

</dd> <dt>

<span data-ttu-id="c3441-129">*ppDataProcessor* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c3441-129">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3441-130">Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="c3441-130">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="c3441-131">Endereço de um ponteiro para um buffer que contém o processador de dados criado (consulte a [**interface ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="c3441-131">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3441-132">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c3441-132">Return value</span></span>

<span data-ttu-id="c3441-133">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c3441-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c3441-134">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="c3441-134">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c3441-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3441-135">Requirements</span></span>



| <span data-ttu-id="c3441-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3441-136">Requirement</span></span> | <span data-ttu-id="c3441-137">Valor</span><span class="sxs-lookup"><span data-stu-id="c3441-137">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3441-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c3441-138">Header</span></span><br/> | <dl> <span data-ttu-id="c3441-139"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3441-139"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3441-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3441-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3441-141">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="c3441-141">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
