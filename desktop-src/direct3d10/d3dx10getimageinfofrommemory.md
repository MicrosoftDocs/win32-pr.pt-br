---
description: Obtenha informações sobre uma imagem já carregada na memória.
ms.assetid: 6750116a-ad4f-4102-aba9-6ef32c367be4
title: Função D3DX10GetImageInfoFromMemory (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10GetImageInfoFromMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 677ce6a2ac8e4e165ca0a2bbb64b6254870e4ed8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105761633"
---
# <a name="d3dx10getimageinfofrommemory-function"></a><span data-ttu-id="41af8-103">Função D3DX10GetImageInfoFromMemory</span><span class="sxs-lookup"><span data-stu-id="41af8-103">D3DX10GetImageInfoFromMemory function</span></span>

<span data-ttu-id="41af8-104">Obtenha informações sobre uma imagem já carregada na memória.</span><span class="sxs-lookup"><span data-stu-id="41af8-104">Get information about an image already loaded into memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="41af8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="41af8-105">Syntax</span></span>


```C++
HRESULT D3DX10GetImageInfoFromMemory(
  _In_  LPCVOID           pSrcData,
  _In_  SIZE_T            SrcDataSize,
  _In_  ID3DX10ThreadPump *pPump,
  _In_  D3DX10_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="41af8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="41af8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41af8-107">*pSrcData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="41af8-107">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41af8-108">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41af8-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41af8-109">Ponteiro para a imagem na memória.</span><span class="sxs-lookup"><span data-stu-id="41af8-109">Pointer to the image in memory.</span></span>

</dd> <dt>

<span data-ttu-id="41af8-110">*SrcDataSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="41af8-110">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41af8-111">Tipo: **[ **tamanho \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41af8-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41af8-112">Tamanho da imagem na memória, em bytes.</span><span class="sxs-lookup"><span data-stu-id="41af8-112">Size of the image in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="41af8-113">*pPump* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="41af8-113">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41af8-114">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="41af8-114">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="41af8-115">Bomba de thread opcional que pode ser usada para carregar as informações de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="41af8-115">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="41af8-116">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="41af8-116">Can be **NULL**.</span></span> <span data-ttu-id="41af8-117">Consulte [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="41af8-117">See [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="41af8-118">*pSrcInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="41af8-118">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41af8-119">Tipo: **[ **D3DX10 \_ Image \_ info**](d3dx10-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="41af8-119">Type: **[**D3DX10\_IMAGE\_INFO**](d3dx10-image-info.md)\***</span></span>

<span data-ttu-id="41af8-120">Informações sobre a imagem na memória.</span><span class="sxs-lookup"><span data-stu-id="41af8-120">Information about the image in memory.</span></span>

</dd> <dt>

<span data-ttu-id="41af8-121">*pHResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="41af8-121">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41af8-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="41af8-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="41af8-123">Um ponteiro para o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="41af8-123">A pointer to the return value.</span></span> <span data-ttu-id="41af8-124">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="41af8-124">May be **NULL**.</span></span> <span data-ttu-id="41af8-125">Se *pPump* não for **NULL**, *pHResult* deverá ser um local de memória válido até que a execução assíncrona seja concluída.</span><span class="sxs-lookup"><span data-stu-id="41af8-125">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41af8-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="41af8-126">Return value</span></span>

<span data-ttu-id="41af8-127">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="41af8-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="41af8-128">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="41af8-128">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="41af8-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41af8-129">Requirements</span></span>



| <span data-ttu-id="41af8-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="41af8-130">Requirement</span></span> | <span data-ttu-id="41af8-131">Valor</span><span class="sxs-lookup"><span data-stu-id="41af8-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="41af8-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="41af8-132">Header</span></span><br/>  | <dl> <span data-ttu-id="41af8-133"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="41af8-133"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="41af8-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="41af8-134">Library</span></span><br/> | <dl> <span data-ttu-id="41af8-135"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="41af8-135"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="41af8-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="41af8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41af8-137">Funções de textura no D3DX 10</span><span class="sxs-lookup"><span data-stu-id="41af8-137">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
