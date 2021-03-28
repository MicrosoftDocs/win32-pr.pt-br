---
title: Função D3DX11GetImageInfoFromMemory (D3DX11tex. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Observação em vez de usar essa função, recomendamos que você use a biblioteca DirectXTex, GetMetadataFromXXXMemory (em que XXX é o WIC, DDS ou TGA; O WIC não oferece suporte a DDS e TGA; O D3DX 9 TGA com suporte como um formato de origem de arte comum para jogos). Obtenha informações sobre uma imagem já carregada na memória.
ms.assetid: b13192fa-4235-4c38-ba46-e14ffab2f653
keywords:
- Função D3DX11GetImageInfoFromMemory Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11GetImageInfoFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85c5f1f04c9540614541b9f63b7833967d6ce959
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968623"
---
# <a name="d3dx11getimageinfofrommemory-function"></a><span data-ttu-id="a8701-106">Função D3DX11GetImageInfoFromMemory</span><span class="sxs-lookup"><span data-stu-id="a8701-106">D3DX11GetImageInfoFromMemory function</span></span>

> [!Note]  
> <span data-ttu-id="a8701-107">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="a8701-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="a8701-108">Em vez de usar essa função, recomendamos que você use a biblioteca [DirectXTex](https://github.com/Microsoft/DirectXTex) , **GetMetadataFromXXXMemory** (em que xxx é o WIC, DDS ou TGA; O WIC não oferece suporte a DDS e TGA; O D3DX 9 TGA com suporte como um formato de origem de arte comum para jogos).</span><span class="sxs-lookup"><span data-stu-id="a8701-108">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **GetMetadataFromXXXMemory** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>

 

<span data-ttu-id="a8701-109">Obtenha informações sobre uma imagem já carregada na memória.</span><span class="sxs-lookup"><span data-stu-id="a8701-109">Get information about an image already loaded into memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8701-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a8701-110">Syntax</span></span>


```C++
HRESULT D3DX11GetImageInfoFromMemory(
  _In_  LPCVOID           pSrcData,
  _In_  SIZE_T            SrcDataSize,
  _In_  ID3DX11ThreadPump *pPump,
  _In_  D3DX11_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="a8701-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a8701-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8701-112">*pSrcData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a8701-112">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8701-113">Tipo: **[ **LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8701-113">Type: **[**LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a8701-114">Ponteiro para a imagem na memória.</span><span class="sxs-lookup"><span data-stu-id="a8701-114">Pointer to the image in memory.</span></span>

</dd> <dt>

<span data-ttu-id="a8701-115">*SrcDataSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a8701-115">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8701-116">Tipo: **[ **tamanho \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8701-116">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a8701-117">Tamanho da imagem na memória, em bytes.</span><span class="sxs-lookup"><span data-stu-id="a8701-117">Size of the image in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="a8701-118">*pPump* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a8701-118">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8701-119">Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="a8701-119">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="a8701-120">Bomba de thread opcional que pode ser usada para carregar as informações de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="a8701-120">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="a8701-121">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="a8701-121">Can be **NULL**.</span></span> <span data-ttu-id="a8701-122">Consulte a [**interface ID3DX11ThreadPump**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="a8701-122">See [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8701-123">*pSrcInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a8701-123">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8701-124">Tipo: **[ **D3DX11 \_ Image \_ info**](d3dx11-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="a8701-124">Type: **[**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md)\***</span></span>

<span data-ttu-id="a8701-125">Informações sobre a imagem na memória.</span><span class="sxs-lookup"><span data-stu-id="a8701-125">Information about the image in memory.</span></span>

</dd> <dt>

<span data-ttu-id="a8701-126">*pHResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a8701-126">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a8701-127">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="a8701-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="a8701-128">Um ponteiro para o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="a8701-128">A pointer to the return value.</span></span> <span data-ttu-id="a8701-129">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="a8701-129">May be **NULL**.</span></span> <span data-ttu-id="a8701-130">Se *pPump* não for **NULL**, *pHResult* deverá ser um local de memória válido até que a execução assíncrona seja concluída.</span><span class="sxs-lookup"><span data-stu-id="a8701-130">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8701-131">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a8701-131">Return value</span></span>

<span data-ttu-id="a8701-132">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a8701-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a8701-133">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="a8701-133">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a8701-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8701-134">Requirements</span></span>



| <span data-ttu-id="a8701-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8701-135">Requirement</span></span> | <span data-ttu-id="a8701-136">Valor</span><span class="sxs-lookup"><span data-stu-id="a8701-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8701-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a8701-137">Header</span></span><br/>  | <dl> <span data-ttu-id="a8701-138"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8701-138"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="a8701-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a8701-139">Library</span></span><br/> | <dl> <span data-ttu-id="a8701-140"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a8701-140"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="a8701-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="a8701-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8701-142">Funções D3DX</span><span class="sxs-lookup"><span data-stu-id="a8701-142">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

