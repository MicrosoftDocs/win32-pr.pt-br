---
description: Define a taxa máxima de entrada em tempo real dos quadros de vídeo sendo alimentados no codificador.
ms.assetid: ACBE8799-A81C-44C3-B985-88ADFB1E51B4
title: Propriedade CODECAPI_AVEncMaxFrameRate (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c04d1fd1297f299db133cd98bd493c968fcc29c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748112"
---
# <a name="codecapi_avencmaxframerate-property"></a><span data-ttu-id="fbe72-103">\_Propriedade CODECAPI AVEncMaxFrameRate</span><span class="sxs-lookup"><span data-stu-id="fbe72-103">CODECAPI\_AVEncMaxFrameRate property</span></span>

<span data-ttu-id="fbe72-104">Define a taxa máxima de entrada em tempo real dos quadros de vídeo sendo alimentados no codificador.</span><span class="sxs-lookup"><span data-stu-id="fbe72-104">Sets the maximum real-time input rate of video frames being fed to the encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="fbe72-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="fbe72-105">Data type</span></span>

<span data-ttu-id="fbe72-106">**ULONGULONG** (VT \_ UI8)</span><span class="sxs-lookup"><span data-stu-id="fbe72-106">**ULONGULONG** (VT\_UI8)</span></span>

## <a name="property-guid"></a><span data-ttu-id="fbe72-107">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="fbe72-107">Property GUID</span></span>

<span data-ttu-id="fbe72-108">**CODECAPI \_ AVEncMaxFrameRate**</span><span class="sxs-lookup"><span data-stu-id="fbe72-108">**CODECAPI\_AVEncMaxFrameRate**</span></span>

## <a name="remarks"></a><span data-ttu-id="fbe72-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="fbe72-109">Remarks</span></span>

<span data-ttu-id="fbe72-110">Essa propriedade permite que o chamador especifique a taxa máxima de entrada em tempo real dos quadros de vídeo sendo alimentados no codificador.</span><span class="sxs-lookup"><span data-stu-id="fbe72-110">This property allows the caller to specify the maximum real-time input rate of video frames being fed to the encoder.</span></span> <span data-ttu-id="fbe72-111">Isso dá ao codificador uma indicação da taxa de que precisará processar os quadros de entrada.</span><span class="sxs-lookup"><span data-stu-id="fbe72-111">This gives the encoder an indication of the rate that it will need to process the incoming frames.</span></span> <span data-ttu-id="fbe72-112">Isso é útil para codificadores que se definem em uma configuração de estado de energia específica com base na resolução e na taxa de quadros do vídeo de origem.</span><span class="sxs-lookup"><span data-stu-id="fbe72-112">This is useful for encoders that set themselves into a particular power state configuration based on the resolution and frame-rate of the source video.</span></span>

<span data-ttu-id="fbe72-113">A taxa de quadros é expressa como uma taxa.</span><span class="sxs-lookup"><span data-stu-id="fbe72-113">The frame rate is expressed as a ratio.</span></span> <span data-ttu-id="fbe72-114">Os bits superiores de 32 do valor do atributo contêm o numerador e os bits inferiores de 32 contêm o denominador.</span><span class="sxs-lookup"><span data-stu-id="fbe72-114">The upper 32 bits of the attribute value contain the numerator and the lower 32 bits contain the denominator.</span></span> <span data-ttu-id="fbe72-115">Por exemplo, se a taxa de quadros for de 30 quadros por segundo (FPS), a taxa será 30/1.</span><span class="sxs-lookup"><span data-stu-id="fbe72-115">For example, if the frame rate is 30 frames per second (fps), the ratio is 30/1.</span></span> <span data-ttu-id="fbe72-116">Se a taxa de quadros for de 29,97 fps, a taxa será 30.000/1001.</span><span class="sxs-lookup"><span data-stu-id="fbe72-116">If the frame rate is 29.97 fps, the ratio is 30,000/1001.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbe72-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbe72-117">Requirements</span></span>



| <span data-ttu-id="fbe72-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbe72-118">Requirement</span></span> | <span data-ttu-id="fbe72-119">Valor</span><span class="sxs-lookup"><span data-stu-id="fbe72-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fbe72-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fbe72-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fbe72-121">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="fbe72-121">Windows 10 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="fbe72-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fbe72-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fbe72-123">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="fbe72-123">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fbe72-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fbe72-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbe72-125"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbe72-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbe72-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="fbe72-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbe72-127">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fbe72-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="fbe72-128">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="fbe72-128">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

