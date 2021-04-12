---
description: Compile um sombreador e crie um processador de dados de forma assíncrona.
ms.assetid: 842db48b-51a7-4f32-8ea6-44247f2619b0
title: Função D3DX10CreateAsyncShaderCompilerProcessor (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncShaderCompilerProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 2a1cd663827cc32b868c9c6c9b74fbc3c21b8ee6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370938"
---
# <a name="d3dx10createasyncshadercompilerprocessor-function"></a><span data-ttu-id="53605-103">Função D3DX10CreateAsyncShaderCompilerProcessor</span><span class="sxs-lookup"><span data-stu-id="53605-103">D3DX10CreateAsyncShaderCompilerProcessor function</span></span>

<span data-ttu-id="53605-104">Compile um sombreador e crie um processador de dados de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="53605-104">Compile a shader and create a data processor asynchronously.</span></span>

## <a name="syntax"></a><span data-ttu-id="53605-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="53605-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncShaderCompilerProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pFunctionName,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags,
  _Out_       ID3D10Blob           **ppCompiledShader,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="53605-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="53605-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53605-107">*pFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="53605-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53605-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="53605-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="53605-109">Uma cadeia de caracteres que contém o nome de arquivo do sombreador.</span><span class="sxs-lookup"><span data-stu-id="53605-109">A string that contains the shader filename.</span></span>

</dd> <dt>

<span data-ttu-id="53605-110">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="53605-110">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53605-111">Tipo: **\* [**macro const \_ D3D \_ Shader**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)**</span><span class="sxs-lookup"><span data-stu-id="53605-111">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="53605-112">Uma matriz de macros de sombreador terminada em nulo (consulte a [**\_ \_ macro do sombreador do D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); Defina como **NULL** para não especificar nenhuma macro.</span><span class="sxs-lookup"><span data-stu-id="53605-112">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="53605-113">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="53605-113">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53605-114">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="53605-114">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="53605-115">Um ponteiro para uma interface de inclusão (consulte a [**interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); Defina como **NULL** para especificar que não há nenhum arquivo de inclusão.</span><span class="sxs-lookup"><span data-stu-id="53605-115">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="53605-116">*pFunctionName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="53605-116">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53605-117">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="53605-117">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="53605-118">Nome da função de ponto de entrada para o sombreador.</span><span class="sxs-lookup"><span data-stu-id="53605-118">Name of the entry point function for the shader.</span></span>

</dd> <dt>

<span data-ttu-id="53605-119">*pProfile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="53605-119">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53605-120">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="53605-120">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="53605-121">Uma cadeia de caracteres que especifica o [perfil do sombreador](../direct3dhlsl/dx-graphics-hlsl-models.md) ou o modelo de sombreador.</span><span class="sxs-lookup"><span data-stu-id="53605-121">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md) or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="53605-122">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="53605-122">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53605-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="53605-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="53605-124">HLSL opções de compilação (consulte os [sinalizadores de sombreador](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="53605-124">HLSL compile options (see [Shader Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="53605-125">*ppCompiledShader* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="53605-125">*ppCompiledShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53605-126">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="53605-126">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="53605-127">Endereço de um ponteiro para o sombreador compilado.</span><span class="sxs-lookup"><span data-stu-id="53605-127">Address of a pointer to the compiled shader.</span></span> <span data-ttu-id="53605-128">Consulte a [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob).</span><span class="sxs-lookup"><span data-stu-id="53605-128">See [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob).</span></span>

</dd> <dt>

<span data-ttu-id="53605-129">*ppErrorBuffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="53605-129">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53605-130">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="53605-130">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="53605-131">Endereço de um ponteiro para um buffer que contém erros de compilação (consulte a [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span><span class="sxs-lookup"><span data-stu-id="53605-131">Address of a pointer to a buffer that contains compile errors (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span></span>

</dd> <dt>

<span data-ttu-id="53605-132">*ppDataProcessor* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="53605-132">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53605-133">Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="53605-133">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="53605-134">Endereço de um ponteiro para um buffer que contém o processador de dados criado (consulte a [**interface ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="53605-134">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53605-135">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="53605-135">Return value</span></span>

<span data-ttu-id="53605-136">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="53605-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="53605-137">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="53605-137">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="53605-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53605-138">Requirements</span></span>



| <span data-ttu-id="53605-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="53605-139">Requirement</span></span> | <span data-ttu-id="53605-140">Valor</span><span class="sxs-lookup"><span data-stu-id="53605-140">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="53605-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="53605-141">Header</span></span><br/> | <dl> <span data-ttu-id="53605-142"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="53605-142"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53605-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="53605-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53605-144">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="53605-144">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
