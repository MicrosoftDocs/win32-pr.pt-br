---
title: Função D3DX11CompileFromFile (D3DX11async. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Observação em vez de usar essa função, recomendamos que você compile offline usando o compilador de linha de comando Fxc.exe ou use uma das APIs de compilação HLSL, como a API D3DCompileFromFile. Compilar um sombreador ou um efeito de um arquivo.
ms.assetid: 91a1a339-50da-4f86-9b55-6af246a60482
keywords:
- Função D3DX11CompileFromFile Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CompileFromFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89c9194eb54652304c220e5a4de0ee12a26ea1a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104091983"
---
# <a name="d3dx11compilefromfile-function"></a><span data-ttu-id="5fcb4-106">Função D3DX11CompileFromFile</span><span class="sxs-lookup"><span data-stu-id="5fcb4-106">D3DX11CompileFromFile function</span></span>

> [!Note]  
> <span data-ttu-id="5fcb4-107">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="5fcb4-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="5fcb4-108">Em vez de usar essa função, recomendamos que você compile offline usando o compilador de linha de comando Fxc.exe ou use uma das APIs de compilação HLSL, como a API [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile) .</span><span class="sxs-lookup"><span data-stu-id="5fcb4-108">Instead of using this function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use one of the HLSL compile APIs, like the [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile) API.</span></span>

 

<span data-ttu-id="5fcb4-109">Compilar um sombreador ou um efeito de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="5fcb4-109">Compile a shader or an effect from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fcb4-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5fcb4-110">Syntax</span></span>


```C++
HRESULT D3DX11CompileFromFile(
  _In_        LPCTSTR            pSrcFile,
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



## <a name="parameters"></a><span data-ttu-id="5fcb4-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5fcb4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fcb4-112">*pSrcFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5fcb4-112">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fcb4-113">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5fcb4-113">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5fcb4-114">O nome do arquivo que contém o código do sombreador.</span><span class="sxs-lookup"><span data-stu-id="5fcb4-114">The name of the file that contains the shader code.</span></span> <span data-ttu-id="5fcb4-115">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="5fcb4-115">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="5fcb4-116">Caso contrário, o tipo de dados será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="5fcb4-116">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="5fcb4-117">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5fcb4-117">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fcb4-118">Tipo: **\* [**\_ \_ macro do sombreador d3d10**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) const**</span><span class="sxs-lookup"><span data-stu-id="5fcb4-118">Type: **const [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="5fcb4-119">Opcional.</span><span class="sxs-lookup"><span data-stu-id="5fcb4-119">Optional.</span></span> <span data-ttu-id="5fcb4-120">Ponteiro para uma matriz de definições de macro (consulte a [**\_ \_ macro do sombreador d3d10**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span><span class="sxs-lookup"><span data-stu-id="5fcb4-120">Pointer to an array of macro definitions (see [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span></span> <span data-ttu-id="5fcb4-121">A última estrutura na matriz serve como um terminador e deve ter todos os membros definidos como 0.</span><span class="sxs-lookup"><span data-stu-id="5fcb4-121">The last structure in the array serves as a terminator and must have all members set to 0.</span></span> <span data-ttu-id="5fcb4-122">Se não for usado, defina *pDefines* como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="5fcb4-122">If not used, set *pDefines* to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5fcb4-123">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5fcb4-123">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fcb4-124">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="5fcb4-124">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="5fcb4-125">Opcional.</span><span class="sxs-lookup"><span data-stu-id="5fcb4-125">Optional.</span></span> <span data-ttu-id="5fcb4-126">Ponteiro para uma interface para manipulação de arquivos de inclusão.</span><span class="sxs-lookup"><span data-stu-id="5fcb4-126">Pointer to an interface for handling include files.</span></span> <span data-ttu-id="5fcb4-127">Definir isso como **NULL** causará um erro de compilação se um sombreador contiver um \# include.</span><span class="sxs-lookup"><span data-stu-id="5fcb4-127">Setting this to **NULL** will cause a compile error if a shader contains a \#include.</span></span>

</dd> <dt>

<span data-ttu-id="5fcb4-128">*pFunctionName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5fcb4-128">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fcb4-129">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5fcb4-129">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5fcb4-130">Nome da função de ponto de entrada do sombreador em que começa a execução do sombreador.</span><span class="sxs-lookup"><span data-stu-id="5fcb4-130">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="5fcb4-131">Quando você compila um efeito, o **D3DX11CompileFromFile** ignora *pFunctionName*; Recomendamos que você defina *pFunctionName* como **NULL** porque é uma boa prática de programação definir um parâmetro de ponteiro como **nulo** se a função chamada não o usar.</span><span class="sxs-lookup"><span data-stu-id="5fcb4-131">When you compile an effect, **D3DX11CompileFromFile** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="5fcb4-132">*pProfile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5fcb4-132">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fcb4-133">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5fcb4-133">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5fcb4-134">Uma cadeia de caracteres que especifica o modelo de sombreador; pode ser qualquer perfil no sombreador modelo 2, o Shader Model 3, o Shader Model 4 ou o Shader Model 5.</span><span class="sxs-lookup"><span data-stu-id="5fcb4-134">A string that specifies the shader model; can be any profile in shader model 2, shader model 3, shader model 4, or shader model 5.</span></span> <span data-ttu-id="5fcb4-135">O perfil também pode ser para o tipo de efeito (por exemplo, FX \_ 4 \_ 1).</span><span class="sxs-lookup"><span data-stu-id="5fcb4-135">The profile can also be for effect type (for example, fx\_4\_1).</span></span>

</dd> <dt>

<span data-ttu-id="5fcb4-136">*Flags1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5fcb4-136">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fcb4-137">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5fcb4-137">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5fcb4-138">[**Sinalizadores de compilação**](/windows/desktop/direct3dhlsl/d3dcompile-constants)de sombreador.</span><span class="sxs-lookup"><span data-stu-id="5fcb4-138">Shader [**compile flags**](/windows/desktop/direct3dhlsl/d3dcompile-constants).</span></span>

</dd> <dt>

<span data-ttu-id="5fcb4-139">*Flags2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5fcb4-139">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fcb4-140">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5fcb4-140">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5fcb4-141">[**Sinalizadores de compilação**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants)de efeito.</span><span class="sxs-lookup"><span data-stu-id="5fcb4-141">Effect [**compile flags**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants).</span></span> <span data-ttu-id="5fcb4-142">Quando você compila um sombreador e não um arquivo de efeito, o **D3DX11CompileFromFile** ignora *Flags2*; é recomendável que você defina *Flags2* como zero porque é uma boa prática de programação definir um parâmetro não-de-ponto como zero se a função chamada não for usá-lo.</span><span class="sxs-lookup"><span data-stu-id="5fcb4-142">When you compile a shader and not an effect file, **D3DX11CompileFromFile** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="5fcb4-143">*pPump* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5fcb4-143">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fcb4-144">Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="5fcb4-144">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="5fcb4-145">Um ponteiro para uma interface de bombeamento de thread (consulte a [**interface ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="5fcb4-145">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="5fcb4-146">Use **NULL** para especificar que essa função não deve retornar até que seja concluída.</span><span class="sxs-lookup"><span data-stu-id="5fcb4-146">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="5fcb4-147">*ppShader* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5fcb4-147">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5fcb4-148">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="5fcb4-148">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="5fcb4-149">Um ponteiro para a memória que contém o sombreador compilado, bem como qualquer informação de depuração e tabela de símbolos inserida.</span><span class="sxs-lookup"><span data-stu-id="5fcb4-149">A pointer to memory which contains the compiled shader, as well as any embedded debug and symbol-table information.</span></span>

</dd> <dt>

<span data-ttu-id="5fcb4-150">*ppErrorMsgs* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5fcb4-150">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5fcb4-151">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="5fcb4-151">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="5fcb4-152">Um ponteiro para memória que contém uma lista de erros e avisos ocorridos durante a compilação.</span><span class="sxs-lookup"><span data-stu-id="5fcb4-152">A pointer to memory which contains a listing of errors and warnings that occurred during compilation.</span></span> <span data-ttu-id="5fcb4-153">Esses erros e avisos são idênticos à saída de depuração de um depurador.</span><span class="sxs-lookup"><span data-stu-id="5fcb4-153">These errors and warnings are identical to the debug output from a debugger.</span></span>

</dd> <dt>

<span data-ttu-id="5fcb4-154">*pHResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5fcb4-154">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5fcb4-155">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="5fcb4-155">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="5fcb4-156">Um ponteiro para o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="5fcb4-156">A pointer to the return value.</span></span> <span data-ttu-id="5fcb4-157">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="5fcb4-157">May be **NULL**.</span></span> <span data-ttu-id="5fcb4-158">Se *pPump* não for **NULL**, *pHResult* deverá ser um local de memória válido até que a execução assíncrona seja concluída.</span><span class="sxs-lookup"><span data-stu-id="5fcb4-158">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fcb4-159">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5fcb4-159">Return value</span></span>

<span data-ttu-id="5fcb4-160">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5fcb4-160">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5fcb4-161">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="5fcb4-161">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

<span data-ttu-id="5fcb4-162">**D3DX11CompileFromFile** retornará E \_ INVALIDARG se você fornecer um valor não **nulo** ao parâmetro *pHResult* quando fornecer **NULL** para o parâmetro *pPump* .</span><span class="sxs-lookup"><span data-stu-id="5fcb4-162">**D3DX11CompileFromFile** returns E\_INVALIDARG if you supply a non-**NULL** value to the *pHResult* parameter when you supply **NULL** to the *pPump* parameter.</span></span> <span data-ttu-id="5fcb4-163">Para obter mais informações sobre essa situação, consulte comentários.</span><span class="sxs-lookup"><span data-stu-id="5fcb4-163">For more information about this situation, see Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="5fcb4-164">Comentários</span><span class="sxs-lookup"><span data-stu-id="5fcb4-164">Remarks</span></span>

<span data-ttu-id="5fcb4-165">Para obter mais informações sobre **D3DX11CompileFromFile**, consulte [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).</span><span class="sxs-lookup"><span data-stu-id="5fcb4-165">For more information about **D3DX11CompileFromFile**, see [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).</span></span>

<span data-ttu-id="5fcb4-166">Você deve fornecer **NULL** para o parâmetro *pHResult* se também fornecer **NULL** para o parâmetro *pPump* .</span><span class="sxs-lookup"><span data-stu-id="5fcb4-166">You must supply **NULL** to the *pHResult* parameter if you also supply **NULL** to the *pPump* parameter.</span></span> <span data-ttu-id="5fcb4-167">Caso contrário, você não pode criar um sombreador usando o código do sombreador compilado que o **D3DX11CompileFromFile** retorna na memória à qual o parâmetro *ppShader* aponta.</span><span class="sxs-lookup"><span data-stu-id="5fcb4-167">Otherwise, you cannot create a shader by using the compiled shader code that **D3DX11CompileFromFile** returns in the memory that the *ppShader* parameter points to.</span></span> <span data-ttu-id="5fcb4-168">Para criar um sombreador do código de sombreador compatível, você chama um dos seguintes métodos de interface [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) :</span><span class="sxs-lookup"><span data-stu-id="5fcb4-168">To create a shader from complied shader code, you call one of the following [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) interface methods:</span></span>

-   [<span data-ttu-id="5fcb4-169">**CreateComputeShader**</span><span class="sxs-lookup"><span data-stu-id="5fcb4-169">**CreateComputeShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createcomputeshader)
-   [<span data-ttu-id="5fcb4-170">**CreateDomainShader**</span><span class="sxs-lookup"><span data-stu-id="5fcb4-170">**CreateDomainShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)
-   [<span data-ttu-id="5fcb4-171">**CreateGeometryShader**</span><span class="sxs-lookup"><span data-stu-id="5fcb4-171">**CreateGeometryShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshader)
-   [<span data-ttu-id="5fcb4-172">**CreateGeometryShaderWithStreamOutput**</span><span class="sxs-lookup"><span data-stu-id="5fcb4-172">**CreateGeometryShaderWithStreamOutput**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)
-   [<span data-ttu-id="5fcb4-173">**CreateHullShader**</span><span class="sxs-lookup"><span data-stu-id="5fcb4-173">**CreateHullShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)
-   [<span data-ttu-id="5fcb4-174">**CreatePixelShader**</span><span class="sxs-lookup"><span data-stu-id="5fcb4-174">**CreatePixelShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createpixelshader)
-   [<span data-ttu-id="5fcb4-175">**CreateVertexShader**</span><span class="sxs-lookup"><span data-stu-id="5fcb4-175">**CreateVertexShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)

<span data-ttu-id="5fcb4-176">Além disso, se você fornecer um valor não **nulo** para *pHResult* quando você fornecer **NULL** para *pPump*, **D3DX11CompileFromFile** retornará o código de \_ erro E INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="5fcb4-176">In addition, if you supply a non-**NULL** value to *pHResult* when you supply **NULL** to *pPump*, **D3DX11CompileFromFile** returns the E\_INVALIDARG error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fcb4-177">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5fcb4-177">Requirements</span></span>



| <span data-ttu-id="5fcb4-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fcb4-178">Requirement</span></span> | <span data-ttu-id="5fcb4-179">Valor</span><span class="sxs-lookup"><span data-stu-id="5fcb4-179">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fcb4-180">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5fcb4-180">Header</span></span><br/>  | <dl> <span data-ttu-id="5fcb4-181"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fcb4-181"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="5fcb4-182">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5fcb4-182">Library</span></span><br/> | <dl> <span data-ttu-id="5fcb4-183"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5fcb4-183"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="5fcb4-184">Confira também</span><span class="sxs-lookup"><span data-stu-id="5fcb4-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fcb4-185">Funções D3DX</span><span class="sxs-lookup"><span data-stu-id="5fcb4-185">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

