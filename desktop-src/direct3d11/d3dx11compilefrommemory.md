---
title: Função D3DX11CompileFromMemory (D3DX11async. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Observação em vez de usar essa função, recomendamos que você compile offline usando o compilador de linha de comando Fxc.exe ou use uma das APIs de compilação HLSL, como a API D3DCompile. Compile um sombreador ou um efeito que é carregado na memória.
ms.assetid: 3396560f-f411-4c66-9f22-03c0050c74b0
keywords:
- Função D3DX11CompileFromMemory Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CompileFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e10590c3db458a23bf4d52b6507146884630087
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968634"
---
# <a name="d3dx11compilefrommemory-function"></a><span data-ttu-id="eec2b-106">Função D3DX11CompileFromMemory</span><span class="sxs-lookup"><span data-stu-id="eec2b-106">D3DX11CompileFromMemory function</span></span>

> [!Note]  
> <span data-ttu-id="eec2b-107">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="eec2b-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="eec2b-108">Em vez de usar essa função, recomendamos que você compile offline usando o compilador de linha de comando Fxc.exe ou use uma das APIs de compilação HLSL, como a API [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) .</span><span class="sxs-lookup"><span data-stu-id="eec2b-108">Instead of using this function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use one of the HLSL compile APIs, like the [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) API.</span></span>

 

<span data-ttu-id="eec2b-109">Compile um sombreador ou um efeito que é carregado na memória.</span><span class="sxs-lookup"><span data-stu-id="eec2b-109">Compile a shader or an effect that is loaded in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="eec2b-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eec2b-110">Syntax</span></span>


```C++
HRESULT D3DX11CompileFromMemory(
  _In_        LPCSTR             pSrcData,
  _In_        SIZE_T             SrcDataLen,
  _In_        LPCSTR             pFileName,
  _In_  const D3D10_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        LPCSTR             pFunctionName,
  _In_        LPCSTR             pProfile,
  _In_        UINT               Flags1,
  _In_        UINT               Flags2,
  _In_        ID3DX11ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShader,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="eec2b-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eec2b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eec2b-112">*pSrcData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="eec2b-112">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eec2b-113">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="eec2b-113">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="eec2b-114">Ponteiro para o sombreador na memória.</span><span class="sxs-lookup"><span data-stu-id="eec2b-114">Pointer to the shader in memory.</span></span>

</dd> <dt>

<span data-ttu-id="eec2b-115">*SrcDataLen* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="eec2b-115">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eec2b-116">Tipo: **[ **tamanho \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="eec2b-116">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="eec2b-117">Tamanho do sombreador na memória.</span><span class="sxs-lookup"><span data-stu-id="eec2b-117">Size of the shader in memory.</span></span>

</dd> <dt>

<span data-ttu-id="eec2b-118">*pFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="eec2b-118">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eec2b-119">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="eec2b-119">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="eec2b-120">O nome do arquivo que contém o código do sombreador.</span><span class="sxs-lookup"><span data-stu-id="eec2b-120">The name of the file that contains the shader code.</span></span>

</dd> <dt>

<span data-ttu-id="eec2b-121">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="eec2b-121">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eec2b-122">Tipo: **\* [**\_ \_ macro do sombreador d3d10**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) const**</span><span class="sxs-lookup"><span data-stu-id="eec2b-122">Type: **const [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="eec2b-123">Opcional.</span><span class="sxs-lookup"><span data-stu-id="eec2b-123">Optional.</span></span> <span data-ttu-id="eec2b-124">Ponteiro para uma matriz de definições de macro (consulte a [**\_ \_ macro do sombreador d3d10**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span><span class="sxs-lookup"><span data-stu-id="eec2b-124">Pointer to an array of macro definitions (see [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span></span> <span data-ttu-id="eec2b-125">A última estrutura na matriz serve como um terminador e deve ter todos os membros definidos como 0.</span><span class="sxs-lookup"><span data-stu-id="eec2b-125">The last structure in the array serves as a terminator and must have all members set to 0.</span></span> <span data-ttu-id="eec2b-126">Se não for usado, defina *pDefines* como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="eec2b-126">If not used, set *pDefines* to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="eec2b-127">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="eec2b-127">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eec2b-128">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="eec2b-128">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="eec2b-129">Opcional.</span><span class="sxs-lookup"><span data-stu-id="eec2b-129">Optional.</span></span> <span data-ttu-id="eec2b-130">Ponteiro para uma interface para manipulação de arquivos de inclusão.</span><span class="sxs-lookup"><span data-stu-id="eec2b-130">Pointer to an interface for handling include files.</span></span> <span data-ttu-id="eec2b-131">Definir isso como **NULL** causará um erro de compilação se um sombreador contiver um \# include.</span><span class="sxs-lookup"><span data-stu-id="eec2b-131">Setting this to **NULL** will cause a compile error if a shader contains a \#include.</span></span>

</dd> <dt>

<span data-ttu-id="eec2b-132">*pFunctionName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="eec2b-132">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eec2b-133">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="eec2b-133">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="eec2b-134">Nome da função de ponto de entrada do sombreador em que começa a execução do sombreador.</span><span class="sxs-lookup"><span data-stu-id="eec2b-134">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="eec2b-135">Quando você compila um efeito, o **D3DX11CompileFromMemory** ignora *pFunctionName*; Recomendamos que você defina *pFunctionName* como **NULL** porque é uma boa prática de programação definir um parâmetro de ponteiro como **nulo** se a função chamada não o usar.</span><span class="sxs-lookup"><span data-stu-id="eec2b-135">When you compile an effect, **D3DX11CompileFromMemory** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="eec2b-136">*pProfile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="eec2b-136">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eec2b-137">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="eec2b-137">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="eec2b-138">Uma cadeia de caracteres que especifica o modelo de sombreador; pode ser qualquer perfil no sombreador modelo 2, o Shader Model 3, o Shader Model 4 ou o Shader Model 5.</span><span class="sxs-lookup"><span data-stu-id="eec2b-138">A string that specifies the shader model; can be any profile in shader model 2, shader model 3, shader model 4, or shader model 5.</span></span> <span data-ttu-id="eec2b-139">O perfil também pode ser para o tipo de efeito (por exemplo, FX \_ 4 \_ 1).</span><span class="sxs-lookup"><span data-stu-id="eec2b-139">The profile can also be for effect type (for example, fx\_4\_1).</span></span>

</dd> <dt>

<span data-ttu-id="eec2b-140">*Flags1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="eec2b-140">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eec2b-141">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="eec2b-141">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="eec2b-142">[**Sinalizadores de compilação**](/windows/desktop/direct3dhlsl/d3dcompile-constants)de sombreador.</span><span class="sxs-lookup"><span data-stu-id="eec2b-142">Shader [**compile flags**](/windows/desktop/direct3dhlsl/d3dcompile-constants).</span></span>

</dd> <dt>

<span data-ttu-id="eec2b-143">*Flags2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="eec2b-143">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eec2b-144">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="eec2b-144">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="eec2b-145">[**Sinalizadores de compilação**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants)de efeito.</span><span class="sxs-lookup"><span data-stu-id="eec2b-145">Effect [**compile flags**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants).</span></span> <span data-ttu-id="eec2b-146">Quando você compila um sombreador e não um arquivo de efeito, o **D3DX11CompileFromMemory** ignora *Flags2*; é recomendável que você defina *Flags2* como zero porque é uma boa prática de programação definir um parâmetro não-de-ponto como zero se a função chamada não for usá-lo.</span><span class="sxs-lookup"><span data-stu-id="eec2b-146">When you compile a shader and not an effect file, **D3DX11CompileFromMemory** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="eec2b-147">*pPump* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="eec2b-147">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eec2b-148">Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="eec2b-148">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="eec2b-149">Um ponteiro para uma interface de bombeamento de thread (consulte a [**interface ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="eec2b-149">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="eec2b-150">Use **NULL** para especificar que essa função não deve retornar até que seja concluída.</span><span class="sxs-lookup"><span data-stu-id="eec2b-150">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="eec2b-151">*ppShader* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="eec2b-151">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eec2b-152">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="eec2b-152">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="eec2b-153">Um ponteiro para a memória que contém o sombreador compilado, bem como qualquer informação de depuração e tabela de símbolos inserida.</span><span class="sxs-lookup"><span data-stu-id="eec2b-153">A pointer to memory which contains the compiled shader, as well as any embedded debug and symbol-table information.</span></span>

</dd> <dt>

<span data-ttu-id="eec2b-154">*ppErrorMsgs* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="eec2b-154">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eec2b-155">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="eec2b-155">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="eec2b-156">Um ponteiro para memória que contém uma lista de erros e avisos ocorridos durante a compilação.</span><span class="sxs-lookup"><span data-stu-id="eec2b-156">A pointer to memory which contains a listing of errors and warnings that occurred during compilation.</span></span> <span data-ttu-id="eec2b-157">Esses erros e avisos são idênticos à saída de depuração de um depurador.</span><span class="sxs-lookup"><span data-stu-id="eec2b-157">These errors and warnings are identical to the debug output from a debugger.</span></span>

</dd> <dt>

<span data-ttu-id="eec2b-158">*pHResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="eec2b-158">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eec2b-159">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="eec2b-159">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="eec2b-160">Um ponteiro para o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="eec2b-160">A pointer to the return value.</span></span> <span data-ttu-id="eec2b-161">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="eec2b-161">May be **NULL**.</span></span> <span data-ttu-id="eec2b-162">Se *pPump* não for **NULL**, *pHResult* deverá ser um local de memória válido até que a execução assíncrona seja concluída.</span><span class="sxs-lookup"><span data-stu-id="eec2b-162">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eec2b-163">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eec2b-163">Return value</span></span>

<span data-ttu-id="eec2b-164">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="eec2b-164">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="eec2b-165">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="eec2b-165">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

<span data-ttu-id="eec2b-166">**D3DX11CompileFromMemory** retornará E \_ INVALIDARG se você fornecer não **nulo** ao parâmetro *pHResult* quando fornecer **NULL** para o parâmetro *pPump* .</span><span class="sxs-lookup"><span data-stu-id="eec2b-166">**D3DX11CompileFromMemory** returns E\_INVALIDARG if you supply non-**NULL** to the *pHResult* parameter when you supply **NULL** to the *pPump* parameter.</span></span> <span data-ttu-id="eec2b-167">Para obter mais informações sobre essa situação, consulte comentários.</span><span class="sxs-lookup"><span data-stu-id="eec2b-167">For more information about this situation, see Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="eec2b-168">Comentários</span><span class="sxs-lookup"><span data-stu-id="eec2b-168">Remarks</span></span>

<span data-ttu-id="eec2b-169">Para obter mais informações sobre **D3DX11CompileFromMemory**, consulte [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).</span><span class="sxs-lookup"><span data-stu-id="eec2b-169">For more information about **D3DX11CompileFromMemory**, see [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).</span></span>

<span data-ttu-id="eec2b-170">Você deve fornecer **NULL** para o parâmetro *pHResult* se também fornecer **NULL** para o parâmetro *pPump* .</span><span class="sxs-lookup"><span data-stu-id="eec2b-170">You must supply **NULL** to the *pHResult* parameter if you also supply **NULL** to the *pPump* parameter.</span></span> <span data-ttu-id="eec2b-171">Caso contrário, você não poderá criar um sombreador subsequentemente usando o código do sombreador compilado que o **D3DX11CompileFromMemory** retorna na memória à qual o parâmetro *ppShader* aponta.</span><span class="sxs-lookup"><span data-stu-id="eec2b-171">Otherwise, you cannot subsequently create a shader by using the compiled shader code that **D3DX11CompileFromMemory** returns in the memory that the *ppShader* parameter points to.</span></span> <span data-ttu-id="eec2b-172">Para criar um sombreador do código de sombreador compatível, você chama um dos seguintes métodos de interface [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) :</span><span class="sxs-lookup"><span data-stu-id="eec2b-172">To create a shader from complied shader code, you call one of the following [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) interface methods:</span></span>

-   [<span data-ttu-id="eec2b-173">**CreateComputeShader**</span><span class="sxs-lookup"><span data-stu-id="eec2b-173">**CreateComputeShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createcomputeshader)
-   [<span data-ttu-id="eec2b-174">**CreateDomainShader**</span><span class="sxs-lookup"><span data-stu-id="eec2b-174">**CreateDomainShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)
-   [<span data-ttu-id="eec2b-175">**CreateGeometryShader**</span><span class="sxs-lookup"><span data-stu-id="eec2b-175">**CreateGeometryShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshader)
-   [<span data-ttu-id="eec2b-176">**CreateGeometryShaderWithStreamOutput**</span><span class="sxs-lookup"><span data-stu-id="eec2b-176">**CreateGeometryShaderWithStreamOutput**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)
-   [<span data-ttu-id="eec2b-177">**CreateHullShader**</span><span class="sxs-lookup"><span data-stu-id="eec2b-177">**CreateHullShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)
-   [<span data-ttu-id="eec2b-178">**CreatePixelShader**</span><span class="sxs-lookup"><span data-stu-id="eec2b-178">**CreatePixelShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createpixelshader)
-   [<span data-ttu-id="eec2b-179">**CreateVertexShader**</span><span class="sxs-lookup"><span data-stu-id="eec2b-179">**CreateVertexShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)

<span data-ttu-id="eec2b-180">Além disso, se você fornecer um valor não **nulo** para *pHResult* quando você fornecer **NULL** para *pPump*, **D3DX11CompileFromMemory** retornará o código de \_ erro E INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="eec2b-180">In addition, if you supply a non-**NULL** value to *pHResult* when you supply **NULL** to *pPump*, **D3DX11CompileFromMemory** returns the E\_INVALIDARG error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="eec2b-181">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eec2b-181">Requirements</span></span>



| <span data-ttu-id="eec2b-182">Requisito</span><span class="sxs-lookup"><span data-stu-id="eec2b-182">Requirement</span></span> | <span data-ttu-id="eec2b-183">Valor</span><span class="sxs-lookup"><span data-stu-id="eec2b-183">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="eec2b-184">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eec2b-184">Header</span></span><br/>  | <dl> <span data-ttu-id="eec2b-185"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="eec2b-185"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="eec2b-186">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eec2b-186">Library</span></span><br/> | <dl> <span data-ttu-id="eec2b-187"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eec2b-187"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="eec2b-188">Confira também</span><span class="sxs-lookup"><span data-stu-id="eec2b-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eec2b-189">Funções D3DX</span><span class="sxs-lookup"><span data-stu-id="eec2b-189">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

