---
description: Crie um processador de dados que carregará um recurso e, em seguida, crie uma exibição de recurso de sombreador para ele. Os processadores de dados são um componente do recurso de carregamento de dados assíncronos no D3DX10 que usa bombas de thread.
ms.assetid: 6e5a6138-c218-4200-a24e-d906d34933b8
title: Função D3DX10CreateAsyncShaderResourceViewProcessor (D3DX10Async. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncShaderResourceViewProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: bd55e4191382c5abde52ce05d0a16b5533d79eac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105787636"
---
# <a name="d3dx10createasyncshaderresourceviewprocessor-function"></a><span data-ttu-id="472ae-104">Função D3DX10CreateAsyncShaderResourceViewProcessor</span><span class="sxs-lookup"><span data-stu-id="472ae-104">D3DX10CreateAsyncShaderResourceViewProcessor function</span></span>

<span data-ttu-id="472ae-105">Crie um processador de dados que carregará um recurso e, em seguida, crie uma exibição de recurso de sombreador para ele.</span><span class="sxs-lookup"><span data-stu-id="472ae-105">Create a data processor that will load a resource and then create a shader-resource view for it.</span></span> <span data-ttu-id="472ae-106">Os processadores de dados são um componente do recurso de carregamento de dados assíncronos no D3DX10 que usa [**bombas de thread**](id3dx10threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="472ae-106">Data processors are a component of the asynchronous data loading feature in D3DX10 that uses [**thread pumps**](id3dx10threadpump.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="472ae-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="472ae-107">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncShaderResourceViewProcessor(
  _In_  ID3D10Device           *pDevice,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX10DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="472ae-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="472ae-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="472ae-109">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="472ae-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="472ae-110">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="472ae-110">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="472ae-111">Ponteiro para o dispositivo Direct3D (consulte a [**interface ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) que será usado para criar um recurso e uma exibição de recurso de sombreador para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="472ae-111">Pointer to the Direct3D device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will be used to create a resource and a shader-resource view for that resource.</span></span>

</dd> <dt>

<span data-ttu-id="472ae-112">*pLoadInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="472ae-112">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="472ae-113">Tipo: **[ **\_ informações de \_ carregamento \_ de imagem D3DX10**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="472ae-113">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="472ae-114">Opcional.</span><span class="sxs-lookup"><span data-stu-id="472ae-114">Optional.</span></span> <span data-ttu-id="472ae-115">Identifica as características de uma textura (consulte [**\_ informações de \_ carregamento \_ de imagem D3DX10**](d3dx10-image-load-info.md)) quando o processador de dados é criado; defina isso como **nulo** para ler as características de uma textura quando a textura for carregada.</span><span class="sxs-lookup"><span data-stu-id="472ae-115">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="472ae-116">*ppDataProcessor* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="472ae-116">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="472ae-117">Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="472ae-117">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="472ae-118">Endereço de um ponteiro para um buffer que contém o processador de dados criado (consulte a [**interface ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="472ae-118">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="472ae-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="472ae-119">Return value</span></span>

<span data-ttu-id="472ae-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="472ae-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="472ae-121">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="472ae-121">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="472ae-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="472ae-122">Requirements</span></span>



| <span data-ttu-id="472ae-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="472ae-123">Requirement</span></span> | <span data-ttu-id="472ae-124">Valor</span><span class="sxs-lookup"><span data-stu-id="472ae-124">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="472ae-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="472ae-125">Header</span></span><br/> | <dl> <span data-ttu-id="472ae-126"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="472ae-126"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="472ae-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="472ae-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="472ae-128">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="472ae-128">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 




