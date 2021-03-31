---
description: Observação em vez de usar essa função herdada, recomendamos que você compile offline usando o compilador de linha de comando Fxc.exe ou use a API D3DCompile. Compile um sombreador ou um efeito que é carregado na memória.
ms.assetid: c6458d82-a649-402c-8180-5b7320f9fdb0
title: Função D3DX10CompileFromMemory (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CompileFromMemory
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: fbb4a716df4a893ea122e7badfd6faad536aacce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930717"
---
# <a name="d3dx10compilefrommemory-function"></a><span data-ttu-id="14baf-104">Função D3DX10CompileFromMemory</span><span class="sxs-lookup"><span data-stu-id="14baf-104">D3DX10CompileFromMemory function</span></span>

> [!Note]  
> <span data-ttu-id="14baf-105">Em vez de usar essa função herdada, recomendamos que você compile offline usando o compilador de linha de comando Fxc.exe ou use a API [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) .</span><span class="sxs-lookup"><span data-stu-id="14baf-105">Instead of using this legacy function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API.</span></span>

 

<span data-ttu-id="14baf-106">Compile um sombreador ou um efeito que é carregado na memória.</span><span class="sxs-lookup"><span data-stu-id="14baf-106">Compile a shader or an effect that is loaded in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="14baf-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="14baf-107">Syntax</span></span>


```C++
HRESULT D3DX10CompileFromMemory(
  _In_        LPCSTR             pSrcData,
  _In_        SIZE_T             SrcDataLen,
  _In_        LPCSTR             pFileName,
  _In_  const D3D10_SHADER_MACRO *pDefines,
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



## <a name="parameters"></a><span data-ttu-id="14baf-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="14baf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14baf-109">*pSrcData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="14baf-109">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14baf-110">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="14baf-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="14baf-111">Ponteiro para o sombreador na memória.</span><span class="sxs-lookup"><span data-stu-id="14baf-111">Pointer to the shader in memory.</span></span>

</dd> <dt>

<span data-ttu-id="14baf-112">*SrcDataLen* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="14baf-112">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14baf-113">Tipo: **[ **tamanho \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="14baf-113">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="14baf-114">Tamanho do sombreador na memória.</span><span class="sxs-lookup"><span data-stu-id="14baf-114">Size of the shader in memory.</span></span>

</dd> <dt>

<span data-ttu-id="14baf-115">*pFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="14baf-115">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14baf-116">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="14baf-116">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="14baf-117">O nome do arquivo que contém o código do sombreador.</span><span class="sxs-lookup"><span data-stu-id="14baf-117">The name of the file that contains the shader code.</span></span>

</dd> <dt>

<span data-ttu-id="14baf-118">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="14baf-118">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14baf-119">Tipo: **\* [**macro const \_ D3D \_ Shader**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)**</span><span class="sxs-lookup"><span data-stu-id="14baf-119">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="14baf-120">Opcional.</span><span class="sxs-lookup"><span data-stu-id="14baf-120">Optional.</span></span> <span data-ttu-id="14baf-121">Ponteiro para uma matriz de definições de macro (consulte a [**\_ \_ macro do sombreador do D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span><span class="sxs-lookup"><span data-stu-id="14baf-121">Pointer to an array of macro definitions (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span></span> <span data-ttu-id="14baf-122">A última estrutura na matriz serve como um terminador e deve ter todos os membros definidos como 0.</span><span class="sxs-lookup"><span data-stu-id="14baf-122">The last structure in the array serves as a terminator and must have all members set to 0.</span></span> <span data-ttu-id="14baf-123">Se não for usado, defina *pDefines* como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="14baf-123">If not used, set *pDefines* to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="14baf-124">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="14baf-124">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14baf-125">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="14baf-125">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="14baf-126">Opcional.</span><span class="sxs-lookup"><span data-stu-id="14baf-126">Optional.</span></span> <span data-ttu-id="14baf-127">Ponteiro para uma interface de [**interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) para manipulação de arquivos de inclusão.</span><span class="sxs-lookup"><span data-stu-id="14baf-127">Pointer to an [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) interface for handling include files.</span></span> <span data-ttu-id="14baf-128">Definir isso como **NULL** causará um erro de compilação se um sombreador contiver um \# include.</span><span class="sxs-lookup"><span data-stu-id="14baf-128">Setting this to **NULL** will cause a compile error if a shader contains a \#include.</span></span>

</dd> <dt>

<span data-ttu-id="14baf-129">*pFunctionName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="14baf-129">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14baf-130">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="14baf-130">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="14baf-131">Nome da função de ponto de entrada do sombreador em que começa a execução do sombreador.</span><span class="sxs-lookup"><span data-stu-id="14baf-131">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="14baf-132">Quando você compila um efeito, o **D3DX10CompileFromMemory** ignora *pFunctionName*; Recomendamos que você defina *pFunctionName* como **NULL** porque é uma boa prática de programação definir um parâmetro de ponteiro como **nulo** se a função chamada não o usar.</span><span class="sxs-lookup"><span data-stu-id="14baf-132">When you compile an effect, **D3DX10CompileFromMemory** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="14baf-133">*pProfile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="14baf-133">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14baf-134">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="14baf-134">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="14baf-135">Uma cadeia de caracteres que especifica o modelo de sombreador; pode ser qualquer perfil no [sombreador modelo 2](../direct3dhlsl/dx-graphics-hlsl-sm2.md), no [Shader Model 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md)ou no [Shader Model 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md).</span><span class="sxs-lookup"><span data-stu-id="14baf-135">A string that specifies the shader model; can be any profile in [shader model 2](../direct3dhlsl/dx-graphics-hlsl-sm2.md), [shader model 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md), or [shader model 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md).</span></span>

</dd> <dt>

<span data-ttu-id="14baf-136">*Flags1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="14baf-136">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14baf-137">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="14baf-137">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="14baf-138">[Sinalizadores de compilação de sombreador](d3d10-shader.md).</span><span class="sxs-lookup"><span data-stu-id="14baf-138">[Shader compile flags](d3d10-shader.md).</span></span>

</dd> <dt>

<span data-ttu-id="14baf-139">*Flags2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="14baf-139">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14baf-140">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="14baf-140">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="14baf-141">[Sinalizadores de compilação de efeito](d3d10-graphics-reference-effect-constants.md).</span><span class="sxs-lookup"><span data-stu-id="14baf-141">[Effect compile flags](d3d10-graphics-reference-effect-constants.md).</span></span> <span data-ttu-id="14baf-142">Quando você compila um sombreador e não um arquivo de efeito, o **D3DX10CompileFromMemory** ignora *Flags2*; é recomendável que você defina *Flags2* como zero porque é uma boa prática de programação definir um parâmetro não-de-ponto como zero se a função chamada não for usá-lo.</span><span class="sxs-lookup"><span data-stu-id="14baf-142">When you compile a shader and not an effect file, **D3DX10CompileFromMemory** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="14baf-143">*pPump* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="14baf-143">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14baf-144">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="14baf-144">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="14baf-145">Um ponteiro para uma interface de bombeamento de thread (consulte a [**interface ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="14baf-145">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="14baf-146">Use **NULL** para especificar que essa função não deve retornar até que seja concluída.</span><span class="sxs-lookup"><span data-stu-id="14baf-146">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="14baf-147">*ppShader* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="14baf-147">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14baf-148">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="14baf-148">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="14baf-149">Um ponteiro para uma [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) que contém o sombreador compilado, bem como qualquer informação de depuração e tabela de símbolos inserida.</span><span class="sxs-lookup"><span data-stu-id="14baf-149">A pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) which contains the compiled shader, as well as any embedded debug and symbol-table information.</span></span>

</dd> <dt>

<span data-ttu-id="14baf-150">*ppErrorMsgs* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="14baf-150">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14baf-151">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="14baf-151">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="14baf-152">Um ponteiro para uma [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) que contém uma listagem de erros e avisos ocorridos durante a compilação.</span><span class="sxs-lookup"><span data-stu-id="14baf-152">A pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) which contains a listing of errors and warnings that occurred during compilation.</span></span> <span data-ttu-id="14baf-153">Esses erros e avisos são idênticos à saída de depuração de um depurador.</span><span class="sxs-lookup"><span data-stu-id="14baf-153">These errors and warnings are identical to the debug output from a debugger.</span></span>

</dd> <dt>

<span data-ttu-id="14baf-154">*pHResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="14baf-154">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14baf-155">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="14baf-155">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="14baf-156">Um ponteiro para o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="14baf-156">A pointer to the return value.</span></span> <span data-ttu-id="14baf-157">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="14baf-157">May be **NULL**.</span></span> <span data-ttu-id="14baf-158">Se *pPump* não for **NULL**, *pHResult* deverá ser um local de memória válido até que a execução assíncrona seja concluída.</span><span class="sxs-lookup"><span data-stu-id="14baf-158">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14baf-159">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="14baf-159">Return value</span></span>

<span data-ttu-id="14baf-160">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="14baf-160">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="14baf-161">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="14baf-161">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="14baf-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14baf-162">Requirements</span></span>



| <span data-ttu-id="14baf-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="14baf-163">Requirement</span></span> | <span data-ttu-id="14baf-164">Valor</span><span class="sxs-lookup"><span data-stu-id="14baf-164">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="14baf-165">parâmetro</span><span class="sxs-lookup"><span data-stu-id="14baf-165">Header</span></span><br/> | <dl> <span data-ttu-id="14baf-166"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="14baf-166"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14baf-167">Confira também</span><span class="sxs-lookup"><span data-stu-id="14baf-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14baf-168">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="14baf-168">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
