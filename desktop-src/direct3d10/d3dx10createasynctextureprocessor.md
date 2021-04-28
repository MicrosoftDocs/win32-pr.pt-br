---
description: Função D3DX10CreateAsyncTextureProcessor – crie um processador de dados para ser usado com uma bomba de thread.
ms.assetid: c96b0ebb-7b9c-47d0-ad4f-fa62ddb74fa1
title: Função D3DX10CreateAsyncTextureProcessor (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncTextureProcessor
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e75ab6b796f23399b453a6c7eebfe0d40e3b7b49
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102784"
---
# <a name="d3dx10createasynctextureprocessor-function"></a><span data-ttu-id="a4f78-103">Função D3DX10CreateAsyncTextureProcessor</span><span class="sxs-lookup"><span data-stu-id="a4f78-103">D3DX10CreateAsyncTextureProcessor function</span></span>

<span data-ttu-id="a4f78-104">Crie um processador de dados para ser usado com uma [**bomba de thread**](id3dx10threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="a4f78-104">Create a data processor to be used with a [**thread pump**](id3dx10threadpump.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a4f78-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a4f78-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncTextureProcessor(
  _In_  ID3D10Device           *pDevice,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX10DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="a4f78-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a4f78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4f78-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a4f78-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4f78-108">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="a4f78-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="a4f78-109">Um ponteiro para o devive (consulte a [**interface ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)).</span><span class="sxs-lookup"><span data-stu-id="a4f78-109">A pointer to the devive (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)).</span></span>

</dd> <dt>

<span data-ttu-id="a4f78-110">*pLoadInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a4f78-110">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4f78-111">Tipo: **[ **\_ informações de \_ carregamento \_ de imagem D3DX10**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="a4f78-111">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="a4f78-112">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a4f78-112">Optional.</span></span> <span data-ttu-id="a4f78-113">Identifica as características de uma textura (consulte [**\_ informações de \_ carregamento \_ de imagem D3DX10**](d3dx10-image-load-info.md)) quando o processador de dados é criado; defina isso como **nulo** para ler as características de uma textura quando a textura for carregada.</span><span class="sxs-lookup"><span data-stu-id="a4f78-113">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="a4f78-114">*ppDataProcessor* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a4f78-114">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4f78-115">Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="a4f78-115">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="a4f78-116">Endereço de um ponteiro para um buffer que contém o processador de dados criado (consulte a [**interface ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="a4f78-116">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4f78-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="a4f78-117">Return value</span></span>

<span data-ttu-id="a4f78-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a4f78-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a4f78-119">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="a4f78-119">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a4f78-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4f78-120">Remarks</span></span>

<span data-ttu-id="a4f78-121">Essa API cria uma interface de processador de dados e carrega a textura; [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md) cria a interface do processador de dados.</span><span class="sxs-lookup"><span data-stu-id="a4f78-121">This API does creates a data-processor interface and loads the texture; [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md) creates the data-processor interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4f78-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4f78-122">Requirements</span></span>



| <span data-ttu-id="a4f78-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4f78-123">Requirement</span></span> | <span data-ttu-id="a4f78-124">Valor</span><span class="sxs-lookup"><span data-stu-id="a4f78-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4f78-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a4f78-125">Header</span></span><br/>  | <dl> <span data-ttu-id="a4f78-126"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4f78-126"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="a4f78-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a4f78-127">Library</span></span><br/> | <dl> <span data-ttu-id="a4f78-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a4f78-128"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="a4f78-129">Consulte também</span><span class="sxs-lookup"><span data-stu-id="a4f78-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4f78-130">Funções de textura no D3DX 10</span><span class="sxs-lookup"><span data-stu-id="a4f78-130">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 




