---
title: Função D3DX11CreateAsyncCompilerProcessor (D3DX11async. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Consulte Observações. Crie um processador de dados assíncronos para um sombreador.
ms.assetid: 90756ac3-946d-49fa-9f97-70dc5da812c6
keywords:
- Função D3DX11CreateAsyncCompilerProcessor Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncCompilerProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 533e487e65640b8c17a0ff8d061388e8b5a6c0f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989354"
---
# <a name="d3dx11createasynccompilerprocessor-function"></a><span data-ttu-id="62809-106">Função D3DX11CreateAsyncCompilerProcessor</span><span class="sxs-lookup"><span data-stu-id="62809-106">D3DX11CreateAsyncCompilerProcessor function</span></span>

> [!Note]  
> <span data-ttu-id="62809-107">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="62809-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="62809-108">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="62809-108">See Remarks.</span></span>

 

<span data-ttu-id="62809-109">Crie um processador de dados assíncronos para um sombreador.</span><span class="sxs-lookup"><span data-stu-id="62809-109">Create an asynchronous-data processor for a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="62809-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="62809-110">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncCompilerProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D11_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pFunctionName,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags1,
  _In_        UINT                 Flags2,
  _Out_       ID3D10Blob           **ppCompiledShader,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX11DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="62809-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="62809-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62809-112">*pFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="62809-112">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62809-113">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="62809-113">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="62809-114">Uma cadeia de caracteres que contém o nome de arquivo do sombreador.</span><span class="sxs-lookup"><span data-stu-id="62809-114">A string that contains the shader filename.</span></span>

</dd> <dt>

<span data-ttu-id="62809-115">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="62809-115">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62809-116">Tipo: **\_ \_ macro \* do sombreador D3D11 const**</span><span class="sxs-lookup"><span data-stu-id="62809-116">Type: **const D3D11\_SHADER\_MACRO\***</span></span>

<span data-ttu-id="62809-117">Uma matriz com terminação nula de macros de sombreador; Defina como **NULL** para não especificar nenhuma macro.</span><span class="sxs-lookup"><span data-stu-id="62809-117">A NULL-terminated array of shader macros; set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="62809-118">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="62809-118">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62809-119">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="62809-119">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="62809-120">Um ponteiro para uma interface de inclusão.</span><span class="sxs-lookup"><span data-stu-id="62809-120">A pointer to an include interface.</span></span> <span data-ttu-id="62809-121">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="62809-121">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="62809-122">*pFunctionName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="62809-122">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62809-123">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="62809-123">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="62809-124">Nome da função de ponto de entrada do sombreador em que começa a execução do sombreador.</span><span class="sxs-lookup"><span data-stu-id="62809-124">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="62809-125">Quando você compila um efeito, o **D3DX11CreateAsyncCompilerProcessor** ignora *pFunctionName*; Recomendamos que você defina *pFunctionName* como **NULL** porque é uma boa prática de programação definir um parâmetro de ponteiro como **nulo** se a função chamada não o usar..</span><span class="sxs-lookup"><span data-stu-id="62809-125">When you compile an effect, **D3DX11CreateAsyncCompilerProcessor** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it..</span></span>

</dd> <dt>

<span data-ttu-id="62809-126">*pProfile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="62809-126">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62809-127">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="62809-127">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="62809-128">Uma cadeia de caracteres que especifica o perfil do sombreador ou o modelo de sombreador; pode ser qualquer perfil no sombreador modelo 2, o Shader Model 3, o Shader Model 4 ou o Shader Model 5.</span><span class="sxs-lookup"><span data-stu-id="62809-128">A string that specifies the shader profile or shader model; can be any profile in shader model 2, shader model 3, shader model 4, or shader model 5.</span></span> <span data-ttu-id="62809-129">O perfil também pode ser para o tipo de efeito (por exemplo, FX \_ 4 \_ 1).</span><span class="sxs-lookup"><span data-stu-id="62809-129">The profile can also be for effect type (for example, fx\_4\_1).</span></span>

</dd> <dt>

<span data-ttu-id="62809-130">*Flags1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="62809-130">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62809-131">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="62809-131">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="62809-132">Sinalizadores de compilação de sombreador.</span><span class="sxs-lookup"><span data-stu-id="62809-132">Shader compile flags.</span></span>

</dd> <dt>

<span data-ttu-id="62809-133">*Flags2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="62809-133">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62809-134">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="62809-134">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="62809-135">Sinalizadores de compilação de efeito.</span><span class="sxs-lookup"><span data-stu-id="62809-135">Effect compile flags.</span></span> <span data-ttu-id="62809-136">Quando você compila um sombreador e não um arquivo de efeito, o **D3DX11CreateAsyncCompilerProcessor** ignora *Flags2*; é recomendável que você defina *Flags2* como zero porque é uma boa prática de programação definir um parâmetro não-de-ponto como zero se a função chamada não for usá-lo.</span><span class="sxs-lookup"><span data-stu-id="62809-136">When you compile a shader and not an effect file, **D3DX11CreateAsyncCompilerProcessor** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="62809-137">*ppCompiledShader* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="62809-137">*ppCompiledShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="62809-138">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="62809-138">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="62809-139">Endereço de um ponteiro para o efeito compilado.</span><span class="sxs-lookup"><span data-stu-id="62809-139">Address of a pointer to the compiled effect.</span></span>

</dd> <dt>

<span data-ttu-id="62809-140">*ppErrorBuffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="62809-140">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="62809-141">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="62809-141">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="62809-142">Endereço de um ponteiro para erros de compilação.</span><span class="sxs-lookup"><span data-stu-id="62809-142">Address of a pointer to compile errors.</span></span>

</dd> <dt>

<span data-ttu-id="62809-143">*ppDataProcessor* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="62809-143">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="62809-144">Tipo: **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="62809-144">Type: **[**ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span></span>

<span data-ttu-id="62809-145">Endereço de um ponteiro para um buffer que contém o processador de dados criado (consulte a [**interface ID3DX11DataProcessor**](id3dx11dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="62809-145">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX11DataProcessor Interface**](id3dx11dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62809-146">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="62809-146">Return value</span></span>

<span data-ttu-id="62809-147">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="62809-147">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="62809-148">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="62809-148">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="62809-149">Comentários</span><span class="sxs-lookup"><span data-stu-id="62809-149">Remarks</span></span>

<span data-ttu-id="62809-150">Não há nenhuma implementação do carregador assíncrono fora do D3DX 10 e D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="62809-150">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="62809-151">Para aplicativos da Windows Store, os exemplos do DirectX (por exemplo, o [exemplo de tutorial do Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) incluem o módulo **BasicLoader** que usa o modelo de programação assíncrona do Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span><span class="sxs-lookup"><span data-stu-id="62809-151">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="62809-152">Para aplicativos de área de trabalho Win32, você pode usar o [tempo de execução de simultaneidade](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) para implementar algo semelhante ao modelo de programação Windows Runtime assíncrona.</span><span class="sxs-lookup"><span data-stu-id="62809-152">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="62809-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62809-153">Requirements</span></span>



| <span data-ttu-id="62809-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="62809-154">Requirement</span></span> | <span data-ttu-id="62809-155">Valor</span><span class="sxs-lookup"><span data-stu-id="62809-155">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="62809-156">parâmetro</span><span class="sxs-lookup"><span data-stu-id="62809-156">Header</span></span><br/>  | <dl> <span data-ttu-id="62809-157"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="62809-157"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="62809-158">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="62809-158">Library</span></span><br/> | <dl> <span data-ttu-id="62809-159"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="62809-159"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="62809-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="62809-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62809-161">Funções D3DX</span><span class="sxs-lookup"><span data-stu-id="62809-161">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

