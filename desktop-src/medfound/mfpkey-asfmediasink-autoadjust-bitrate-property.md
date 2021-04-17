---
description: Especifica se o coletor de mídia ASF ajusta automaticamente a taxa de bits.
ms.assetid: 0a6f4dd4-4ad7-4aab-a33d-14b4716f9902
title: Propriedade MFPKEY_ASFMEDIASINK_AUTOADJUST_BITRATE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2d22463f477eb5abc1bb84254ad312427ecef52
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105763264"
---
# <a name="mfpkey_asfmediasink_autoadjust_bitrate-property"></a><span data-ttu-id="90831-103">\_Propriedade MFPKEY ASFMEDIASINK \_ autoadjust \_ taxa de bits</span><span class="sxs-lookup"><span data-stu-id="90831-103">MFPKEY\_ASFMEDIASINK\_AUTOADJUST\_BITRATE property</span></span>

<span data-ttu-id="90831-104">Especifica se o coletor de mídia ASF ajusta automaticamente a taxa de bits.</span><span class="sxs-lookup"><span data-stu-id="90831-104">Specifies whether the ASF media sink automatically adjusts the bit rate.</span></span>



<span data-ttu-id="90831-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="90831-105">Data type</span></span>

<span data-ttu-id="90831-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="90831-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="90831-107">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="90831-107">PROPVARIANT member</span></span>

<span data-ttu-id="90831-108">**BOOL de variante \_**</span><span class="sxs-lookup"><span data-stu-id="90831-108">**VARIANT\_BOOL**</span></span>

<span data-ttu-id="90831-109">BOOL do VT \_</span><span class="sxs-lookup"><span data-stu-id="90831-109">VT\_BOOL</span></span>

<span data-ttu-id="90831-110">**boolVal**</span><span class="sxs-lookup"><span data-stu-id="90831-110">**boolVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="90831-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="90831-111">Remarks</span></span>

<span data-ttu-id="90831-112">Se o valor dessa propriedade for VARIANT \_ true, o coletor de mídia ASF ajustará automaticamente a taxa de bits do conteúdo ASF em resposta às características dos fluxos que estão sendo multiplexados.</span><span class="sxs-lookup"><span data-stu-id="90831-112">If the value of this property is VARIANT\_TRUE, the ASF media sink automatically adjusts the bit rate of the ASF content in response to the characteristics of the streams being multiplexed.</span></span>

<span data-ttu-id="90831-113">Essa propriedade afeta a forma como o coletor de mídia ASF se comporta quando um fluxo estoura os parâmetros de "Bucket de vazamentos" do coletor:</span><span class="sxs-lookup"><span data-stu-id="90831-113">This property affects how the ASF media sink behaves when a stream overflows the sink's "leaky bucket" parameters:</span></span>



| <span data-ttu-id="90831-114">Valor</span><span class="sxs-lookup"><span data-stu-id="90831-114">Value</span></span>              | <span data-ttu-id="90831-115">Comportamento</span><span class="sxs-lookup"><span data-stu-id="90831-115">Behavior</span></span>                                                                                                                                      |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90831-116">**VARIANTE \_ true**</span><span class="sxs-lookup"><span data-stu-id="90831-116">**VARIANT\_TRUE**</span></span>  | <span data-ttu-id="90831-117">O coletor de mídia ASF ajusta automaticamente a taxa de bits do conteúdo ASF em resposta às características dos fluxos que estão sendo multiplexados.</span><span class="sxs-lookup"><span data-stu-id="90831-117">The ASF media sink automatically adjusts the bit rate of the ASF content in response to the characteristics of the streams being multiplexed.</span></span> |
| <span data-ttu-id="90831-118">**VARIANTE \_ falso**</span><span class="sxs-lookup"><span data-stu-id="90831-118">**VARIANT\_FALSE**</span></span> | <span data-ttu-id="90831-119">O coletor de mídia ASF usa o valor de taxa de bits de fluxo fornecido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="90831-119">The ASF media sink uses the stream bit rate value provided by the application.</span></span>                                                                |



 

<span data-ttu-id="90831-120">O valor padrão é **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="90831-120">The default value is **VARIANT\_FALSE**.</span></span>

<span data-ttu-id="90831-121">Defina essa propriedade ao configurar o coletor de mídia ASF.</span><span class="sxs-lookup"><span data-stu-id="90831-121">Set this property when you configure the ASF media sink.</span></span> <span data-ttu-id="90831-122">O uso depende de qual função você chama para criar o coletor de mídia ASF:</span><span class="sxs-lookup"><span data-stu-id="90831-122">The usage depends on which function you call to create the ASF media sink:</span></span>

-   <span data-ttu-id="90831-123">[**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): consulta o ponteiro [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) recuperado para a interface **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="90831-123">[**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): Query the retrieved [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) pointer for the **IPropertyStore** interface.</span></span>

-   <span data-ttu-id="90831-124">[**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): chame [**IMFASFContentInfo:: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) no ponteiro [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) especificado no parâmetro *pContentInfo* .</span><span class="sxs-lookup"><span data-stu-id="90831-124">[**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): Call [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) on the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) pointer specified in the *pContentInfo* parameter.</span></span>

<span data-ttu-id="90831-125">Definir essa propriedade como VARIANT \_ true faz com que o coletor de mídia ASF defina o sinalizador de **taxa de bits do MFASF \_ multiplexador \_ \_ AutoAjuste** no Multiplexador de ASF.</span><span class="sxs-lookup"><span data-stu-id="90831-125">Setting this property to VARIANT\_TRUE causes the ASF media sink to set the **MFASF\_MULTIPLEXER\_AUTOADJUST\_BITRATE** flag on the ASF multiplexer.</span></span> <span data-ttu-id="90831-126">Consulte [**IMFASFMultiplexer:: SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags).</span><span class="sxs-lookup"><span data-stu-id="90831-126">See [**IMFASFMultiplexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags).</span></span>

<span data-ttu-id="90831-127">Para obter mais informações sobre o conceito de Bucket de vazamento, consulte o tópico "o modelo de buffer de buckets de vazamentos" na documentação do Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="90831-127">For more information about the leaky bucket concept, see the topic "The Leaky Bucket Buffer Model" in the Windows Media Format SDK documentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="90831-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90831-128">Requirements</span></span>



| <span data-ttu-id="90831-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="90831-129">Requirement</span></span> | <span data-ttu-id="90831-130">Valor</span><span class="sxs-lookup"><span data-stu-id="90831-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="90831-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90831-131">Minimum supported client</span></span><br/> | <span data-ttu-id="90831-132">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="90831-132">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="90831-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90831-133">Minimum supported server</span></span><br/> | <span data-ttu-id="90831-134">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="90831-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="90831-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="90831-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="90831-136"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="90831-136"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90831-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="90831-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90831-138">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="90831-138">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="90831-139">**\_ASFSTREAMCONFIG MF \_ LEAKYBUCKET1**</span><span class="sxs-lookup"><span data-stu-id="90831-139">**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**</span></span>](mf-asfstreamconfig-leakybucket1-attribute.md)
</dt> <dt>

[<span data-ttu-id="90831-140">**\_ASFSTREAMCONFIG MF \_ LEAKYBUCKET2**</span><span class="sxs-lookup"><span data-stu-id="90831-140">**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET2**</span></span>](mf-asfstreamconfig-leakybucket2-attribute.md)
</dt> </dl>

 

 




