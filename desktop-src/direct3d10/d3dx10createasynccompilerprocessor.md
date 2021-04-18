---
description: Crie um processador de dados assíncronos para um sombreador.
ms.assetid: e23290fa-ccd7-4703-ae6b-4fffe352875e
title: Função D3DX10CreateAsyncCompilerProcessor (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncCompilerProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 1fa6a558efd56917832da3280df2aad4ac400def
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172963"
---
# <a name="d3dx10createasynccompilerprocessor-function"></a><span data-ttu-id="d4ab9-103">Função D3DX10CreateAsyncCompilerProcessor</span><span class="sxs-lookup"><span data-stu-id="d4ab9-103">D3DX10CreateAsyncCompilerProcessor function</span></span>

<span data-ttu-id="d4ab9-104">Crie um processador de dados assíncronos para um sombreador.</span><span class="sxs-lookup"><span data-stu-id="d4ab9-104">Create an asynchronous-data processor for a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4ab9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d4ab9-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncCompilerProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D10_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pFunctionName,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags1,
  _In_        UINT                 Flags2,
  _Out_       ID3D10Blob           **ppCompiledShader,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="d4ab9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d4ab9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4ab9-107">*pFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d4ab9-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4ab9-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4ab9-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d4ab9-109">Uma cadeia de caracteres que contém o nome de arquivo do sombreador.</span><span class="sxs-lookup"><span data-stu-id="d4ab9-109">A string that contains the shader filename.</span></span>

</dd> <dt>

<span data-ttu-id="d4ab9-110">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d4ab9-110">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4ab9-111">Tipo: **\* [**macro const \_ D3D \_ Shader**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)**</span><span class="sxs-lookup"><span data-stu-id="d4ab9-111">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="d4ab9-112">Uma matriz de macros de sombreador terminada em nulo (consulte a [**\_ \_ macro do sombreador do D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); Defina como **NULL** para não especificar nenhuma macro.</span><span class="sxs-lookup"><span data-stu-id="d4ab9-112">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="d4ab9-113">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d4ab9-113">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4ab9-114">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="d4ab9-114">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="d4ab9-115">Um ponteiro para uma interface de inclusão (consulte a [**interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="d4ab9-115">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="d4ab9-116">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d4ab9-116">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d4ab9-117">*pFunctionName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d4ab9-117">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4ab9-118">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4ab9-118">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d4ab9-119">Nome da função de ponto de entrada do sombreador em que começa a execução do sombreador.</span><span class="sxs-lookup"><span data-stu-id="d4ab9-119">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="d4ab9-120">Quando você compila um efeito, o **D3DX10CreateAsyncCompilerProcessor** ignora *pFunctionName*; Recomendamos que você defina *pFunctionName* como **NULL** porque é uma boa prática de programação definir um parâmetro de ponteiro como **nulo** se a função chamada não o usar.</span><span class="sxs-lookup"><span data-stu-id="d4ab9-120">When you compile an effect, **D3DX10CreateAsyncCompilerProcessor** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="d4ab9-121">*pProfile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d4ab9-121">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4ab9-122">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4ab9-122">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d4ab9-123">Uma cadeia de caracteres que especifica o [perfil do sombreador](../direct3dhlsl/dx-graphics-hlsl-models.md) ou o modelo de sombreador.</span><span class="sxs-lookup"><span data-stu-id="d4ab9-123">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md) or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="d4ab9-124">*Flags1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d4ab9-124">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4ab9-125">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4ab9-125">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d4ab9-126">[Sinalizadores de compilação de sombreador](d3d10-shader.md).</span><span class="sxs-lookup"><span data-stu-id="d4ab9-126">[Shader compile flags](d3d10-shader.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4ab9-127">*Flags2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d4ab9-127">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4ab9-128">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4ab9-128">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d4ab9-129">[Sinalizadores de compilação de efeito](d3d10-graphics-reference-effect-constants.md).</span><span class="sxs-lookup"><span data-stu-id="d4ab9-129">[Effect compile flags](d3d10-graphics-reference-effect-constants.md).</span></span> <span data-ttu-id="d4ab9-130">Quando você compila um sombreador e não um arquivo de efeito, o **D3DX10CreateAsyncCompilerProcessor** ignora *Flags2*; é recomendável que você defina *Flags2* como zero porque é uma boa prática de programação definir um parâmetro de ponteiro como **nulo** se a função chamada não o usar.</span><span class="sxs-lookup"><span data-stu-id="d4ab9-130">When you compile a shader and not an effect file, **D3DX10CreateAsyncCompilerProcessor** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="d4ab9-131">*ppCompiledShader* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d4ab9-131">*ppCompiledShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4ab9-132">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="d4ab9-132">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="d4ab9-133">Endereço de um ponteiro para o efeito compilado (consulte a [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span><span class="sxs-lookup"><span data-stu-id="d4ab9-133">Address of a pointer to the compiled effect (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span></span>

</dd> <dt>

<span data-ttu-id="d4ab9-134">*ppErrorBuffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d4ab9-134">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4ab9-135">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="d4ab9-135">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="d4ab9-136">Endereço de um ponteiro para erros de compilação (consulte a [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span><span class="sxs-lookup"><span data-stu-id="d4ab9-136">Address of a pointer to compile errors (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span></span>

</dd> <dt>

<span data-ttu-id="d4ab9-137">*ppDataProcessor* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d4ab9-137">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4ab9-138">Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="d4ab9-138">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="d4ab9-139">Endereço de um ponteiro para um buffer que contém o processador de dados criado (consulte a [**interface ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="d4ab9-139">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4ab9-140">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d4ab9-140">Return value</span></span>

<span data-ttu-id="d4ab9-141">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d4ab9-141">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d4ab9-142">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="d4ab9-142">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d4ab9-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4ab9-143">Requirements</span></span>



| <span data-ttu-id="d4ab9-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4ab9-144">Requirement</span></span> | <span data-ttu-id="d4ab9-145">Valor</span><span class="sxs-lookup"><span data-stu-id="d4ab9-145">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4ab9-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d4ab9-146">Header</span></span><br/> | <dl> <span data-ttu-id="d4ab9-147"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4ab9-147"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4ab9-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="d4ab9-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4ab9-149">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="d4ab9-149">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
