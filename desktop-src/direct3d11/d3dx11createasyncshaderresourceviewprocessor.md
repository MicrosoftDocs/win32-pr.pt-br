---
title: Função D3DX11CreateAsyncShaderResourceViewProcessor (D3DX11async. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.
ms.assetid: bd9349af-f433-47f9-b443-3049c32fc286
keywords:
- Função D3DX11CreateAsyncShaderResourceViewProcessor Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncShaderResourceViewProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3164aac5ddaec3d61108a2cf129b76991b8f76a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989345"
---
# <a name="d3dx11createasyncshaderresourceviewprocessor-function"></a><span data-ttu-id="43de6-104">Função D3DX11CreateAsyncShaderResourceViewProcessor</span><span class="sxs-lookup"><span data-stu-id="43de6-104">D3DX11CreateAsyncShaderResourceViewProcessor function</span></span>

> [!Note]  
> <span data-ttu-id="43de6-105">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="43de6-105">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="43de6-106">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="43de6-106">See Remarks.</span></span>

 

<span data-ttu-id="43de6-107">Crie um processador de dados que carregará um recurso e, em seguida, crie uma exibição de recurso de sombreador para ele.</span><span class="sxs-lookup"><span data-stu-id="43de6-107">Create a data processor that will load a resource and then create a shader-resource view for it.</span></span> <span data-ttu-id="43de6-108">Os processadores de dados são um componente do recurso de carregamento de dados assíncronos no D3DX11 que usa [**bombas de thread**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="43de6-108">Data processors are a component of the asynchronous data loading feature in D3DX11 that uses [**thread pumps**](id3dx11threadpump.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="43de6-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43de6-109">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncShaderResourceViewProcessor(
  _In_  ID3D11Device           *pDevice,
  _In_  D3DX11_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX11DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="43de6-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43de6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43de6-111">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="43de6-111">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43de6-112">Tipo: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span><span class="sxs-lookup"><span data-stu-id="43de6-112">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span></span>

<span data-ttu-id="43de6-113">Ponteiro para o dispositivo Direct3D (consulte [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) que será usado para criar um recurso e uma exibição de recurso de sombreador para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="43de6-113">Pointer to the Direct3D device (see [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) that will be used to create a resource and a shader-resource view for that resource.</span></span>

</dd> <dt>

<span data-ttu-id="43de6-114">*pLoadInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="43de6-114">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43de6-115">Tipo: **[ **\_ informações de \_ carregamento \_ de imagem D3DX11**](d3dx11-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="43de6-115">Type: **[**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)\***</span></span>

<span data-ttu-id="43de6-116">Opcional.</span><span class="sxs-lookup"><span data-stu-id="43de6-116">Optional.</span></span> <span data-ttu-id="43de6-117">Identifica as características de uma textura (consulte [**\_ informações de \_ carregamento \_ de imagem D3DX11**](d3dx11-image-load-info.md)) quando o processador de dados é criado; defina isso como **nulo** para ler as características de uma textura quando a textura for carregada.</span><span class="sxs-lookup"><span data-stu-id="43de6-117">Identifies the characteristics of a texture (see [**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="43de6-118">*ppDataProcessor* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="43de6-118">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43de6-119">Tipo: **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="43de6-119">Type: **[**ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span></span>

<span data-ttu-id="43de6-120">Endereço de um ponteiro para um buffer que contém o processador de dados criado (consulte a [**interface ID3DX11DataProcessor**](id3dx11dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="43de6-120">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX11DataProcessor Interface**](id3dx11dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43de6-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="43de6-121">Return value</span></span>

<span data-ttu-id="43de6-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="43de6-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="43de6-123">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="43de6-123">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="43de6-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="43de6-124">Remarks</span></span>

<span data-ttu-id="43de6-125">Não há nenhuma implementação do carregador assíncrono fora do D3DX 10 e D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="43de6-125">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="43de6-126">Para aplicativos da Windows Store, os exemplos do DirectX (por exemplo, o [exemplo de tutorial do Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) incluem o módulo **BasicLoader** que usa o modelo de programação assíncrona do Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span><span class="sxs-lookup"><span data-stu-id="43de6-126">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="43de6-127">Para aplicativos de área de trabalho Win32, você pode usar o [tempo de execução de simultaneidade](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) para implementar algo semelhante ao modelo de programação Windows Runtime assíncrona.</span><span class="sxs-lookup"><span data-stu-id="43de6-127">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="43de6-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43de6-128">Requirements</span></span>



| <span data-ttu-id="43de6-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="43de6-129">Requirement</span></span> | <span data-ttu-id="43de6-130">Valor</span><span class="sxs-lookup"><span data-stu-id="43de6-130">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="43de6-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="43de6-131">Header</span></span><br/>  | <dl> <span data-ttu-id="43de6-132"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="43de6-132"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="43de6-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="43de6-133">Library</span></span><br/> | <dl> <span data-ttu-id="43de6-134"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="43de6-134"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="43de6-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="43de6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43de6-136">Funções D3DX</span><span class="sxs-lookup"><span data-stu-id="43de6-136">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

