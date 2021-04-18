---
description: Especifica o sinalizador de informações de produção de áudio em um fluxo de áudio Dolby Digital. Essa propriedade se aplica aos codificadores Dolby Digital Audio.
ms.assetid: 72f5f988-37c3-40d4-9c1c-07086e60ea51
title: Propriedade AVEncDDProductionInfoExists (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5069c8d30f0266b0727f735ede822be491c4a4a2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105785504"
---
# <a name="avencddproductioninfoexists-property"></a><span data-ttu-id="86867-104">Propriedade AVEncDDProductionInfoExists</span><span class="sxs-lookup"><span data-stu-id="86867-104">AVEncDDProductionInfoExists property</span></span>

<span data-ttu-id="86867-105">Especifica o sinalizador de informações de produção de áudio em um fluxo de áudio Dolby Digital.</span><span class="sxs-lookup"><span data-stu-id="86867-105">Specifies the audio production information flag in a Dolby Digital audio stream.</span></span> <span data-ttu-id="86867-106">Essa propriedade se aplica aos codificadores Dolby Digital Audio.</span><span class="sxs-lookup"><span data-stu-id="86867-106">This property applies to Dolby Digital audio encoders.</span></span>

<span data-ttu-id="86867-107">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="86867-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="86867-108">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="86867-108">Data type</span></span>

<span data-ttu-id="86867-109">**Variante \_ BOOL** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="86867-109">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="86867-110">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="86867-110">Property GUID</span></span>

<span data-ttu-id="86867-111">**CODECAPI \_ AVEncDDProductionInfoExists**</span><span class="sxs-lookup"><span data-stu-id="86867-111">**CODECAPI\_AVEncDDProductionInfoExists**</span></span>

## <a name="remarks"></a><span data-ttu-id="86867-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="86867-112">Remarks</span></span>

<span data-ttu-id="86867-113">Se o valor for **Variant \_ true**, as configurações de nível de combinação e de tipo de sala serão válidas.</span><span class="sxs-lookup"><span data-stu-id="86867-113">If the value is **VARIANT\_TRUE**, the mixing level and room type settings are valid.</span></span> <span data-ttu-id="86867-114">Especifique essas configurações com as propriedades [**AVEncDDProductionRoomType**](avencddproductionroomtype-property.md) e [**AVEncDDProductionMixLevel**](avencddproductionmixlevel-property.md) .</span><span class="sxs-lookup"><span data-stu-id="86867-114">Specify these settings with the [**AVEncDDProductionRoomType**](avencddproductionroomtype-property.md) and [**AVEncDDProductionMixLevel**](avencddproductionmixlevel-property.md) properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="86867-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86867-115">Requirements</span></span>



| <span data-ttu-id="86867-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="86867-116">Requirement</span></span> | <span data-ttu-id="86867-117">Valor</span><span class="sxs-lookup"><span data-stu-id="86867-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="86867-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="86867-118">Minimum supported client</span></span><br/> | <span data-ttu-id="86867-119">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="86867-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="86867-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="86867-120">Minimum supported server</span></span><br/> | <span data-ttu-id="86867-121">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="86867-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="86867-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="86867-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="86867-123"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="86867-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86867-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="86867-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86867-125">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="86867-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="86867-126">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="86867-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




