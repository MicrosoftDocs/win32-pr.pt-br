---
description: Especifica o nível de combinação, em decibéis (dB), em um fluxo de áudio Dolby Digital. Essa propriedade se aplica aos codificadores Dolby Digital Audio.
ms.assetid: fcb16d02-af4f-4626-99ee-2831172e5280
title: Propriedade AVEncDDProductionMixLevel (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8a1726db6ab4841b4603a61bcfe39504742db42
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105758889"
---
# <a name="avencddproductionmixlevel-property"></a><span data-ttu-id="16bfa-104">Propriedade AVEncDDProductionMixLevel</span><span class="sxs-lookup"><span data-stu-id="16bfa-104">AVEncDDProductionMixLevel property</span></span>

<span data-ttu-id="16bfa-105">Especifica o nível de combinação, em decibéis (dB), em um fluxo de áudio Dolby Digital.</span><span class="sxs-lookup"><span data-stu-id="16bfa-105">Specifies the mixing level, in decibels (dB), in a Dolby Digital audio stream.</span></span> <span data-ttu-id="16bfa-106">Essa propriedade se aplica aos codificadores Dolby Digital Audio.</span><span class="sxs-lookup"><span data-stu-id="16bfa-106">This property applies to Dolby Digital audio encoders.</span></span>

<span data-ttu-id="16bfa-107">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="16bfa-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="16bfa-108">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="16bfa-108">Data type</span></span>

<span data-ttu-id="16bfa-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="16bfa-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="16bfa-110">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="16bfa-110">Property GUID</span></span>

<span data-ttu-id="16bfa-111">**CODECAPI \_ AVEncDDProductionMixLevel**</span><span class="sxs-lookup"><span data-stu-id="16bfa-111">**CODECAPI\_AVEncDDProductionMixLevel**</span></span>

## <a name="property-value"></a><span data-ttu-id="16bfa-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="16bfa-112">Property value</span></span>

<span data-ttu-id="16bfa-113">Esta propriedade tem um intervalo linear de valores.</span><span class="sxs-lookup"><span data-stu-id="16bfa-113">This property has a linear range of values.</span></span> <span data-ttu-id="16bfa-114">Para obter o intervalo com suporte, chame [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="16bfa-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="16bfa-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="16bfa-115">Remarks</span></span>

<span data-ttu-id="16bfa-116">Se você definir essa propriedade, defina a propriedade [**AVEncDDProductionInfoExists**](avencddproductioninfoexists-property.md) como **true**.</span><span class="sxs-lookup"><span data-stu-id="16bfa-116">If you set this property, set the [**AVEncDDProductionInfoExists**](avencddproductioninfoexists-property.md) property to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="16bfa-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16bfa-117">Requirements</span></span>



| <span data-ttu-id="16bfa-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="16bfa-118">Requirement</span></span> | <span data-ttu-id="16bfa-119">Valor</span><span class="sxs-lookup"><span data-stu-id="16bfa-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="16bfa-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16bfa-120">Minimum supported client</span></span><br/> | <span data-ttu-id="16bfa-121">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="16bfa-121">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="16bfa-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16bfa-122">Minimum supported server</span></span><br/> | <span data-ttu-id="16bfa-123">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="16bfa-123">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="16bfa-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="16bfa-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="16bfa-125"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="16bfa-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16bfa-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="16bfa-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16bfa-127">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="16bfa-127">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="16bfa-128">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="16bfa-128">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




