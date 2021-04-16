---
description: Observação em vez de usar essa função herdada, recomendamos que você use a API D3DPreprocess. Crie um sombreador de um arquivo sem compilá-lo.
ms.assetid: 9f609aa5-5ee7-45fb-9693-69de130b6cc0
title: Função D3DX10PreprocessShaderFromFile (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10PreprocessShaderFromFile
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: e6222febd378b262d9fb9e87a6224968c2d04038
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105765340"
---
# <a name="d3dx10preprocessshaderfromfile-function"></a><span data-ttu-id="d9a17-104">Função D3DX10PreprocessShaderFromFile</span><span class="sxs-lookup"><span data-stu-id="d9a17-104">D3DX10PreprocessShaderFromFile function</span></span>

> [!Note]  
> <span data-ttu-id="d9a17-105">Em vez de usar essa função herdada, recomendamos que você use a API [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="d9a17-105">Instead of using this legacy function, we recommend that you use the [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API.</span></span>

 

<span data-ttu-id="d9a17-106">Crie um sombreador de um arquivo sem compilá-lo.</span><span class="sxs-lookup"><span data-stu-id="d9a17-106">Create a shader from a file without compiling it.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9a17-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d9a17-107">Syntax</span></span>


```C++
HRESULT D3DX10PreprocessShaderFromFile(
  _In_        LPCTSTR            pFileName,
  _In_  const D3D10_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="d9a17-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d9a17-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9a17-109">*pFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d9a17-109">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9a17-110">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d9a17-110">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d9a17-111">Nome do arquivo do sombreador.</span><span class="sxs-lookup"><span data-stu-id="d9a17-111">Name of the shader file.</span></span>

</dd> <dt>

<span data-ttu-id="d9a17-112">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d9a17-112">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9a17-113">Tipo: **\* [**macro const \_ D3D \_ Shader**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)**</span><span class="sxs-lookup"><span data-stu-id="d9a17-113">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="d9a17-114">Uma matriz de macros de sombreador terminada em nulo (consulte a [**\_ \_ macro do sombreador do D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); Defina como **NULL** para não especificar nenhuma macro.</span><span class="sxs-lookup"><span data-stu-id="d9a17-114">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="d9a17-115">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d9a17-115">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9a17-116">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="d9a17-116">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="d9a17-117">Um ponteiro para uma interface de inclusão (consulte a [**interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); Defina como **NULL** para especificar que não há nenhum arquivo de inclusão.</span><span class="sxs-lookup"><span data-stu-id="d9a17-117">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="d9a17-118">*pPump* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d9a17-118">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9a17-119">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="d9a17-119">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="d9a17-120">Um ponteiro para uma interface de bombeamento de thread (consulte a [**interface ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="d9a17-120">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="d9a17-121">Use **NULL** para especificar que essa função não deve retornar até que seja concluída.</span><span class="sxs-lookup"><span data-stu-id="d9a17-121">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="d9a17-122">*ppShaderText* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d9a17-122">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9a17-123">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="d9a17-123">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="d9a17-124">Um ponteiro para memória (consulte a [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) que contém o sombreador não compilado.</span><span class="sxs-lookup"><span data-stu-id="d9a17-124">A pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains the uncompiled shader.</span></span>

</dd> <dt>

<span data-ttu-id="d9a17-125">*ppErrorMsgs* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d9a17-125">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9a17-126">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="d9a17-126">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="d9a17-127">O endereço de um ponteiro para a memória (consulte a [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) que contém erros de criação de efeito, se houver.</span><span class="sxs-lookup"><span data-stu-id="d9a17-127">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect-creation errors, if any occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9a17-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d9a17-128">Return value</span></span>

<span data-ttu-id="d9a17-129">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d9a17-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d9a17-130">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="d9a17-130">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d9a17-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9a17-131">Requirements</span></span>



| <span data-ttu-id="d9a17-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9a17-132">Requirement</span></span> | <span data-ttu-id="d9a17-133">Valor</span><span class="sxs-lookup"><span data-stu-id="d9a17-133">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9a17-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d9a17-134">Header</span></span><br/> | <dl> <span data-ttu-id="d9a17-135"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9a17-135"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9a17-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="d9a17-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9a17-137">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="d9a17-137">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
