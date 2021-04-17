---
description: Especifica se o coletor de amostra de exemplo usa o relógio de apresentação para agendar exemplos.
ms.assetid: 780ec4a6-8e14-4b81-9d50-82b2850c70ae
title: Atributo MF_SAMPLEGRABBERSINK_IGNORE_CLOCK (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57ad5476779d958bdbf94af554d889dd8d174ca3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771383"
---
# <a name="mf_samplegrabbersink_ignore_clock-attribute"></a><span data-ttu-id="102fb-103">\_Atributo de \_ relógio de ignorar SAMPLEGRABBERSINK MF \_</span><span class="sxs-lookup"><span data-stu-id="102fb-103">MF\_SAMPLEGRABBERSINK\_IGNORE\_CLOCK attribute</span></span>

<span data-ttu-id="102fb-104">Especifica se o coletor de amostra de exemplo usa o relógio de apresentação para agendar exemplos.</span><span class="sxs-lookup"><span data-stu-id="102fb-104">Specifies whether the sample-grabber sink uses the presentation clock to schedule samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="102fb-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="102fb-105">Data type</span></span>

<span data-ttu-id="102fb-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="102fb-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="102fb-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="102fb-107">Get/set</span></span>

<span data-ttu-id="102fb-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="102fb-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="102fb-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="102fb-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="102fb-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="102fb-110">Remarks</span></span>

<span data-ttu-id="102fb-111">Você pode definir esse atributo no objeto de ativação criado pela função [**MFCreateSampleGrabberSinkActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) .</span><span class="sxs-lookup"><span data-stu-id="102fb-111">You can set this attribute on the activation object created by the [**MFCreateSampleGrabberSinkActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) function.</span></span> <span data-ttu-id="102fb-112">Defina o atributo antes de chamar o método [**IMFActivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) no objeto de ativação.</span><span class="sxs-lookup"><span data-stu-id="102fb-112">Set the attribute before calling the [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) method on the activation object.</span></span>

<span data-ttu-id="102fb-113">Por padrão, quando o coletor de amostra de exemplo recebe um exemplo, ele aguarda até que o tempo de apresentação do exemplo invoque o retorno de chamada do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="102fb-113">By default, when the sample-grabber sink receives a sample, it waits until the presentation time of the sample to invoke the application's callback.</span></span> <span data-ttu-id="102fb-114">Se o \_ atributo de relógio MF SAMPLEGRABBERSINK \_ ignorar \_ for diferente de zero, o coletor de apoio de exemplo ignorará o relógio de apresentação e invocará o retorno de chamada assim que receber cada exemplo.</span><span class="sxs-lookup"><span data-stu-id="102fb-114">If the MF\_SAMPLEGRABBERSINK\_IGNORE\_CLOCK attribute is nonzero, the sample-grabber sink ignores the presentation clock and invokes the callback as soon as it receives each sample.</span></span>

<span data-ttu-id="102fb-115">Uso recomendado:</span><span class="sxs-lookup"><span data-stu-id="102fb-115">Recommended usage:</span></span>

-   <span data-ttu-id="102fb-116">Se você quiser processar amostras o mais rápido possível, defina esse atributo como **true**.</span><span class="sxs-lookup"><span data-stu-id="102fb-116">If you want to process samples as quickly as possible, set this attribute to **TRUE**.</span></span>
-   <span data-ttu-id="102fb-117">Se você quiser que as chamadas para o método de retorno de chamada sejam sincronizadas com o relógio, não defina esse atributo ou defina-o como **false**.</span><span class="sxs-lookup"><span data-stu-id="102fb-117">If you want the calls to the callback method to be synchronized with the clock, either do not set this attribute or set it to **FALSE**.</span></span> <span data-ttu-id="102fb-118">Você pode obter amostras levemente antes do relógio, enquanto ainda permaneceu sincronizado, definindo o atributo de [**\_ deslocamento de \_ \_ tempo \_ de exemplo SAMPLEGRABBERSINK MF**](mf-samplegrabbersink-sample-time-offset-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="102fb-118">You can get samples slightly ahead of the clock, while still remaining synchronized, by setting the [**MF\_SAMPLEGRABBERSINK\_SAMPLE\_TIME\_OFFSET**](mf-samplegrabbersink-sample-time-offset-attribute.md) attribute.</span></span>

<span data-ttu-id="102fb-119">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="102fb-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="102fb-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="102fb-120">Requirements</span></span>



| <span data-ttu-id="102fb-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="102fb-121">Requirement</span></span> | <span data-ttu-id="102fb-122">Valor</span><span class="sxs-lookup"><span data-stu-id="102fb-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="102fb-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="102fb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="102fb-124">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="102fb-124">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="102fb-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="102fb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="102fb-126">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="102fb-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="102fb-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="102fb-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="102fb-128"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="102fb-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="102fb-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="102fb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="102fb-130">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="102fb-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="102fb-131">Atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="102fb-131">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 




