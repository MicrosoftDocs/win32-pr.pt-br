---
description: A função CheckVideoInfoType verifica um tipo de mídia que contém uma estrutura de formato VIDEOINFOHEADER para determinados erros comuns que podem causar saturações de buffer ou estouros de inteiros.
ms.assetid: 7ffca7de-26f9-4d8d-b70e-231eca462211
title: Função CheckVideoInfoType (Checkbmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CheckVideoInfoType
api_type:
- HeaderDef
api_location:
- checkbmi.h
ms.openlocfilehash: 7c3a3c9603f974458ed3012dc651815abd432645
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749017"
---
# <a name="checkvideoinfotype-function"></a><span data-ttu-id="3e8d5-103">Função CheckVideoInfoType</span><span class="sxs-lookup"><span data-stu-id="3e8d5-103">CheckVideoInfoType function</span></span>

<span data-ttu-id="3e8d5-104">A `CheckVideoInfoType` função verifica um tipo de mídia que contém uma estrutura de formato [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) para determinados erros comuns que podem causar saturações de buffer ou estouros de inteiros.</span><span class="sxs-lookup"><span data-stu-id="3e8d5-104">The `CheckVideoInfoType` function checks a media type that contains a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) format structure for certain common errors that can cause buffer overruns or integer overflows.</span></span>

> [!Note]  
> <span data-ttu-id="3e8d5-105">Essa função não garante que o tipo de mídia seja válido ou que o código que usa a estrutura seja seguro.</span><span class="sxs-lookup"><span data-stu-id="3e8d5-105">This function does not guarantee that the media type is valid or that code using the structure is secure.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="3e8d5-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3e8d5-106">Syntax</span></span>


```C++
HRESULT CheckVideoInfoType(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="3e8d5-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3e8d5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e8d5-108">*PMT*</span><span class="sxs-lookup"><span data-stu-id="3e8d5-108">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="3e8d5-109">Ponteiro para a estrutura do [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) para validar</span><span class="sxs-lookup"><span data-stu-id="3e8d5-109">Pointer to the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure to validate</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e8d5-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3e8d5-110">Return value</span></span>

<span data-ttu-id="3e8d5-111">Retorna um dos valores de **HRESULT** a seguir.</span><span class="sxs-lookup"><span data-stu-id="3e8d5-111">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="3e8d5-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="3e8d5-112">Return code</span></span>                                                                                                | <span data-ttu-id="3e8d5-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="3e8d5-113">Description</span></span>                        |
|------------------------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <span data-ttu-id="3e8d5-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3e8d5-114"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="3e8d5-115">Êxito.</span><span class="sxs-lookup"><span data-stu-id="3e8d5-115">Success.</span></span><br/>                |
| <dl> <span data-ttu-id="3e8d5-116"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="3e8d5-116"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="3e8d5-117">Valor de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="3e8d5-117">**NULL** pointer value.</span></span><br/> |
| <dl> <span data-ttu-id="3e8d5-118"><dt>**\_tipo E \_ VFW \_ não \_ aceito**</dt></span><span class="sxs-lookup"><span data-stu-id="3e8d5-118"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="3e8d5-119">Tipo de mídia inválido.</span><span class="sxs-lookup"><span data-stu-id="3e8d5-119">Invalid media type.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="3e8d5-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e8d5-120">Remarks</span></span>

<span data-ttu-id="3e8d5-121">Essa função chama [**ValidateBitmapInfoHeader**](validatebitmapinfoheader.md) para validar a estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) no tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="3e8d5-121">This function calls [**ValidateBitmapInfoHeader**](validatebitmapinfoheader.md) to validate the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure in the media type.</span></span> <span data-ttu-id="3e8d5-122">Se o tipo de formato não for FORMAT \_ VIDEOINFO, a função retornará VFW \_ E \_ tipo \_ não \_ aceito.</span><span class="sxs-lookup"><span data-stu-id="3e8d5-122">If the format type is not FORMAT\_VideoInfo, the function returns VFW\_E\_TYPE\_NOT\_ACCEPTED.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e8d5-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e8d5-123">Requirements</span></span>



| <span data-ttu-id="3e8d5-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e8d5-124">Requirement</span></span> | <span data-ttu-id="3e8d5-125">Valor</span><span class="sxs-lookup"><span data-stu-id="3e8d5-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3e8d5-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3e8d5-126">Header</span></span><br/> | <dl> <span data-ttu-id="3e8d5-127"><dt>Checkbmi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e8d5-127"><dt>Checkbmi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e8d5-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e8d5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e8d5-129">Funções de vídeo e imagem</span><span class="sxs-lookup"><span data-stu-id="3e8d5-129">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




