---
description: Crie um processador de dados para ser usado com uma bomba de thread.
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
ms.openlocfilehash: d1d9c61729e72cc4ae5432361e9c1d968551b9c2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012150"
---
# <a name="d3dx10createasynctextureprocessor-function"></a><span data-ttu-id="46eed-103">Função D3DX10CreateAsyncTextureProcessor</span><span class="sxs-lookup"><span data-stu-id="46eed-103">D3DX10CreateAsyncTextureProcessor function</span></span>

<span data-ttu-id="46eed-104">Crie um processador de dados para ser usado com uma [**bomba de thread**](id3dx10threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="46eed-104">Create a data processor to be used with a [**thread pump**](id3dx10threadpump.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="46eed-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="46eed-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncTextureProcessor(
  _In_  ID3D10Device           *pDevice,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX10DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="46eed-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="46eed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46eed-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="46eed-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46eed-108">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="46eed-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="46eed-109">Um ponteiro para o devive (consulte a [**interface ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)).</span><span class="sxs-lookup"><span data-stu-id="46eed-109">A pointer to the devive (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)).</span></span>

</dd> <dt>

<span data-ttu-id="46eed-110">*pLoadInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="46eed-110">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46eed-111">Tipo: **[ **\_ informações de \_ carregamento \_ de imagem D3DX10**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="46eed-111">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="46eed-112">Opcional.</span><span class="sxs-lookup"><span data-stu-id="46eed-112">Optional.</span></span> <span data-ttu-id="46eed-113">Identifica as características de uma textura (consulte [**\_ informações de \_ carregamento \_ de imagem D3DX10**](d3dx10-image-load-info.md)) quando o processador de dados é criado; defina isso como **nulo** para ler as características de uma textura quando a textura for carregada.</span><span class="sxs-lookup"><span data-stu-id="46eed-113">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="46eed-114">*ppDataProcessor* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="46eed-114">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46eed-115">Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="46eed-115">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="46eed-116">Endereço de um ponteiro para um buffer que contém o processador de dados criado (consulte a [**interface ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="46eed-116">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46eed-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="46eed-117">Return value</span></span>

<span data-ttu-id="46eed-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="46eed-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="46eed-119">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="46eed-119">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="46eed-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="46eed-120">Remarks</span></span>

<span data-ttu-id="46eed-121">Essa API cria uma interface de processador de dados e carrega a textura; [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md) cria a interface do processador de dados.</span><span class="sxs-lookup"><span data-stu-id="46eed-121">This API does creates a data-processor interface and loads the texture; [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md) creates the data-processor interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="46eed-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46eed-122">Requirements</span></span>



| <span data-ttu-id="46eed-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="46eed-123">Requirement</span></span> | <span data-ttu-id="46eed-124">Valor</span><span class="sxs-lookup"><span data-stu-id="46eed-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="46eed-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="46eed-125">Header</span></span><br/>  | <dl> <span data-ttu-id="46eed-126"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="46eed-126"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="46eed-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="46eed-127">Library</span></span><br/> | <dl> <span data-ttu-id="46eed-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="46eed-128"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="46eed-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="46eed-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46eed-130">Funções de textura no D3DX 10</span><span class="sxs-lookup"><span data-stu-id="46eed-130">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 




