---
title: Função D3DX11CompileFromResource (D3DX11async. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Observação em vez de usar essa função, recomendamos que você use funções de recurso e, em seguida, compile offline usando o compilador de linha de comando Fxc.exe ou use uma das APIs de compilação HLSL, como a API D3DCompile. Compilar um sombreador ou um efeito de um recurso.
ms.assetid: ececa469-f5e3-4cb3-befe-0ed1a5a57671
keywords:
- Função D3DX11CompileFromResource Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CompileFromResource
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b26eeb825a1d3b6bcda9f77eae24c99c3cec168b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930678"
---
# <a name="d3dx11compilefromresource-function"></a><span data-ttu-id="d138b-106">Função D3DX11CompileFromResource</span><span class="sxs-lookup"><span data-stu-id="d138b-106">D3DX11CompileFromResource function</span></span>

> [!Note]  
> <span data-ttu-id="d138b-107">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="d138b-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="d138b-108">Em vez de usar essa função, recomendamos que você use [funções de recurso](/windows/desktop/menurc/resources-functions)e, em seguida, compile offline usando o compilador de linha de comando Fxc.exe ou use uma das APIs de compilação HLSL, como a API [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) .</span><span class="sxs-lookup"><span data-stu-id="d138b-108">Instead of using this function, we recommend that you use [resource functions](/windows/desktop/menurc/resources-functions), then compile offline by using the Fxc.exe command-line compiler or use one of the HLSL compile APIs, like the [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) API.</span></span>

 

<span data-ttu-id="d138b-109">Compilar um sombreador ou um efeito de um recurso.</span><span class="sxs-lookup"><span data-stu-id="d138b-109">Compile a shader or an effect from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="d138b-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d138b-110">Syntax</span></span>


```C++
HRESULT D3DX11CompileFromResource(
  _In_        HMODULE            hSrcModule,
  _In_        LPCTSTR            pSrcResource,
  _In_        LPCTSTR            pSrcFileName,
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



## <a name="parameters"></a><span data-ttu-id="d138b-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d138b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d138b-112">*hSrcModule* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d138b-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d138b-113">Tipo: **[ **HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d138b-113">Type: **[**HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d138b-114">Identificador para o módulo de recurso que contém o sombreador.</span><span class="sxs-lookup"><span data-stu-id="d138b-114">Handle to the resource module containing the shader.</span></span> <span data-ttu-id="d138b-115">HMODULE pode ser obtido com a [função GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span><span class="sxs-lookup"><span data-stu-id="d138b-115">HMODULE can be obtained with [GetModuleHandle Function](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="d138b-116">*pSrcResource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d138b-116">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d138b-117">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d138b-117">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d138b-118">Nome do recurso que contém o sombreador.</span><span class="sxs-lookup"><span data-stu-id="d138b-118">Name of the resource containing the shader.</span></span> <span data-ttu-id="d138b-119">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="d138b-119">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="d138b-120">Caso contrário, o tipo de dados será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="d138b-120">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="d138b-121">*pSrcFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d138b-121">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d138b-122">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d138b-122">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d138b-123">Opcional.</span><span class="sxs-lookup"><span data-stu-id="d138b-123">Optional.</span></span> <span data-ttu-id="d138b-124">Nome do arquivo de efeito, que é usado somente para mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="d138b-124">Effect file name, which is used for error messages only.</span></span> <span data-ttu-id="d138b-125">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d138b-125">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d138b-126">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d138b-126">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d138b-127">Tipo: **\* [**\_ \_ macro do sombreador d3d10**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) const**</span><span class="sxs-lookup"><span data-stu-id="d138b-127">Type: **const [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="d138b-128">Opcional.</span><span class="sxs-lookup"><span data-stu-id="d138b-128">Optional.</span></span> <span data-ttu-id="d138b-129">Ponteiro para uma matriz de definições de macro (consulte a [**\_ \_ macro do sombreador d3d10**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span><span class="sxs-lookup"><span data-stu-id="d138b-129">Pointer to an array of macro definitions (see [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span></span> <span data-ttu-id="d138b-130">A última estrutura na matriz serve como um terminador e deve ter todos os membros definidos como 0.</span><span class="sxs-lookup"><span data-stu-id="d138b-130">The last structure in the array serves as a terminator and must have all members set to 0.</span></span> <span data-ttu-id="d138b-131">Se não for usado, defina *pDefines* como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="d138b-131">If not used, set *pDefines* to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d138b-132">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d138b-132">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d138b-133">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="d138b-133">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="d138b-134">Opcional.</span><span class="sxs-lookup"><span data-stu-id="d138b-134">Optional.</span></span> <span data-ttu-id="d138b-135">Ponteiro para uma interface para manipulação de arquivos de inclusão.</span><span class="sxs-lookup"><span data-stu-id="d138b-135">Pointer to an interface for handling include files.</span></span> <span data-ttu-id="d138b-136">Definir isso como **NULL** causará um erro de compilação se um sombreador contiver um \# include.</span><span class="sxs-lookup"><span data-stu-id="d138b-136">Setting this to **NULL** will cause a compile error if a shader contains a \#include.</span></span>

</dd> <dt>

<span data-ttu-id="d138b-137">*pFunctionName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d138b-137">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d138b-138">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d138b-138">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d138b-139">Nome da função de ponto de entrada do sombreador em que começa a execução do sombreador.</span><span class="sxs-lookup"><span data-stu-id="d138b-139">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="d138b-140">Quando você compila um efeito, o **D3DX11CompileFromResource** ignora *pFunctionName*; Recomendamos que você defina *pFunctionName* como **NULL** porque é uma boa prática de programação definir um parâmetro de ponteiro como **nulo** se a função chamada não o usar.</span><span class="sxs-lookup"><span data-stu-id="d138b-140">When you compile an effect, **D3DX11CompileFromResource** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="d138b-141">*pProfile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d138b-141">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d138b-142">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d138b-142">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d138b-143">Uma cadeia de caracteres que especifica o modelo de sombreador; pode ser qualquer perfil no sombreador modelo 2, o Shader Model 3, o Shader Model 4 ou o Shader Model 5.</span><span class="sxs-lookup"><span data-stu-id="d138b-143">A string that specifies the shader model; can be any profile in shader model 2, shader model 3, shader model 4, or shader model 5.</span></span> <span data-ttu-id="d138b-144">O perfil também pode ser para o tipo de efeito (por exemplo, FX \_ 4 \_ 1).</span><span class="sxs-lookup"><span data-stu-id="d138b-144">The profile can also be for effect type (for example, fx\_4\_1).</span></span>

</dd> <dt>

<span data-ttu-id="d138b-145">*Flags1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d138b-145">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d138b-146">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d138b-146">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d138b-147">[**Sinalizadores de compilação**](/windows/desktop/direct3dhlsl/d3dcompile-constants)de sombreador.</span><span class="sxs-lookup"><span data-stu-id="d138b-147">Shader [**compile flags**](/windows/desktop/direct3dhlsl/d3dcompile-constants).</span></span>

</dd> <dt>

<span data-ttu-id="d138b-148">*Flags2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d138b-148">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d138b-149">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d138b-149">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d138b-150">[**Sinalizadores de compilação**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants)de efeito.</span><span class="sxs-lookup"><span data-stu-id="d138b-150">Effect [**compile flags**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants).</span></span> <span data-ttu-id="d138b-151">Quando você compila um sombreador e não um arquivo de efeito, o **D3DX11CompileFromResource** ignora *Flags2*; é recomendável que você defina *Flags2* como zero porque é uma boa prática de programação definir um parâmetro não-de-ponto como zero se a função chamada não for usá-lo.</span><span class="sxs-lookup"><span data-stu-id="d138b-151">When you compile a shader and not an effect file, **D3DX11CompileFromResource** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="d138b-152">*pPump* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d138b-152">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d138b-153">Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="d138b-153">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="d138b-154">Um ponteiro para uma interface de bombeamento de thread (consulte a [**interface ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="d138b-154">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="d138b-155">Use **NULL** para especificar que essa função não deve retornar até que seja concluída.</span><span class="sxs-lookup"><span data-stu-id="d138b-155">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="d138b-156">*ppShader* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d138b-156">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d138b-157">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="d138b-157">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="d138b-158">Um ponteiro para a memória que contém o sombreador compilado, bem como qualquer informação de depuração e tabela de símbolos inserida.</span><span class="sxs-lookup"><span data-stu-id="d138b-158">A pointer to memory which contains the compiled shader, as well as any embedded debug and symbol-table information.</span></span>

</dd> <dt>

<span data-ttu-id="d138b-159">*ppErrorMsgs* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d138b-159">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d138b-160">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="d138b-160">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="d138b-161">Um ponteiro para memória que contém uma lista de erros e avisos ocorridos durante a compilação.</span><span class="sxs-lookup"><span data-stu-id="d138b-161">A pointer to memory which contains a listing of errors and warnings that occurred during compilation.</span></span> <span data-ttu-id="d138b-162">Esses erros e avisos são idênticos à saída de depuração de um depurador.</span><span class="sxs-lookup"><span data-stu-id="d138b-162">These errors and warnings are identical to the debug output from a debugger.</span></span>

</dd> <dt>

<span data-ttu-id="d138b-163">*pHResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d138b-163">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d138b-164">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="d138b-164">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="d138b-165">Um ponteiro para o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="d138b-165">A pointer to the return value.</span></span> <span data-ttu-id="d138b-166">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d138b-166">May be **NULL**.</span></span> <span data-ttu-id="d138b-167">Se *pPump* não for **NULL**, *pHResult* deverá ser um local de memória válido até que a execução assíncrona seja concluída.</span><span class="sxs-lookup"><span data-stu-id="d138b-167">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d138b-168">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d138b-168">Return value</span></span>

<span data-ttu-id="d138b-169">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d138b-169">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d138b-170">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="d138b-170">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

<span data-ttu-id="d138b-171">**D3DX11CompileFromResource** retornará E \_ INVALIDARG se você fornecer não **nulo** ao parâmetro *pHResult* quando fornecer **NULL** para o parâmetro *pPump* .</span><span class="sxs-lookup"><span data-stu-id="d138b-171">**D3DX11CompileFromResource** returns E\_INVALIDARG if you supply non-**NULL** to the *pHResult* parameter when you supply **NULL** to the *pPump* parameter.</span></span> <span data-ttu-id="d138b-172">Para obter mais informações sobre essa situação, consulte comentários.</span><span class="sxs-lookup"><span data-stu-id="d138b-172">For more information about this situation, see Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="d138b-173">Comentários</span><span class="sxs-lookup"><span data-stu-id="d138b-173">Remarks</span></span>

<span data-ttu-id="d138b-174">Para obter mais informações sobre **D3DX11CompileFromResource**, consulte [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).</span><span class="sxs-lookup"><span data-stu-id="d138b-174">For more information about **D3DX11CompileFromResource**, see [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).</span></span>

<span data-ttu-id="d138b-175">Você deve fornecer **NULL** para o parâmetro *pHResult* se também fornecer **NULL** para o parâmetro *pPump* .</span><span class="sxs-lookup"><span data-stu-id="d138b-175">You must supply **NULL** to the *pHResult* parameter if you also supply **NULL** to the *pPump* parameter.</span></span> <span data-ttu-id="d138b-176">Caso contrário, você não poderá criar um sombreador subsequentemente usando o código do sombreador compilado que o **D3DX11CompileFromResource** retorna na memória à qual o parâmetro *ppShader* aponta.</span><span class="sxs-lookup"><span data-stu-id="d138b-176">Otherwise, you cannot subsequently create a shader by using the compiled shader code that **D3DX11CompileFromResource** returns in the memory that the *ppShader* parameter points to.</span></span> <span data-ttu-id="d138b-177">Para criar um sombreador do código de sombreador compatível, você chama um dos seguintes métodos de interface [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) :</span><span class="sxs-lookup"><span data-stu-id="d138b-177">To create a shader from complied shader code, you call one of the following [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) interface methods:</span></span>

-   [<span data-ttu-id="d138b-178">**CreateComputeShader**</span><span class="sxs-lookup"><span data-stu-id="d138b-178">**CreateComputeShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createcomputeshader)
-   [<span data-ttu-id="d138b-179">**CreateDomainShader**</span><span class="sxs-lookup"><span data-stu-id="d138b-179">**CreateDomainShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)
-   [<span data-ttu-id="d138b-180">**CreateGeometryShader**</span><span class="sxs-lookup"><span data-stu-id="d138b-180">**CreateGeometryShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshader)
-   [<span data-ttu-id="d138b-181">**CreateGeometryShaderWithStreamOutput**</span><span class="sxs-lookup"><span data-stu-id="d138b-181">**CreateGeometryShaderWithStreamOutput**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)
-   [<span data-ttu-id="d138b-182">**CreateHullShader**</span><span class="sxs-lookup"><span data-stu-id="d138b-182">**CreateHullShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)
-   [<span data-ttu-id="d138b-183">**CreatePixelShader**</span><span class="sxs-lookup"><span data-stu-id="d138b-183">**CreatePixelShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createpixelshader)
-   [<span data-ttu-id="d138b-184">**CreateVertexShader**</span><span class="sxs-lookup"><span data-stu-id="d138b-184">**CreateVertexShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)

<span data-ttu-id="d138b-185">Além disso, se você fornecer um valor não **nulo** para *pHResult* quando você fornecer **NULL** para *pPump*, **D3DX11CompileFromResource** retornará o código de \_ erro E INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="d138b-185">In addition, if you supply a non-**NULL** value to *pHResult* when you supply **NULL** to *pPump*, **D3DX11CompileFromResource** returns the E\_INVALIDARG error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d138b-186">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d138b-186">Requirements</span></span>



| <span data-ttu-id="d138b-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="d138b-187">Requirement</span></span> | <span data-ttu-id="d138b-188">Valor</span><span class="sxs-lookup"><span data-stu-id="d138b-188">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d138b-189">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d138b-189">Header</span></span><br/>  | <dl> <span data-ttu-id="d138b-190"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="d138b-190"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="d138b-191">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d138b-191">Library</span></span><br/> | <dl> <span data-ttu-id="d138b-192"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d138b-192"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="d138b-193">Confira também</span><span class="sxs-lookup"><span data-stu-id="d138b-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d138b-194">Funções D3DX</span><span class="sxs-lookup"><span data-stu-id="d138b-194">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

