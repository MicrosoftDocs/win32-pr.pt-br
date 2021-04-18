---
description: Especifica o nível final do buffer de codificação, em bits, no final do processo de codificação. Essa propriedade só se aplica a constantes de taxa de bits constante (CBR) e a taxa de bits variável (VBR).
ms.assetid: d5bcdf54-061a-436b-8b1a-61ef7d7c90bf
title: Propriedade AVEncCommonBufferOutLevel (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90d99cdea909a1fd1c3777aac4868a570161c3fc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105756657"
---
# <a name="avenccommonbufferoutlevel-property"></a><span data-ttu-id="1560b-104">Propriedade AVEncCommonBufferOutLevel</span><span class="sxs-lookup"><span data-stu-id="1560b-104">AVEncCommonBufferOutLevel property</span></span>

<span data-ttu-id="1560b-105">Especifica o nível final do buffer de codificação, em bits, no final do processo de codificação.</span><span class="sxs-lookup"><span data-stu-id="1560b-105">Specifies the final level of the encoding buffer, in bits, at the end of the encoding process.</span></span> <span data-ttu-id="1560b-106">Essa propriedade só se aplica a constantes de taxa de bits constante (CBR) e a taxa de bits variável (VBR).</span><span class="sxs-lookup"><span data-stu-id="1560b-106">This property applies only to constant bit rate (CBR) and variable bit rate (VBR) encoding modes.</span></span>

<span data-ttu-id="1560b-107">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="1560b-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="1560b-108">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="1560b-108">Data type</span></span>

<span data-ttu-id="1560b-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="1560b-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="1560b-110">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="1560b-110">Property GUID</span></span>

<span data-ttu-id="1560b-111">**CODECAPI \_ AVEncCommonBufferOutLevel**</span><span class="sxs-lookup"><span data-stu-id="1560b-111">**CODECAPI\_AVEncCommonBufferOutLevel**</span></span>

## <a name="property-value"></a><span data-ttu-id="1560b-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="1560b-112">Property value</span></span>

<span data-ttu-id="1560b-113">Esta propriedade tem um intervalo linear de valores.</span><span class="sxs-lookup"><span data-stu-id="1560b-113">This property has a linear range of values.</span></span> <span data-ttu-id="1560b-114">Para obter o intervalo com suporte, chame [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="1560b-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="1560b-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="1560b-115">Remarks</span></span>

<span data-ttu-id="1560b-116">A propriedade estará disponível somente se a duração da codificação for definida com antecedência, usando a propriedade [**AVEncVideoNoOfFieldsToEncode**](avencvideonooffieldstoencode-property.md) ou a propriedade [**AVEncAudioIntervalToEncode**](avencaudiointervaltoencode-property.md) .</span><span class="sxs-lookup"><span data-stu-id="1560b-116">The property is available only if the encoding duration is defined in advance, using the [**AVEncVideoNoOfFieldsToEncode**](avencvideonooffieldstoencode-property.md) property or [**AVEncAudioIntervalToEncode**](avencaudiointervaltoencode-property.md) property.</span></span>

<span data-ttu-id="1560b-117">Para o vídeo MPEG, essa propriedade define a totalidade do verificador de buffer de vídeo (VBV) no final do processo de codificação.</span><span class="sxs-lookup"><span data-stu-id="1560b-117">For MPEG video, this property defines the video buffer verifier (VBV) fullness at the end of the encoding process.</span></span> <span data-ttu-id="1560b-118">Ele dá suporte à concatenação de fluxos durante a codificação.</span><span class="sxs-lookup"><span data-stu-id="1560b-118">It supports the concatenation of streams during encoding.</span></span>

## <a name="requirements"></a><span data-ttu-id="1560b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1560b-119">Requirements</span></span>



| <span data-ttu-id="1560b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1560b-120">Requirement</span></span> | <span data-ttu-id="1560b-121">Valor</span><span class="sxs-lookup"><span data-stu-id="1560b-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1560b-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1560b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1560b-123">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="1560b-123">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="1560b-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1560b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1560b-125">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="1560b-125">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="1560b-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1560b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1560b-127"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1560b-127"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1560b-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="1560b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1560b-129">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="1560b-129">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="1560b-130">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="1560b-130">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




