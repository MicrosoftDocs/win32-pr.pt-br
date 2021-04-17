---
description: Observação em vez de usar essa função herdada, recomendamos que você compile offline usando o compilador de linha de comando Fxc.exe ou use a API D3DCompile. Compilar um sombreador ou um efeito de um recurso.
ms.assetid: d291e47d-e04f-4e2d-9d05-9aef8e4fcf7e
title: Função D3DX10CompileFromResource (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CompileFromResource
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 6b698700804ca767c953343e6d5a5e540ca77555
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105812393"
---
# <a name="d3dx10compilefromresource-function"></a><span data-ttu-id="27c85-104">Função D3DX10CompileFromResource</span><span class="sxs-lookup"><span data-stu-id="27c85-104">D3DX10CompileFromResource function</span></span>

> [!Note]  
> <span data-ttu-id="27c85-105">Em vez de usar essa função herdada, recomendamos que você compile offline usando o compilador de linha de comando Fxc.exe ou use a API [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) .</span><span class="sxs-lookup"><span data-stu-id="27c85-105">Instead of using this legacy function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API.</span></span>

 

<span data-ttu-id="27c85-106">Compilar um sombreador ou um efeito de um recurso.</span><span class="sxs-lookup"><span data-stu-id="27c85-106">Compile a shader or an effect from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="27c85-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="27c85-107">Syntax</span></span>


```C++
HRESULT D3DX10CompileFromResource(
  _In_        HMODULE            hSrcModule,
  _In_        LPCTSTR            pSrcResource,
  _In_        LPCTSTR            pSrcFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        LPCSTR             pFunctionName,
  _In_        LPCSTR             pProfile,
  _In_        UINT               Flags1,
  _In_        UINT               Flags2,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShader,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="27c85-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="27c85-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27c85-109">*hSrcModule* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="27c85-109">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27c85-110">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="27c85-110">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="27c85-111">Identificador para o módulo de recurso que contém o sombreador.</span><span class="sxs-lookup"><span data-stu-id="27c85-111">Handle to the resource module containing the shader.</span></span> <span data-ttu-id="27c85-112">HMODULE pode ser obtido com a [função GetModuleHandle](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span><span class="sxs-lookup"><span data-stu-id="27c85-112">HMODULE can be obtained with [GetModuleHandle Function](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="27c85-113">*pSrcResource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="27c85-113">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27c85-114">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="27c85-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="27c85-115">Nome do recurso que contém o sombreador.</span><span class="sxs-lookup"><span data-stu-id="27c85-115">Name of the resource containing the shader.</span></span> <span data-ttu-id="27c85-116">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="27c85-116">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="27c85-117">Caso contrário, o tipo de dados será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="27c85-117">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="27c85-118">*pSrcFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="27c85-118">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27c85-119">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="27c85-119">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="27c85-120">Opcional.</span><span class="sxs-lookup"><span data-stu-id="27c85-120">Optional.</span></span> <span data-ttu-id="27c85-121">Nome do arquivo de efeito, que é usado somente para mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="27c85-121">Effect file name, which is used for error messages only.</span></span> <span data-ttu-id="27c85-122">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="27c85-122">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="27c85-123">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="27c85-123">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27c85-124">Tipo: **\* [**macro const \_ D3D \_ Shader**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)**</span><span class="sxs-lookup"><span data-stu-id="27c85-124">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="27c85-125">Opcional.</span><span class="sxs-lookup"><span data-stu-id="27c85-125">Optional.</span></span> <span data-ttu-id="27c85-126">Ponteiro para uma matriz de definições de macro (consulte a [**\_ \_ macro do sombreador do D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span><span class="sxs-lookup"><span data-stu-id="27c85-126">Pointer to an array of macro definitions (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span></span> <span data-ttu-id="27c85-127">A última estrutura na matriz serve como um terminador e deve ter todos os membros definidos como 0.</span><span class="sxs-lookup"><span data-stu-id="27c85-127">The last structure in the array serves as a terminator and must have all members set to 0.</span></span> <span data-ttu-id="27c85-128">Se não for usado, defina *pDefines* como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="27c85-128">If not used, set *pDefines* to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="27c85-129">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="27c85-129">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27c85-130">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="27c85-130">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="27c85-131">Opcional.</span><span class="sxs-lookup"><span data-stu-id="27c85-131">Optional.</span></span> <span data-ttu-id="27c85-132">Ponteiro para uma interface de [**interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) para manipulação de arquivos de inclusão.</span><span class="sxs-lookup"><span data-stu-id="27c85-132">Pointer to an [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) interface for handling include files.</span></span> <span data-ttu-id="27c85-133">Definir isso como **NULL** causará um erro de compilação se um sombreador contiver um \# include.</span><span class="sxs-lookup"><span data-stu-id="27c85-133">Setting this to **NULL** will cause a compile error if a shader contains a \#include.</span></span>

</dd> <dt>

<span data-ttu-id="27c85-134">*pFunctionName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="27c85-134">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27c85-135">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="27c85-135">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="27c85-136">Nome da função de ponto de entrada do sombreador em que começa a execução do sombreador.</span><span class="sxs-lookup"><span data-stu-id="27c85-136">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="27c85-137">Quando você compila um efeito, o **D3DX10CompileFromResource** ignora *pFunctionName*; Recomendamos que você defina *pFunctionName* como **NULL** porque é uma boa prática de programação definir um parâmetro de ponteiro como **nulo** se a função chamada não o usar.</span><span class="sxs-lookup"><span data-stu-id="27c85-137">When you compile an effect, **D3DX10CompileFromResource** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="27c85-138">*pProfile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="27c85-138">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27c85-139">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="27c85-139">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="27c85-140">Uma cadeia de caracteres que especifica o modelo de sombreador; pode ser qualquer perfil no [sombreador modelo 2](../direct3dhlsl/dx-graphics-hlsl-sm2.md), no [Shader Model 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md)ou no [Shader Model 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md).</span><span class="sxs-lookup"><span data-stu-id="27c85-140">A string that specifies the shader model; can be any profile in [shader model 2](../direct3dhlsl/dx-graphics-hlsl-sm2.md), [shader model 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md), or [shader model 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md).</span></span>

</dd> <dt>

<span data-ttu-id="27c85-141">*Flags1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="27c85-141">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27c85-142">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="27c85-142">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="27c85-143">[Sinalizadores de compilação de sombreador](d3d10-shader.md).</span><span class="sxs-lookup"><span data-stu-id="27c85-143">[Shader compile flags](d3d10-shader.md).</span></span>

</dd> <dt>

<span data-ttu-id="27c85-144">*Flags2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="27c85-144">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27c85-145">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="27c85-145">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="27c85-146">[Sinalizadores de compilação de efeito](d3d10-graphics-reference-effect-constants.md).</span><span class="sxs-lookup"><span data-stu-id="27c85-146">[Effect compile flags](d3d10-graphics-reference-effect-constants.md).</span></span> <span data-ttu-id="27c85-147">Quando você compila um sombreador e não um arquivo de efeito, o **D3DX10CompileFromResource** ignora *Flags2*; é recomendável que você defina *Flags2* como zero porque é uma boa prática de programação definir um parâmetro não-de-ponto como zero se a função chamada não for usá-lo.</span><span class="sxs-lookup"><span data-stu-id="27c85-147">When you compile a shader and not an effect file, **D3DX10CompileFromResource** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="27c85-148">*pPump* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="27c85-148">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27c85-149">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="27c85-149">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="27c85-150">Um ponteiro para uma interface de bombeamento de thread (consulte a [**interface ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="27c85-150">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="27c85-151">Use **NULL** para especificar que essa função não deve retornar até que seja concluída.</span><span class="sxs-lookup"><span data-stu-id="27c85-151">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="27c85-152">*ppShader* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="27c85-152">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="27c85-153">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="27c85-153">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="27c85-154">Um ponteiro para uma [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) que contém o sombreador compilado, bem como qualquer informação de depuração e tabela de símbolos inserida.</span><span class="sxs-lookup"><span data-stu-id="27c85-154">A pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) which contains the compiled shader, as well as any embedded debug and symbol-table information.</span></span>

</dd> <dt>

<span data-ttu-id="27c85-155">*ppErrorMsgs* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="27c85-155">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="27c85-156">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="27c85-156">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="27c85-157">Um ponteiro para uma [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) que contém uma listagem de erros e avisos ocorridos durante a compilação.</span><span class="sxs-lookup"><span data-stu-id="27c85-157">A pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) which contains a listing of errors and warnings that occurred during compilation.</span></span> <span data-ttu-id="27c85-158">Esses erros e avisos são idênticos à saída de depuração de um depurador.</span><span class="sxs-lookup"><span data-stu-id="27c85-158">These errors and warnings are identical to the debug output from a debugger.</span></span>

</dd> <dt>

<span data-ttu-id="27c85-159">*pHResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="27c85-159">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="27c85-160">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="27c85-160">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="27c85-161">Um ponteiro para o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="27c85-161">A pointer to the return value.</span></span> <span data-ttu-id="27c85-162">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="27c85-162">May be **NULL**.</span></span> <span data-ttu-id="27c85-163">Se *pPump* não for **NULL**, *pHResult* deverá ser um local de memória válido até que a execução assíncrona seja concluída.</span><span class="sxs-lookup"><span data-stu-id="27c85-163">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27c85-164">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="27c85-164">Return value</span></span>

<span data-ttu-id="27c85-165">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="27c85-165">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="27c85-166">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="27c85-166">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="27c85-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27c85-167">Requirements</span></span>



| <span data-ttu-id="27c85-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="27c85-168">Requirement</span></span> | <span data-ttu-id="27c85-169">Valor</span><span class="sxs-lookup"><span data-stu-id="27c85-169">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="27c85-170">parâmetro</span><span class="sxs-lookup"><span data-stu-id="27c85-170">Header</span></span><br/> | <dl> <span data-ttu-id="27c85-171"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="27c85-171"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27c85-172">Confira também</span><span class="sxs-lookup"><span data-stu-id="27c85-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27c85-173">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="27c85-173">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
