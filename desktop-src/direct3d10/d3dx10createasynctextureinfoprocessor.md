---
description: Crie um processador de dados para ser usado com uma bomba de thread.
ms.assetid: e97b6aca-1839-48ea-8dab-b96a52ec2a68
title: Função D3DX10CreateAsyncTextureInfoProcessor (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncTextureInfoProcessor
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fe56fc217af6ebae9255b4f72d3c3af2f279fa29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105815448"
---
# <a name="d3dx10createasynctextureinfoprocessor-function"></a><span data-ttu-id="2d6e6-103">Função D3DX10CreateAsyncTextureInfoProcessor</span><span class="sxs-lookup"><span data-stu-id="2d6e6-103">D3DX10CreateAsyncTextureInfoProcessor function</span></span>

<span data-ttu-id="2d6e6-104">Crie um processador de dados para ser usado com uma [**bomba de thread**](id3dx10threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="2d6e6-104">Create a data processor to be used with a [**thread pump**](id3dx10threadpump.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2d6e6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2d6e6-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncTextureInfoProcessor(
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX10DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="2d6e6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2d6e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d6e6-107">*pLoadInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2d6e6-107">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d6e6-108">Tipo: **[ **\_ informações de \_ carregamento \_ de imagem D3DX10**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="2d6e6-108">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="2d6e6-109">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2d6e6-109">Optional.</span></span> <span data-ttu-id="2d6e6-110">Identifica as características de uma textura (consulte [**\_ informações de \_ carregamento \_ de imagem D3DX10**](d3dx10-image-load-info.md)) quando o processador de dados é criado; defina isso como **nulo** para ler as características de uma textura quando a textura for carregada.</span><span class="sxs-lookup"><span data-stu-id="2d6e6-110">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="2d6e6-111">*ppDataProcessor* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2d6e6-111">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d6e6-112">Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="2d6e6-112">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="2d6e6-113">Endereço de um ponteiro para um buffer que contém o processador de dados criado (consulte a [**interface ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="2d6e6-113">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d6e6-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2d6e6-114">Return value</span></span>

<span data-ttu-id="2d6e6-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2d6e6-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2d6e6-116">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="2d6e6-116">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2d6e6-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="2d6e6-117">Remarks</span></span>

<span data-ttu-id="2d6e6-118">Essa API cria uma interface de processador de dados; [**D3DX10CreateAsyncTextureProcessor**](d3dx10createasynctextureprocessor.md) cria a interface do processador de dados e carrega a textura.</span><span class="sxs-lookup"><span data-stu-id="2d6e6-118">This API does creates a data-processor interface; [**D3DX10CreateAsyncTextureProcessor**](d3dx10createasynctextureprocessor.md) creates the data-processor interface and loads the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d6e6-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d6e6-119">Requirements</span></span>



| <span data-ttu-id="2d6e6-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d6e6-120">Requirement</span></span> | <span data-ttu-id="2d6e6-121">Valor</span><span class="sxs-lookup"><span data-stu-id="2d6e6-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d6e6-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2d6e6-122">Header</span></span><br/>  | <dl> <span data-ttu-id="2d6e6-123"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d6e6-123"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="2d6e6-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2d6e6-124">Library</span></span><br/> | <dl> <span data-ttu-id="2d6e6-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d6e6-125"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="2d6e6-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="2d6e6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d6e6-127">Funções de textura no D3DX 10</span><span class="sxs-lookup"><span data-stu-id="2d6e6-127">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 




