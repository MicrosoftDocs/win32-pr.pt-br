---
description: Observação em vez de usar essa função herdada, recomendamos que você use a API D3DPreprocess. Crie um sombreador da memória sem compilá-lo.
ms.assetid: 099bc010-1269-4833-8a96-a7c78ed48206
title: Função D3DX10PreprocessShaderFromMemory (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10PreprocessShaderFromMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d1d06e46a5cd6b86420543b380f74273be032c17
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664063"
---
# <a name="d3dx10preprocessshaderfrommemory-function"></a><span data-ttu-id="e1c5b-104">Função D3DX10PreprocessShaderFromMemory</span><span class="sxs-lookup"><span data-stu-id="e1c5b-104">D3DX10PreprocessShaderFromMemory function</span></span>

> [!Note]  
> <span data-ttu-id="e1c5b-105">Em vez de usar essa função herdada, recomendamos que você use a API [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="e1c5b-105">Instead of using this legacy function, we recommend that you use the [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API.</span></span>

 

<span data-ttu-id="e1c5b-106">Crie um sombreador da memória sem compilá-lo.</span><span class="sxs-lookup"><span data-stu-id="e1c5b-106">Create a shader from memory without compiling it.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1c5b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e1c5b-107">Syntax</span></span>


```C++
HRESULT D3DX10PreprocessShaderFromMemory(
  _In_        LPCSTR             pSrcData,
  _In_        SIZE_T             SrcDataSize,
  _In_        LPCSTR             pFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="e1c5b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e1c5b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1c5b-109">*pSrcData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e1c5b-109">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1c5b-110">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e1c5b-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e1c5b-111">Ponteiro para a memória que contém o sombreador.</span><span class="sxs-lookup"><span data-stu-id="e1c5b-111">Pointer to the memory containing the shader.</span></span>

</dd> <dt>

<span data-ttu-id="e1c5b-112">*SrcDataSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e1c5b-112">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1c5b-113">Tipo: **[ **tamanho \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e1c5b-113">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e1c5b-114">Tamanho do sombreador.</span><span class="sxs-lookup"><span data-stu-id="e1c5b-114">Size of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="e1c5b-115">*pFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e1c5b-115">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1c5b-116">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e1c5b-116">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e1c5b-117">Nome do sombreador.</span><span class="sxs-lookup"><span data-stu-id="e1c5b-117">Name of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="e1c5b-118">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e1c5b-118">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1c5b-119">Tipo: **\* [**macro const \_ D3D \_ Shader**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)**</span><span class="sxs-lookup"><span data-stu-id="e1c5b-119">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="e1c5b-120">Uma matriz de macros de sombreador terminada em nulo (consulte a [**\_ \_ macro do sombreador do D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); Defina como **NULL** para não especificar nenhuma macro.</span><span class="sxs-lookup"><span data-stu-id="e1c5b-120">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="e1c5b-121">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e1c5b-121">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1c5b-122">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="e1c5b-122">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="e1c5b-123">Um ponteiro para uma interface de inclusão (consulte a [**interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); Defina como **NULL** para especificar que não há nenhum arquivo de inclusão.</span><span class="sxs-lookup"><span data-stu-id="e1c5b-123">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="e1c5b-124">*pPump* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e1c5b-124">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1c5b-125">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="e1c5b-125">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="e1c5b-126">Um ponteiro para uma interface de bombeamento de thread (consulte a [**interface ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="e1c5b-126">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="e1c5b-127">Use **NULL** para especificar que essa função não deve retornar até que seja concluída.</span><span class="sxs-lookup"><span data-stu-id="e1c5b-127">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="e1c5b-128">*ppShaderText* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e1c5b-128">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e1c5b-129">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="e1c5b-129">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="e1c5b-130">Um ponteiro para memória (consulte a [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) que contém o sombreador não compilado.</span><span class="sxs-lookup"><span data-stu-id="e1c5b-130">A pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains the uncompiled shader.</span></span>

</dd> <dt>

<span data-ttu-id="e1c5b-131">*ppErrorMsgs* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e1c5b-131">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e1c5b-132">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="e1c5b-132">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="e1c5b-133">O endereço de um ponteiro para a memória (consulte a [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) que contém erros de criação de efeito, se houver.</span><span class="sxs-lookup"><span data-stu-id="e1c5b-133">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect-creation errors, if any occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1c5b-134">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e1c5b-134">Return value</span></span>

<span data-ttu-id="e1c5b-135">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e1c5b-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e1c5b-136">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="e1c5b-136">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e1c5b-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1c5b-137">Requirements</span></span>



| <span data-ttu-id="e1c5b-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1c5b-138">Requirement</span></span> | <span data-ttu-id="e1c5b-139">Valor</span><span class="sxs-lookup"><span data-stu-id="e1c5b-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e1c5b-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e1c5b-140">Header</span></span><br/>  | <dl> <span data-ttu-id="e1c5b-141"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1c5b-141"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="e1c5b-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e1c5b-142">Library</span></span><br/> | <dl> <span data-ttu-id="e1c5b-143"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e1c5b-143"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1c5b-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1c5b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1c5b-145">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="e1c5b-145">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
