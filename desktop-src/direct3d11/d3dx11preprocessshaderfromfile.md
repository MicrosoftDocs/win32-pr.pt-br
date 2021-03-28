---
title: Função D3DX11PreprocessShaderFromFile (D3DX11async. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Observação em vez de usar essa função, recomendamos que você use a API D3DPreprocess. Crie um sombreador de um arquivo sem compilá-lo.
ms.assetid: aab08efd-b6b0-44e5-bd68-f32c242d9e94
keywords:
- Função D3DX11PreprocessShaderFromFile Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11PreprocessShaderFromFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1987ef25688e83a48059805f79af4dc8a88c1ac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968621"
---
# <a name="d3dx11preprocessshaderfromfile-function"></a><span data-ttu-id="dcadf-106">Função D3DX11PreprocessShaderFromFile</span><span class="sxs-lookup"><span data-stu-id="dcadf-106">D3DX11PreprocessShaderFromFile function</span></span>

> [!Note]  
> <span data-ttu-id="dcadf-107">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="dcadf-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="dcadf-108">Em vez de usar essa função, recomendamos que você use a API [**D3DPreprocess**](/windows/desktop/direct3dhlsl/d3dpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="dcadf-108">Instead of using this function, we recommend that you use the [**D3DPreprocess**](/windows/desktop/direct3dhlsl/d3dpreprocess) API.</span></span>

 

<span data-ttu-id="dcadf-109">Crie um sombreador de um arquivo sem compilá-lo.</span><span class="sxs-lookup"><span data-stu-id="dcadf-109">Create a shader from a file without compiling it.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcadf-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dcadf-110">Syntax</span></span>


```C++
HRESULT D3DX11PreprocessShaderFromFile(
  _In_        LPCTSTR            pFileName,
  _In_  const D3D11_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX11ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="dcadf-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dcadf-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcadf-112">*pFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dcadf-112">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcadf-113">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="dcadf-113">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="dcadf-114">Nome do arquivo do sombreador.</span><span class="sxs-lookup"><span data-stu-id="dcadf-114">Name of the shader file.</span></span>

</dd> <dt>

<span data-ttu-id="dcadf-115">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dcadf-115">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcadf-116">Tipo: **\_ \_ macro \* do sombreador D3D11 const**</span><span class="sxs-lookup"><span data-stu-id="dcadf-116">Type: **const D3D11\_SHADER\_MACRO\***</span></span>

<span data-ttu-id="dcadf-117">Uma matriz com terminação nula de macros de sombreador; Defina como **NULL** para não especificar nenhuma macro.</span><span class="sxs-lookup"><span data-stu-id="dcadf-117">A NULL-terminated array of shader macros; set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="dcadf-118">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dcadf-118">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcadf-119">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="dcadf-119">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="dcadf-120">Um ponteiro para uma interface de inclusão; Defina como **NULL** para especificar que não há nenhum arquivo de inclusão.</span><span class="sxs-lookup"><span data-stu-id="dcadf-120">A pointer to an include interface; set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="dcadf-121">*pPump* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dcadf-121">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcadf-122">Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="dcadf-122">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="dcadf-123">Um ponteiro para uma interface de bombeamento de thread (consulte a [**interface ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="dcadf-123">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="dcadf-124">Use **NULL** para especificar que essa função não deve retornar até que seja concluída.</span><span class="sxs-lookup"><span data-stu-id="dcadf-124">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="dcadf-125">*ppShaderText* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="dcadf-125">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dcadf-126">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="dcadf-126">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="dcadf-127">Um ponteiro para a memória que contém o sombreador não compilado.</span><span class="sxs-lookup"><span data-stu-id="dcadf-127">A pointer to memory that contains the uncompiled shader.</span></span>

</dd> <dt>

<span data-ttu-id="dcadf-128">*ppErrorMsgs* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="dcadf-128">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dcadf-129">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="dcadf-129">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="dcadf-130">O endereço de um ponteiro para memória que contém erros de criação de efeito, se houver.</span><span class="sxs-lookup"><span data-stu-id="dcadf-130">The address of a pointer to memory that contains effect-creation errors, if any occurred.</span></span>

</dd> <dt>

<span data-ttu-id="dcadf-131">*pHResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="dcadf-131">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dcadf-132">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="dcadf-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="dcadf-133">Um ponteiro para o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="dcadf-133">A pointer to the return value.</span></span> <span data-ttu-id="dcadf-134">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="dcadf-134">May be **NULL**.</span></span> <span data-ttu-id="dcadf-135">Se *pPump* não for **NULL**, *pHResult* deverá ser um local de memória válido até que a execução assíncrona seja concluída.</span><span class="sxs-lookup"><span data-stu-id="dcadf-135">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcadf-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dcadf-136">Return value</span></span>

<span data-ttu-id="dcadf-137">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dcadf-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dcadf-138">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="dcadf-138">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dcadf-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dcadf-139">Requirements</span></span>



| <span data-ttu-id="dcadf-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcadf-140">Requirement</span></span> | <span data-ttu-id="dcadf-141">Valor</span><span class="sxs-lookup"><span data-stu-id="dcadf-141">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcadf-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dcadf-142">Header</span></span><br/>  | <dl> <span data-ttu-id="dcadf-143"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcadf-143"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="dcadf-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dcadf-144">Library</span></span><br/> | <dl> <span data-ttu-id="dcadf-145"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dcadf-145"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="dcadf-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="dcadf-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcadf-147">Funções D3DX</span><span class="sxs-lookup"><span data-stu-id="dcadf-147">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

