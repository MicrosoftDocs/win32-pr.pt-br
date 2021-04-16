---
description: Retorna o número de quadros de vídeo recebidos pelo codificador.
ms.assetid: 3de49105-3c74-4a52-9cac-465b4abfcbf5
title: Propriedade AVEncStatVideoTotalFrames (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d76adda51e6d16676a2a957fd16a5aac2a15691e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105747623"
---
# <a name="avencstatvideototalframes-property"></a><span data-ttu-id="3752d-103">Propriedade AVEncStatVideoTotalFrames</span><span class="sxs-lookup"><span data-stu-id="3752d-103">AVEncStatVideoTotalFrames property</span></span>

<span data-ttu-id="3752d-104">Retorna o número de quadros de vídeo recebidos pelo codificador.</span><span class="sxs-lookup"><span data-stu-id="3752d-104">Returns the number of video frames that the encoder received.</span></span>

<span data-ttu-id="3752d-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="3752d-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="3752d-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="3752d-106">Data type</span></span>

<span data-ttu-id="3752d-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="3752d-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="3752d-108">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="3752d-108">Property GUID</span></span>

<span data-ttu-id="3752d-109">**CODECAPI \_ AVEncStatVideoTotalFrames**</span><span class="sxs-lookup"><span data-stu-id="3752d-109">**CODECAPI\_AVEncStatVideoTotalFrames**</span></span>

## <a name="remarks"></a><span data-ttu-id="3752d-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="3752d-110">Remarks</span></span>

<span data-ttu-id="3752d-111">Essa propriedade estará disponível após a conclusão da codificação.</span><span class="sxs-lookup"><span data-stu-id="3752d-111">This property is available after the encoding is completed.</span></span>

<span data-ttu-id="3752d-112">O valor dessa propriedade é o número total de quadros enviados ao codificador, incluindo os quadros que foram descartados.</span><span class="sxs-lookup"><span data-stu-id="3752d-112">The value of this property is the total number of frames sent to the encoder, including frames that were dropped.</span></span> <span data-ttu-id="3752d-113">Para obter o número de quadros codificados, leia a propriedade [**AVEncStatVideoCodedFrames**](avencstatvideocodedframes-property.md) .</span><span class="sxs-lookup"><span data-stu-id="3752d-113">To get the number of encoded frames, read the [**AVEncStatVideoCodedFrames**](avencstatvideocodedframes-property.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="3752d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3752d-114">Requirements</span></span>



| <span data-ttu-id="3752d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3752d-115">Requirement</span></span> | <span data-ttu-id="3752d-116">Valor</span><span class="sxs-lookup"><span data-stu-id="3752d-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3752d-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3752d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3752d-118">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="3752d-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="3752d-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3752d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3752d-120">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="3752d-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="3752d-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3752d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3752d-122"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3752d-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3752d-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="3752d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3752d-124">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="3752d-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="3752d-125">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="3752d-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




