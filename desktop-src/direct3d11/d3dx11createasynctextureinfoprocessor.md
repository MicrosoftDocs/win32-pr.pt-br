---
title: Função D3DX11CreateAsyncTextureInfoProcessor (D3DX11tex. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Consulte Observações. Crie um processador de dados para ser usado com uma bomba de thread. | Função D3DX11CreateAsyncTextureInfoProcessor (D3DX11tex. h)
ms.assetid: 87de73a5-21f7-4abd-b83a-65c6761681c3
keywords:
- Função D3DX11CreateAsyncTextureInfoProcessor Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncTextureInfoProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aac60b1d496e0f1d4ecb604b18a8ef71cac8b5d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989347"
---
# <a name="d3dx11createasynctextureinfoprocessor-function"></a><span data-ttu-id="a8bce-107">Função D3DX11CreateAsyncTextureInfoProcessor</span><span class="sxs-lookup"><span data-stu-id="a8bce-107">D3DX11CreateAsyncTextureInfoProcessor function</span></span>

> [!Note]  
> <span data-ttu-id="a8bce-108">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="a8bce-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="a8bce-109">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="a8bce-109">See Remarks.</span></span>

 

<span data-ttu-id="a8bce-110">Crie um processador de dados para ser usado com uma [**bomba de thread**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="a8bce-110">Create a data processor to be used with a [**thread pump**](id3dx11threadpump.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a8bce-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a8bce-111">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncTextureInfoProcessor(
  _In_  D3DX11_IMAGE_INFO    *pImageInfo,
  _Out_ ID3DX11DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="a8bce-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a8bce-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8bce-113">*pImageInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a8bce-113">*pImageInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8bce-114">Tipo: **[ **D3DX11 \_ Image \_ info**](d3dx11-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="a8bce-114">Type: **[**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md)\***</span></span>

<span data-ttu-id="a8bce-115">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a8bce-115">Optional.</span></span> <span data-ttu-id="a8bce-116">Identifica as características de uma textura (consulte [**\_ \_ informações de imagem D3DX11**](d3dx11-image-info.md)) quando o processador de dados é criado; defina isso como **nulo** para ler as características de uma textura quando a textura for carregada.</span><span class="sxs-lookup"><span data-stu-id="a8bce-116">Identifies the characteristics of a texture (see [**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="a8bce-117">*ppDataProcessor* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a8bce-117">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a8bce-118">Tipo: **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="a8bce-118">Type: **[**ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span></span>

<span data-ttu-id="a8bce-119">Endereço de um ponteiro para um buffer que contém o processador de dados criado (consulte a [**interface ID3DX11DataProcessor**](id3dx11dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="a8bce-119">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX11DataProcessor Interface**](id3dx11dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8bce-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a8bce-120">Return value</span></span>

<span data-ttu-id="a8bce-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a8bce-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a8bce-122">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="a8bce-122">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a8bce-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="a8bce-123">Remarks</span></span>

<span data-ttu-id="a8bce-124">Essa API cria uma interface de processador de dados; [**D3DX11CreateAsyncTextureProcessor**](d3dx11createasynctextureprocessor.md) cria a interface do processador de dados e carrega a textura.</span><span class="sxs-lookup"><span data-stu-id="a8bce-124">This API does creates a data-processor interface; [**D3DX11CreateAsyncTextureProcessor**](d3dx11createasynctextureprocessor.md) creates the data-processor interface and loads the texture.</span></span>

<span data-ttu-id="a8bce-125">Não há nenhuma implementação do carregador assíncrono fora do D3DX 10 e D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="a8bce-125">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="a8bce-126">Para aplicativos da Windows Store, os exemplos do DirectX (por exemplo, o [exemplo de tutorial do Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) incluem o módulo **BasicLoader** que usa o modelo de programação assíncrona do Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span><span class="sxs-lookup"><span data-stu-id="a8bce-126">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="a8bce-127">Para aplicativos de área de trabalho Win32, você pode usar o [tempo de execução de simultaneidade](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) para implementar algo semelhante ao modelo de programação Windows Runtime assíncrona.</span><span class="sxs-lookup"><span data-stu-id="a8bce-127">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8bce-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8bce-128">Requirements</span></span>



| <span data-ttu-id="a8bce-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8bce-129">Requirement</span></span> | <span data-ttu-id="a8bce-130">Valor</span><span class="sxs-lookup"><span data-stu-id="a8bce-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8bce-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a8bce-131">Header</span></span><br/>  | <dl> <span data-ttu-id="a8bce-132"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8bce-132"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="a8bce-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a8bce-133">Library</span></span><br/> | <dl> <span data-ttu-id="a8bce-134"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a8bce-134"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="a8bce-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="a8bce-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8bce-136">Funções D3DX</span><span class="sxs-lookup"><span data-stu-id="a8bce-136">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

