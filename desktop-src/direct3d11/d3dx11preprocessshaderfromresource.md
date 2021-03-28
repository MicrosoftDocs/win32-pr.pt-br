---
title: Função D3DX11PreprocessShaderFromResource (D3DX11async. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Observação em vez de usar essa função, recomendamos que você use a API D3DPreprocess. Crie um sombreador de um recurso sem compilá-lo.
ms.assetid: 13362ad6-f02e-4899-8962-4f7d4750ff69
keywords:
- Função D3DX11PreprocessShaderFromResource Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11PreprocessShaderFromResource
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 645d872e983cabbcd81aab05a59ee8f1f83cc403
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989333"
---
# <a name="d3dx11preprocessshaderfromresource-function"></a><span data-ttu-id="df6d6-106">Função D3DX11PreprocessShaderFromResource</span><span class="sxs-lookup"><span data-stu-id="df6d6-106">D3DX11PreprocessShaderFromResource function</span></span>

> [!Note]  
> <span data-ttu-id="df6d6-107">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="df6d6-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="df6d6-108">Em vez de usar essa função, recomendamos que você use a API [**D3DPreprocess**](/windows/desktop/direct3dhlsl/d3dpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="df6d6-108">Instead of using this function, we recommend that you use the [**D3DPreprocess**](/windows/desktop/direct3dhlsl/d3dpreprocess) API.</span></span>

 

<span data-ttu-id="df6d6-109">Crie um sombreador de um recurso sem compilá-lo.</span><span class="sxs-lookup"><span data-stu-id="df6d6-109">Create a shader from a resource without compiling it.</span></span>

## <a name="syntax"></a><span data-ttu-id="df6d6-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="df6d6-110">Syntax</span></span>


```C++
HRESULT D3DX11PreprocessShaderFromResource(
  _In_        HMODULE            hModule,
  _In_        LPCTSTR            pResourceName,
  _In_        LPCTSTR            pSrcFileName,
  _In_  const D3D11_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX11ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="df6d6-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="df6d6-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df6d6-112">*HMODULE* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="df6d6-112">*hModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df6d6-113">Tipo: **[ **HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="df6d6-113">Type: **[**HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="df6d6-114">Identificador para o módulo de recurso que contém o sombreador.</span><span class="sxs-lookup"><span data-stu-id="df6d6-114">Handle to the resource module containing the shader.</span></span> <span data-ttu-id="df6d6-115">HMODULE pode ser obtido com a [função GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span><span class="sxs-lookup"><span data-stu-id="df6d6-115">HMODULE can be obtained with [GetModuleHandle Function](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="df6d6-116">*origem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="df6d6-116">*pResourceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df6d6-117">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="df6d6-117">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="df6d6-118">O nome do recurso no lado hModule que contém o sombreador.</span><span class="sxs-lookup"><span data-stu-id="df6d6-118">The name of the resource in side hModule containing the shader.</span></span> <span data-ttu-id="df6d6-119">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="df6d6-119">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="df6d6-120">Caso contrário, o tipo de dados será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="df6d6-120">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="df6d6-121">*pSrcFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="df6d6-121">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df6d6-122">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="df6d6-122">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="df6d6-123">Opcional.</span><span class="sxs-lookup"><span data-stu-id="df6d6-123">Optional.</span></span> <span data-ttu-id="df6d6-124">Nome do arquivo de efeito, que é usado somente para mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="df6d6-124">Effect file name, which is used for error messages only.</span></span> <span data-ttu-id="df6d6-125">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="df6d6-125">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="df6d6-126">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="df6d6-126">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df6d6-127">Tipo: **\_ \_ macro \* do sombreador D3D11 const**</span><span class="sxs-lookup"><span data-stu-id="df6d6-127">Type: **const D3D11\_SHADER\_MACRO\***</span></span>

<span data-ttu-id="df6d6-128">Uma matriz com terminação nula de macros de sombreador; Defina como **NULL** para não especificar nenhuma macro.</span><span class="sxs-lookup"><span data-stu-id="df6d6-128">A NULL-terminated array of shader macros; set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="df6d6-129">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="df6d6-129">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df6d6-130">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="df6d6-130">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="df6d6-131">Um ponteiro para uma interface de inclusão; Defina como **NULL** para especificar que não há nenhum arquivo de inclusão.</span><span class="sxs-lookup"><span data-stu-id="df6d6-131">A pointer to an include interface; set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="df6d6-132">*pPump* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="df6d6-132">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df6d6-133">Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="df6d6-133">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="df6d6-134">Um ponteiro para uma interface de bombeamento de thread (consulte a [**interface ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="df6d6-134">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="df6d6-135">Use **NULL** para especificar que essa função não deve retornar até que seja concluída.</span><span class="sxs-lookup"><span data-stu-id="df6d6-135">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="df6d6-136">*ppShaderText* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="df6d6-136">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df6d6-137">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="df6d6-137">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="df6d6-138">Um ponteiro para a memória que contém o sombreador não compilado.</span><span class="sxs-lookup"><span data-stu-id="df6d6-138">A pointer to memory that contains the uncompiled shader.</span></span>

</dd> <dt>

<span data-ttu-id="df6d6-139">*ppErrorMsgs* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="df6d6-139">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df6d6-140">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="df6d6-140">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="df6d6-141">O endereço de um ponteiro para memória que contém erros de criação de efeito, se houver.</span><span class="sxs-lookup"><span data-stu-id="df6d6-141">The address of a pointer to memory that contains effect-creation errors, if any occurred.</span></span>

</dd> <dt>

<span data-ttu-id="df6d6-142">*pHResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="df6d6-142">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df6d6-143">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="df6d6-143">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="df6d6-144">Um ponteiro para o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="df6d6-144">A pointer to the return value.</span></span> <span data-ttu-id="df6d6-145">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="df6d6-145">May be **NULL**.</span></span> <span data-ttu-id="df6d6-146">Se *pPump* não for **NULL**, *pHResult* deverá ser um local de memória válido até que a execução assíncrona seja concluída.</span><span class="sxs-lookup"><span data-stu-id="df6d6-146">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df6d6-147">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="df6d6-147">Return value</span></span>

<span data-ttu-id="df6d6-148">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="df6d6-148">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="df6d6-149">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="df6d6-149">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="df6d6-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df6d6-150">Requirements</span></span>



| <span data-ttu-id="df6d6-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="df6d6-151">Requirement</span></span> | <span data-ttu-id="df6d6-152">Valor</span><span class="sxs-lookup"><span data-stu-id="df6d6-152">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="df6d6-153">parâmetro</span><span class="sxs-lookup"><span data-stu-id="df6d6-153">Header</span></span><br/>  | <dl> <span data-ttu-id="df6d6-154"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="df6d6-154"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="df6d6-155">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="df6d6-155">Library</span></span><br/> | <dl> <span data-ttu-id="df6d6-156"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="df6d6-156"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="df6d6-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="df6d6-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df6d6-158">Funções D3DX</span><span class="sxs-lookup"><span data-stu-id="df6d6-158">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

