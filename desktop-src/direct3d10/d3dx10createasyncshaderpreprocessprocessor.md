---
description: Crie um processador de dados para um sombreador de forma assíncrona.
ms.assetid: f5521e55-5f20-422d-979e-98b70efd3b13
title: Função D3DX10CreateAsyncShaderPreprocessProcessor (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncShaderPreprocessProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 14afdb899d99b7c0278d3042fbc9a108f446c692
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105782750"
---
# <a name="d3dx10createasyncshaderpreprocessprocessor-function"></a><span data-ttu-id="e8c47-103">Função D3DX10CreateAsyncShaderPreprocessProcessor</span><span class="sxs-lookup"><span data-stu-id="e8c47-103">D3DX10CreateAsyncShaderPreprocessProcessor function</span></span>

<span data-ttu-id="e8c47-104">Crie um processador de dados para um sombreador de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="e8c47-104">Create a data processor for a shader asynchronously.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8c47-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e8c47-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncShaderPreprocessProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _Out_       ID3D10Blob           **ppShaderText,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="e8c47-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e8c47-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8c47-107">*pFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e8c47-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8c47-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e8c47-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e8c47-109">Uma cadeia de caracteres que contém o nome de arquivo do sombreador.</span><span class="sxs-lookup"><span data-stu-id="e8c47-109">A string that contains the shader filename.</span></span>

</dd> <dt>

<span data-ttu-id="e8c47-110">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e8c47-110">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8c47-111">Tipo: **\* [**macro const \_ D3D \_ Shader**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)**</span><span class="sxs-lookup"><span data-stu-id="e8c47-111">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="e8c47-112">Uma matriz de macros de sombreador terminada em nulo (consulte a [**\_ \_ macro do sombreador do D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); Defina como **NULL** para não especificar nenhuma macro.</span><span class="sxs-lookup"><span data-stu-id="e8c47-112">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="e8c47-113">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e8c47-113">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8c47-114">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="e8c47-114">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="e8c47-115">Um ponteiro para uma interface de inclusão (consulte a [**interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); Defina como **NULL** para especificar que não há nenhum arquivo de inclusão.</span><span class="sxs-lookup"><span data-stu-id="e8c47-115">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="e8c47-116">*ppShaderText* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e8c47-116">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8c47-117">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="e8c47-117">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="e8c47-118">Endereço de um ponteiro para um buffer que contém o texto ASCII do sombreador (consulte a [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span><span class="sxs-lookup"><span data-stu-id="e8c47-118">Address of a pointer to a buffer that contains the ASCII text of the shader (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span></span>

</dd> <dt>

<span data-ttu-id="e8c47-119">*ppErrorBuffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e8c47-119">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8c47-120">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="e8c47-120">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="e8c47-121">Endereço de um ponteiro para um buffer que contém erros de compilação (consulte a [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span><span class="sxs-lookup"><span data-stu-id="e8c47-121">Address of a pointer to a buffer that contains compile errors (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span></span>

</dd> <dt>

<span data-ttu-id="e8c47-122">*ppDataProcessor* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e8c47-122">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8c47-123">Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="e8c47-123">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="e8c47-124">Endereço de um ponteiro para um buffer que contém o processador de dados criado (consulte a [**interface ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="e8c47-124">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8c47-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e8c47-125">Return value</span></span>

<span data-ttu-id="e8c47-126">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e8c47-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e8c47-127">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="e8c47-127">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e8c47-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8c47-128">Requirements</span></span>



| <span data-ttu-id="e8c47-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8c47-129">Requirement</span></span> | <span data-ttu-id="e8c47-130">Valor</span><span class="sxs-lookup"><span data-stu-id="e8c47-130">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8c47-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e8c47-131">Header</span></span><br/> | <dl> <span data-ttu-id="e8c47-132"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8c47-132"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8c47-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="e8c47-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8c47-134">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="e8c47-134">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
