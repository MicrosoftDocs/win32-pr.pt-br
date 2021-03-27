---
title: Função D3DX11CreateAsyncShaderPreprocessProcessor (D3DX11async. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Consulte Observações. Crie um processador de dados para um sombreador de forma assíncrona.
ms.assetid: a7e9754b-acc1-49d0-bd8e-b116bc3c7e3a
keywords:
- Função D3DX11CreateAsyncShaderPreprocessProcessor Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncShaderPreprocessProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46e58b267f186e5fd0104b10e9f9423f407aaf13
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930676"
---
# <a name="d3dx11createasyncshaderpreprocessprocessor-function"></a><span data-ttu-id="3ed31-106">Função D3DX11CreateAsyncShaderPreprocessProcessor</span><span class="sxs-lookup"><span data-stu-id="3ed31-106">D3DX11CreateAsyncShaderPreprocessProcessor function</span></span>

> [!Note]  
> <span data-ttu-id="3ed31-107">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="3ed31-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="3ed31-108">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="3ed31-108">See Remarks.</span></span>

 

<span data-ttu-id="3ed31-109">Crie um processador de dados para um sombreador de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="3ed31-109">Create a data processor for a shader asynchronously.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ed31-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3ed31-110">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncShaderPreprocessProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D11_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _Out_       ID3D10Blob           **ppShaderText,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX11DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="3ed31-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3ed31-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ed31-112">*pFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3ed31-112">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ed31-113">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3ed31-113">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3ed31-114">Uma cadeia de caracteres que contém o nome de arquivo do sombreador.</span><span class="sxs-lookup"><span data-stu-id="3ed31-114">A string that contains the shader filename.</span></span>

</dd> <dt>

<span data-ttu-id="3ed31-115">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3ed31-115">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ed31-116">Tipo: **\_ \_ macro \* do sombreador D3D11 const**</span><span class="sxs-lookup"><span data-stu-id="3ed31-116">Type: **const D3D11\_SHADER\_MACRO\***</span></span>

<span data-ttu-id="3ed31-117">Uma matriz com terminação nula de macros de sombreador; Defina como **NULL** para não especificar nenhuma macro.</span><span class="sxs-lookup"><span data-stu-id="3ed31-117">A NULL-terminated array of shader macros; set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="3ed31-118">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3ed31-118">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ed31-119">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="3ed31-119">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="3ed31-120">Um ponteiro para uma interface de inclusão; Defina como **NULL** para especificar que não há nenhum arquivo de inclusão.</span><span class="sxs-lookup"><span data-stu-id="3ed31-120">A pointer to an include interface; set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="3ed31-121">*ppShaderText* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3ed31-121">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ed31-122">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="3ed31-122">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="3ed31-123">Endereço de um ponteiro para um buffer que contém o texto ASCII do sombreador.</span><span class="sxs-lookup"><span data-stu-id="3ed31-123">Address of a pointer to a buffer that contains the ASCII text of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="3ed31-124">*ppErrorBuffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3ed31-124">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ed31-125">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="3ed31-125">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="3ed31-126">Endereço de um ponteiro para um buffer que contém erros de compilação.</span><span class="sxs-lookup"><span data-stu-id="3ed31-126">Address of a pointer to a buffer that contains compile errors.</span></span>

</dd> <dt>

<span data-ttu-id="3ed31-127">*ppDataProcessor* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3ed31-127">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ed31-128">Tipo: **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="3ed31-128">Type: **[**ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span></span>

<span data-ttu-id="3ed31-129">Endereço de um ponteiro para um buffer que contém o processador de dados criado (consulte a [**interface ID3DX11DataProcessor**](id3dx11dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="3ed31-129">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX11DataProcessor Interface**](id3dx11dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ed31-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3ed31-130">Return value</span></span>

<span data-ttu-id="3ed31-131">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3ed31-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3ed31-132">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="3ed31-132">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3ed31-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ed31-133">Remarks</span></span>

<span data-ttu-id="3ed31-134">Não há nenhuma implementação do carregador assíncrono fora do D3DX 10 e D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="3ed31-134">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="3ed31-135">Para aplicativos da Windows Store, os exemplos do DirectX (por exemplo, o [exemplo de tutorial do Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) incluem o módulo **BasicLoader** que usa o modelo de programação assíncrona do Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span><span class="sxs-lookup"><span data-stu-id="3ed31-135">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="3ed31-136">Para aplicativos de área de trabalho Win32, você pode usar o [tempo de execução de simultaneidade](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) para implementar algo semelhante ao modelo de programação Windows Runtime assíncrona.</span><span class="sxs-lookup"><span data-stu-id="3ed31-136">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ed31-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ed31-137">Requirements</span></span>



| <span data-ttu-id="3ed31-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ed31-138">Requirement</span></span> | <span data-ttu-id="3ed31-139">Valor</span><span class="sxs-lookup"><span data-stu-id="3ed31-139">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ed31-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3ed31-140">Header</span></span><br/>  | <dl> <span data-ttu-id="3ed31-141"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ed31-141"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="3ed31-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3ed31-142">Library</span></span><br/> | <dl> <span data-ttu-id="3ed31-143"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3ed31-143"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="3ed31-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ed31-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ed31-145">Funções D3DX</span><span class="sxs-lookup"><span data-stu-id="3ed31-145">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

