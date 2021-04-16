---
description: Especifica a taxa média de bits codificada, em bits por segundo. Essa propriedade só se aplica a constantes de taxa de bits constante (CBR) e a taxa de bits variável (VBR).
ms.assetid: 8519685a-4f5b-44af-ad46-09eba7a198c6
title: Propriedade AVEncCommonMeanBitRate (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4eaec7fc6578e6e69a45616ee6de059bb7a378b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500655"
---
# <a name="avenccommonmeanbitrate-property"></a><span data-ttu-id="b5142-104">Propriedade AVEncCommonMeanBitRate</span><span class="sxs-lookup"><span data-stu-id="b5142-104">AVEncCommonMeanBitRate property</span></span>

<span data-ttu-id="b5142-105">Especifica a taxa média de bits codificada, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="b5142-105">Specifies the average encoded bit rate, in bits per second.</span></span> <span data-ttu-id="b5142-106">Essa propriedade só se aplica a constantes de taxa de bits constante (CBR) e a taxa de bits variável (VBR).</span><span class="sxs-lookup"><span data-stu-id="b5142-106">This property applies only to constant bit rate (CBR) and variable bit rate (VBR) encoding modes.</span></span>

<span data-ttu-id="b5142-107">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="b5142-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="b5142-108">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b5142-108">Data type</span></span>

<span data-ttu-id="b5142-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="b5142-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="b5142-110">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="b5142-110">Property GUID</span></span>

<span data-ttu-id="b5142-111">**CODECAPI \_ AVEncCommonMeanBitRate**</span><span class="sxs-lookup"><span data-stu-id="b5142-111">**CODECAPI\_AVEncCommonMeanBitRate**</span></span>

## <a name="property-value"></a><span data-ttu-id="b5142-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="b5142-112">Property value</span></span>

<span data-ttu-id="b5142-113">Os codificadores podem implementar essa propriedade como um conjunto enumerado ou como um intervalo linear.</span><span class="sxs-lookup"><span data-stu-id="b5142-113">Encoders can implement this property as an enumerated set or as a linear range.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5142-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b5142-114">Remarks</span></span>

<span data-ttu-id="b5142-115">Essa propriedade também é usada com [codificadores de câmera H. 264 UVC 1,5](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span><span class="sxs-lookup"><span data-stu-id="b5142-115">This property is also used with [H.264 UVC 1.5 camera encoders](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span></span>

## <a name="requirements"></a><span data-ttu-id="b5142-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5142-116">Requirements</span></span>



| <span data-ttu-id="b5142-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5142-117">Requirement</span></span> | <span data-ttu-id="b5142-118">Valor</span><span class="sxs-lookup"><span data-stu-id="b5142-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b5142-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5142-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b5142-120">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b5142-120">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="b5142-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5142-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b5142-122">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b5142-122">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="b5142-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b5142-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5142-124"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5142-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5142-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="b5142-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5142-126">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="b5142-126">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="b5142-127">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="b5142-127">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

