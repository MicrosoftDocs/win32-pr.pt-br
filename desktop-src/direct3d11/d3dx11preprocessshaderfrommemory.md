---
title: Função D3DX11PreprocessShaderFromMemory (D3DX11async. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Observação em vez de usar essa função, recomendamos que você use a API D3DPreprocess. Crie um sombreador da memória sem compilá-lo.
ms.assetid: 3c646914-9334-44fe-a8a0-b84d0dc1a16e
keywords:
- Função D3DX11PreprocessShaderFromMemory Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11PreprocessShaderFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71a94633270fe0f4e462e60915de862be8693daa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989334"
---
# <a name="d3dx11preprocessshaderfrommemory-function"></a><span data-ttu-id="4cee4-106">Função D3DX11PreprocessShaderFromMemory</span><span class="sxs-lookup"><span data-stu-id="4cee4-106">D3DX11PreprocessShaderFromMemory function</span></span>

> [!Note]  
> <span data-ttu-id="4cee4-107">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="4cee4-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="4cee4-108">Em vez de usar essa função, recomendamos que você use a API [**D3DPreprocess**](/windows/desktop/direct3dhlsl/d3dpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="4cee4-108">Instead of using this function, we recommend that you use the [**D3DPreprocess**](/windows/desktop/direct3dhlsl/d3dpreprocess) API.</span></span>

 

<span data-ttu-id="4cee4-109">Crie um sombreador da memória sem compilá-lo.</span><span class="sxs-lookup"><span data-stu-id="4cee4-109">Create a shader from memory without compiling it.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cee4-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4cee4-110">Syntax</span></span>


```C++
HRESULT D3DX11PreprocessShaderFromMemory(
  _In_        LPCSTR             pSrcData,
  _In_        SIZE_T             SrcDataSize,
  _In_        LPCSTR             pFileName,
  _In_  const D3D11_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX11ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="4cee4-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4cee4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cee4-112">*pSrcData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4cee4-112">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cee4-113">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4cee4-113">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="4cee4-114">Ponteiro para a memória que contém o sombreador.</span><span class="sxs-lookup"><span data-stu-id="4cee4-114">Pointer to the memory containing the shader.</span></span>

</dd> <dt>

<span data-ttu-id="4cee4-115">*SrcDataSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4cee4-115">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cee4-116">Tipo: **[ **tamanho \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4cee4-116">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="4cee4-117">Tamanho do sombreador.</span><span class="sxs-lookup"><span data-stu-id="4cee4-117">Size of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="4cee4-118">*pFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4cee4-118">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cee4-119">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4cee4-119">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="4cee4-120">Nome do sombreador.</span><span class="sxs-lookup"><span data-stu-id="4cee4-120">Name of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="4cee4-121">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4cee4-121">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cee4-122">Tipo: **\_ \_ macro \* do sombreador D3D11 const**</span><span class="sxs-lookup"><span data-stu-id="4cee4-122">Type: **const D3D11\_SHADER\_MACRO\***</span></span>

<span data-ttu-id="4cee4-123">Uma matriz com terminação nula de macros de sombreador; Defina como **NULL** para não especificar nenhuma macro.</span><span class="sxs-lookup"><span data-stu-id="4cee4-123">A NULL-terminated array of shader macros; set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="4cee4-124">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4cee4-124">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cee4-125">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="4cee4-125">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="4cee4-126">Um ponteiro para uma interface de inclusão; Defina como **NULL** para especificar que não há nenhum arquivo de inclusão.</span><span class="sxs-lookup"><span data-stu-id="4cee4-126">A pointer to an include interface; set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="4cee4-127">*pPump* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4cee4-127">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cee4-128">Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="4cee4-128">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="4cee4-129">Um ponteiro para uma interface de bombeamento de thread (consulte a [**interface ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="4cee4-129">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="4cee4-130">Use **NULL** para especificar que essa função não deve retornar até que seja concluída.</span><span class="sxs-lookup"><span data-stu-id="4cee4-130">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="4cee4-131">*ppShaderText* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="4cee4-131">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4cee4-132">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="4cee4-132">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="4cee4-133">Um ponteiro para a memória que contém o sombreador não compilado.</span><span class="sxs-lookup"><span data-stu-id="4cee4-133">A pointer to memory that contains the uncompiled shader.</span></span>

</dd> <dt>

<span data-ttu-id="4cee4-134">*ppErrorMsgs* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="4cee4-134">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4cee4-135">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="4cee4-135">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="4cee4-136">O endereço de um ponteiro para memória que contém erros de criação de efeito, se houver.</span><span class="sxs-lookup"><span data-stu-id="4cee4-136">The address of a pointer to memory that contains effect-creation errors, if any occurred.</span></span>

</dd> <dt>

<span data-ttu-id="4cee4-137">*pHResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="4cee4-137">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4cee4-138">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="4cee4-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="4cee4-139">Um ponteiro para o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="4cee4-139">A pointer to the return value.</span></span> <span data-ttu-id="4cee4-140">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="4cee4-140">May be **NULL**.</span></span> <span data-ttu-id="4cee4-141">Se *pPump* não for **NULL**, *pHResult* deverá ser um local de memória válido até que a execução assíncrona seja concluída.</span><span class="sxs-lookup"><span data-stu-id="4cee4-141">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cee4-142">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4cee4-142">Return value</span></span>

<span data-ttu-id="4cee4-143">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4cee4-143">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4cee4-144">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="4cee4-144">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4cee4-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4cee4-145">Requirements</span></span>



| <span data-ttu-id="4cee4-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cee4-146">Requirement</span></span> | <span data-ttu-id="4cee4-147">Valor</span><span class="sxs-lookup"><span data-stu-id="4cee4-147">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cee4-148">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4cee4-148">Header</span></span><br/>  | <dl> <span data-ttu-id="4cee4-149"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cee4-149"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="4cee4-150">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4cee4-150">Library</span></span><br/> | <dl> <span data-ttu-id="4cee4-151"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4cee4-151"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="4cee4-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="4cee4-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cee4-153">Funções D3DX</span><span class="sxs-lookup"><span data-stu-id="4cee4-153">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

