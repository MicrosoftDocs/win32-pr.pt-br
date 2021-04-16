---
description: A função CheckVideoInfo2Type verifica um tipo de mídia que contém uma estrutura de formato VIDEOINFOHEADER2 para determinados erros comuns que podem causar saturações de buffer ou estouros de inteiros.
ms.assetid: 6a71ce7e-c6fc-4811-9182-67949644a0a5
title: Função CheckVideoInfo2Type (Checkbmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CheckVideoInfo2Type
api_type:
- HeaderDef
api_location:
- checkbmi.h
ms.openlocfilehash: 5ec092bdea1e3dd00de36893d1816f70ca6d7945
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105786993"
---
# <a name="checkvideoinfo2type-function"></a><span data-ttu-id="19a71-103">Função CheckVideoInfo2Type</span><span class="sxs-lookup"><span data-stu-id="19a71-103">CheckVideoInfo2Type function</span></span>

<span data-ttu-id="19a71-104">A `CheckVideoInfo2Type` função verifica um tipo de mídia que contém uma estrutura de formato [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) para determinados erros comuns que podem causar saturações de buffer ou estouros de inteiros.</span><span class="sxs-lookup"><span data-stu-id="19a71-104">The `CheckVideoInfo2Type` function checks a media type that contains a [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format structure for certain common errors that can cause buffer overruns or integer overflows.</span></span>

> [!Note]  
> <span data-ttu-id="19a71-105">Essa função não garante que o tipo de mídia seja válido ou que o código que usa a estrutura seja seguro.</span><span class="sxs-lookup"><span data-stu-id="19a71-105">This function does not guarantee that the media type is valid or that code using the structure is secure.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="19a71-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="19a71-106">Syntax</span></span>


```C++
HRESULT CheckVideoInfo2Type(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="19a71-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="19a71-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19a71-108">*PMT*</span><span class="sxs-lookup"><span data-stu-id="19a71-108">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="19a71-109">Ponteiro para a estrutura do [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) a ser validada.</span><span class="sxs-lookup"><span data-stu-id="19a71-109">Pointer to the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure to validate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19a71-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="19a71-110">Return value</span></span>

<span data-ttu-id="19a71-111">Retorna um dos valores de **HRESULT** a seguir.</span><span class="sxs-lookup"><span data-stu-id="19a71-111">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="19a71-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="19a71-112">Return code</span></span>                                                                                                | <span data-ttu-id="19a71-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="19a71-113">Description</span></span>                       |
|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="19a71-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="19a71-114"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="19a71-115">Sucesso</span><span class="sxs-lookup"><span data-stu-id="19a71-115">Success</span></span><br/>                |
| <dl> <span data-ttu-id="19a71-116"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="19a71-116"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="19a71-117">Valor de ponteiro **nulo**</span><span class="sxs-lookup"><span data-stu-id="19a71-117">**NULL** pointer value</span></span><br/> |
| <dl> <span data-ttu-id="19a71-118"><dt>**\_tipo E \_ VFW \_ não \_ aceito**</dt></span><span class="sxs-lookup"><span data-stu-id="19a71-118"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="19a71-119">Tipo de mídia inválido</span><span class="sxs-lookup"><span data-stu-id="19a71-119">Invalid media type</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="19a71-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="19a71-120">Remarks</span></span>

<span data-ttu-id="19a71-121">Essa função chama [**ValidateBitmapInfoHeader**](validatebitmapinfoheader.md) para validar a estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) no tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="19a71-121">This function calls [**ValidateBitmapInfoHeader**](validatebitmapinfoheader.md) to validate the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure in the media type.</span></span> <span data-ttu-id="19a71-122">Se o tipo de formato não for **Format \_ VideoInfo2**, a função retornará **VFW \_ E \_ tipo \_ não \_ aceito**.</span><span class="sxs-lookup"><span data-stu-id="19a71-122">If the format type is not **FORMAT\_VideoInfo2**, the function returns **VFW\_E\_TYPE\_NOT\_ACCEPTED**.</span></span>

## <a name="requirements"></a><span data-ttu-id="19a71-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19a71-123">Requirements</span></span>



| <span data-ttu-id="19a71-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="19a71-124">Requirement</span></span> | <span data-ttu-id="19a71-125">Valor</span><span class="sxs-lookup"><span data-stu-id="19a71-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="19a71-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="19a71-126">Header</span></span><br/> | <dl> <span data-ttu-id="19a71-127"><dt>Checkbmi. h</dt></span><span class="sxs-lookup"><span data-stu-id="19a71-127"><dt>Checkbmi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19a71-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="19a71-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19a71-129">Funções de vídeo e imagem</span><span class="sxs-lookup"><span data-stu-id="19a71-129">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




