---
description: Especifica o modo de downmix de estéreo preferencial para um fluxo de áudio Dolby Digital. Essa propriedade se aplica aos codificadores Dolby Digital Audio.
ms.assetid: 3cf9fba7-6895-4dfb-9aef-571c512b7955
title: Propriedade AVEncDDPreferredStereoDownMixMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aea695491175c8cb7d769673fcb09dd6ad2ae9f6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825952"
---
# <a name="avencddpreferredstereodownmixmode-property"></a><span data-ttu-id="cb4de-104">Propriedade AVEncDDPreferredStereoDownMixMode</span><span class="sxs-lookup"><span data-stu-id="cb4de-104">AVEncDDPreferredStereoDownMixMode property</span></span>

<span data-ttu-id="cb4de-105">Especifica o modo de downmix de estéreo preferencial para um fluxo de áudio Dolby Digital.</span><span class="sxs-lookup"><span data-stu-id="cb4de-105">Specifies the preferred stereo downmix mode for a Dolby Digital audio stream.</span></span> <span data-ttu-id="cb4de-106">Essa propriedade se aplica aos codificadores Dolby Digital Audio.</span><span class="sxs-lookup"><span data-stu-id="cb4de-106">This property applies to Dolby Digital audio encoders.</span></span>

<span data-ttu-id="cb4de-107">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="cb4de-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="cb4de-108">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="cb4de-108">Data type</span></span>

<span data-ttu-id="cb4de-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="cb4de-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="cb4de-110">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="cb4de-110">Property GUID</span></span>

<span data-ttu-id="cb4de-111">**CODECAPI \_ AVEncDDPreferredStereoDownMixMode**</span><span class="sxs-lookup"><span data-stu-id="cb4de-111">**CODECAPI\_AVEncDDPreferredStereoDownMixMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="cb4de-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="cb4de-112">Property value</span></span>

<span data-ttu-id="cb4de-113">O valor dessa propriedade é um membro da enumeração [**eAVEncDDPreferredStereoDownMixMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencddpreferredstereodownmixmode) .</span><span class="sxs-lookup"><span data-stu-id="cb4de-113">The value of this property is a member of the [**eAVEncDDPreferredStereoDownMixMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencddpreferredstereodownmixmode) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb4de-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="cb4de-114">Remarks</span></span>

<span data-ttu-id="cb4de-115">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="cb4de-115">This property is read/write.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb4de-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb4de-116">Requirements</span></span>



| <span data-ttu-id="cb4de-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb4de-117">Requirement</span></span> | <span data-ttu-id="cb4de-118">Valor</span><span class="sxs-lookup"><span data-stu-id="cb4de-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cb4de-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cb4de-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cb4de-120">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="cb4de-120">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="cb4de-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cb4de-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cb4de-122">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="cb4de-122">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="cb4de-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cb4de-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb4de-124"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb4de-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb4de-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="cb4de-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb4de-126">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="cb4de-126">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="cb4de-127">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="cb4de-127">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




