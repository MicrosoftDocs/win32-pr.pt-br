---
description: Especifica o modo de controle de taxa.
ms.assetid: 4a0d49b1-30da-4ebe-abff-3fceef6dd94a
title: Propriedade AVEncCommonRateControlMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d18d0d7cb68936326fb4c4ba08188e362fdc91d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163862"
---
# <a name="avenccommonratecontrolmode-property"></a><span data-ttu-id="33aab-103">Propriedade AVEncCommonRateControlMode</span><span class="sxs-lookup"><span data-stu-id="33aab-103">AVEncCommonRateControlMode property</span></span>

<span data-ttu-id="33aab-104">Especifica o modo de controle de taxa.</span><span class="sxs-lookup"><span data-stu-id="33aab-104">Specifies the rate control mode.</span></span>

<span data-ttu-id="33aab-105">Os aplicativos podem definir essa propriedade para especificar o modo de controle de taxa.</span><span class="sxs-lookup"><span data-stu-id="33aab-105">Applications can set this property to specify the rate control mode.</span></span> <span data-ttu-id="33aab-106">Os codificadores também podem retornar essa propriedade como um recurso.</span><span class="sxs-lookup"><span data-stu-id="33aab-106">Encoders can also return this property as a capability.</span></span>

<span data-ttu-id="33aab-107">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="33aab-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="33aab-108">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="33aab-108">Data type</span></span>

<span data-ttu-id="33aab-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="33aab-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="33aab-110">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="33aab-110">Property GUID</span></span>

<span data-ttu-id="33aab-111">**CODECAPI \_ AVEncCommonRateControlMode**</span><span class="sxs-lookup"><span data-stu-id="33aab-111">**CODECAPI\_AVEncCommonRateControlMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="33aab-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="33aab-112">Property value</span></span>

<span data-ttu-id="33aab-113">O valor dessa propriedade é um membro da enumeração [**eAVEncCommonRateControlMode**](/windows/win32/api/codecapi/ne-codecapi-eavenccommonratecontrolmode) .</span><span class="sxs-lookup"><span data-stu-id="33aab-113">The value of this property is a member of the [**eAVEncCommonRateControlMode**](/windows/win32/api/codecapi/ne-codecapi-eavenccommonratecontrolmode) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="33aab-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="33aab-114">Remarks</span></span>

<span data-ttu-id="33aab-115">Essa propriedade também é usada com [codificadores de câmera H. 264 UVC 1,5](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span><span class="sxs-lookup"><span data-stu-id="33aab-115">This property is also used with [H.264 UVC 1.5 camera encoders](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span></span>

<span data-ttu-id="33aab-116">[CODECAPI \_ AVEncVideoTemporalLayerCount](/windows/desktop/medfound/codecapi-avencvideotemporallayercount), [CODECAPI \_ AVEncVideoUsage](/windows/desktop/medfound/codecapi-avencvideousage)e CODECAPI \_ AVEncCommonRateControlMode são propriedades de codificador estáticos.</span><span class="sxs-lookup"><span data-stu-id="33aab-116">[CODECAPI\_AVEncVideoTemporalLayerCount](/windows/desktop/medfound/codecapi-avencvideotemporallayercount), [CODECAPI\_AVEncVideoUsage](/windows/desktop/medfound/codecapi-avencvideousage), and CODECAPI\_AVEncCommonRateControlMode are static encoder properties.</span></span> <span data-ttu-id="33aab-117">Uma vez definido, eles só terão efeito depois que um tipo de mídia definido for chamado no pino de saída da câmera.</span><span class="sxs-lookup"><span data-stu-id="33aab-117">Once set, these will only take effect after a set media type is called on the camera’s output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="33aab-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33aab-118">Requirements</span></span>



| <span data-ttu-id="33aab-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="33aab-119">Requirement</span></span> | <span data-ttu-id="33aab-120">Valor</span><span class="sxs-lookup"><span data-stu-id="33aab-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="33aab-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33aab-121">Minimum supported client</span></span><br/> | <span data-ttu-id="33aab-122">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="33aab-122">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="33aab-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33aab-123">Minimum supported server</span></span><br/> | <span data-ttu-id="33aab-124">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="33aab-124">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="33aab-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="33aab-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="33aab-126"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="33aab-126"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33aab-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="33aab-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33aab-128">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="33aab-128">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="33aab-129">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="33aab-129">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

