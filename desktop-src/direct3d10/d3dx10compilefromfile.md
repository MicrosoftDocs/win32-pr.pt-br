---
description: Observação em vez de usar essa função herdada, recomendamos que você compile offline usando o compilador de linha de comando Fxc.exe ou use a API D3DCompile. Compilar um sombreador ou um efeito de um arquivo.
ms.assetid: b0ca0b6a-3ff0-49ee-83de-14c4686a7104
title: Função D3DX10CompileFromFile (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CompileFromFile
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 571f8123a9834c95ecca6043c3495fb18fbaca47
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105815528"
---
# <a name="d3dx10compilefromfile-function"></a><span data-ttu-id="1f442-104">Função D3DX10CompileFromFile</span><span class="sxs-lookup"><span data-stu-id="1f442-104">D3DX10CompileFromFile function</span></span>

> [!Note]  
> <span data-ttu-id="1f442-105">Em vez de usar essa função herdada, recomendamos que você compile offline usando o compilador de linha de comando Fxc.exe ou use a API [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) .</span><span class="sxs-lookup"><span data-stu-id="1f442-105">Instead of using this legacy function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API.</span></span>

 

<span data-ttu-id="1f442-106">Compilar um sombreador ou um efeito de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="1f442-106">Compile a shader or an effect from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f442-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1f442-107">Syntax</span></span>


```C++
HRESULT D3DX10CompileFromFile(
  _In_        LPCTSTR            pSrcFile,
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



## <a name="parameters"></a><span data-ttu-id="1f442-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1f442-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f442-109">*pSrcFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1f442-109">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f442-110">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1f442-110">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1f442-111">O nome do arquivo que contém o código do sombreador.</span><span class="sxs-lookup"><span data-stu-id="1f442-111">The name of the file that contains the shader code.</span></span> <span data-ttu-id="1f442-112">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="1f442-112">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="1f442-113">Caso contrário, o tipo de dados será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="1f442-113">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="1f442-114">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1f442-114">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f442-115">Tipo: **\* [**macro const \_ D3D \_ Shader**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)**</span><span class="sxs-lookup"><span data-stu-id="1f442-115">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="1f442-116">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1f442-116">Optional.</span></span> <span data-ttu-id="1f442-117">Ponteiro para uma matriz de definições de macro (consulte a [**\_ \_ macro do sombreador do D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span><span class="sxs-lookup"><span data-stu-id="1f442-117">Pointer to an array of macro definitions (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span></span> <span data-ttu-id="1f442-118">A última estrutura na matriz serve como um terminador e deve ter todos os membros definidos como 0.</span><span class="sxs-lookup"><span data-stu-id="1f442-118">The last structure in the array serves as a terminator and must have all members set to 0.</span></span> <span data-ttu-id="1f442-119">Se não for usado, defina *pDefines* como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="1f442-119">If not used, set *pDefines* to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1f442-120">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1f442-120">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f442-121">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="1f442-121">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="1f442-122">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1f442-122">Optional.</span></span> <span data-ttu-id="1f442-123">Ponteiro para uma interface de [**interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) para manipulação de arquivos de inclusão.</span><span class="sxs-lookup"><span data-stu-id="1f442-123">Pointer to an [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) interface for handling include files.</span></span> <span data-ttu-id="1f442-124">Definir isso como **NULL** causará um erro de compilação se um sombreador contiver um \# include.</span><span class="sxs-lookup"><span data-stu-id="1f442-124">Setting this to **NULL** will cause a compile error if a shader contains a \#include.</span></span>

</dd> <dt>

<span data-ttu-id="1f442-125">*pFunctionName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1f442-125">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f442-126">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1f442-126">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1f442-127">Nome da função de ponto de entrada do sombreador em que começa a execução do sombreador.</span><span class="sxs-lookup"><span data-stu-id="1f442-127">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="1f442-128">Quando você compila um efeito, o **D3DX10CompileFromFile** ignora *pFunctionName*; Recomendamos que você defina *pFunctionName* como **NULL** porque é uma boa prática de programação definir um parâmetro de ponteiro como **nulo** se a função chamada não o usar.</span><span class="sxs-lookup"><span data-stu-id="1f442-128">When you compile an effect, **D3DX10CompileFromFile** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="1f442-129">*pProfile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1f442-129">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f442-130">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1f442-130">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1f442-131">Uma cadeia de caracteres que especifica o modelo de sombreador; pode ser qualquer perfil no [sombreador modelo 2](../direct3dhlsl/dx-graphics-hlsl-sm2.md), no [Shader Model 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md)ou no [Shader Model 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md).</span><span class="sxs-lookup"><span data-stu-id="1f442-131">A string that specifies the shader model; can be any profile in [shader model 2](../direct3dhlsl/dx-graphics-hlsl-sm2.md), [shader model 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md), or [shader model 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f442-132">*Flags1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1f442-132">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f442-133">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1f442-133">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1f442-134">[Sinalizadores de compilação de sombreador](d3d10-shader.md).</span><span class="sxs-lookup"><span data-stu-id="1f442-134">[Shader compile flags](d3d10-shader.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f442-135">*Flags2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1f442-135">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f442-136">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1f442-136">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1f442-137">[Sinalizadores de compilação de efeito](d3d10-graphics-reference-effect-constants.md).</span><span class="sxs-lookup"><span data-stu-id="1f442-137">[Effect compile flags](d3d10-graphics-reference-effect-constants.md).</span></span> <span data-ttu-id="1f442-138">Quando você compila um sombreador e não um arquivo de efeito, o **D3DX10CompileFromFile** ignora *Flags2*; é recomendável que você defina *Flags2* como zero porque é uma boa prática de programação definir um parâmetro não-de-ponto como zero se a função chamada não for usá-lo.</span><span class="sxs-lookup"><span data-stu-id="1f442-138">When you compile a shader and not an effect file, **D3DX10CompileFromFile** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="1f442-139">*pPump* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1f442-139">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f442-140">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="1f442-140">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="1f442-141">Um ponteiro para uma interface de bombeamento de thread (consulte a [**interface ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="1f442-141">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="1f442-142">Use **NULL** para especificar que essa função não deve retornar até que seja concluída.</span><span class="sxs-lookup"><span data-stu-id="1f442-142">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="1f442-143">*ppShader* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1f442-143">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f442-144">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="1f442-144">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="1f442-145">Um ponteiro para uma [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) que contém o sombreador compilado, bem como qualquer informação de depuração e tabela de símbolos inserida.</span><span class="sxs-lookup"><span data-stu-id="1f442-145">A pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) which contains the compiled shader, as well as any embedded debug and symbol-table information.</span></span>

</dd> <dt>

<span data-ttu-id="1f442-146">*ppErrorMsgs* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1f442-146">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f442-147">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="1f442-147">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="1f442-148">Um ponteiro para uma [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) que contém uma listagem de erros e avisos ocorridos durante a compilação.</span><span class="sxs-lookup"><span data-stu-id="1f442-148">A pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) which contains a listing of errors and warnings that occurred during compilation.</span></span> <span data-ttu-id="1f442-149">Esses erros e avisos são idênticos à saída de depuração de um depurador.</span><span class="sxs-lookup"><span data-stu-id="1f442-149">These errors and warnings are identical to the debug output from a debugger.</span></span>

</dd> <dt>

<span data-ttu-id="1f442-150">*pHResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1f442-150">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f442-151">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="1f442-151">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="1f442-152">Um ponteiro para o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="1f442-152">A pointer to the return value.</span></span> <span data-ttu-id="1f442-153">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="1f442-153">May be **NULL**.</span></span> <span data-ttu-id="1f442-154">Se *pPump* não for **NULL**, *pHResult* deverá ser um local de memória válido até que a execução assíncrona seja concluída.</span><span class="sxs-lookup"><span data-stu-id="1f442-154">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f442-155">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1f442-155">Return value</span></span>

<span data-ttu-id="1f442-156">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1f442-156">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1f442-157">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="1f442-157">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1f442-158">Comentários</span><span class="sxs-lookup"><span data-stu-id="1f442-158">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="1f442-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f442-159">Requirements</span></span>



| <span data-ttu-id="1f442-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f442-160">Requirement</span></span> | <span data-ttu-id="1f442-161">Valor</span><span class="sxs-lookup"><span data-stu-id="1f442-161">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f442-162">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1f442-162">Header</span></span><br/> | <dl> <span data-ttu-id="1f442-163"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f442-163"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f442-164">Confira também</span><span class="sxs-lookup"><span data-stu-id="1f442-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f442-165">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="1f442-165">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
