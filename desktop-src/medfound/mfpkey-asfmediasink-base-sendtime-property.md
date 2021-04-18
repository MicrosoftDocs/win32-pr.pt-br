---
description: Tempo de envio base para o coletor de mídia ASF, em milissegundos.
ms.assetid: 1b99845e-751a-4ec6-bd2d-e4644cd6863e
title: Propriedade MFPKEY_ASFMEDIASINK_BASE_SENDTIME (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3f9bc7f9d92a598a723e3eeee733f63b59d27d2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105813561"
---
# <a name="mfpkey_asfmediasink_base_sendtime-property"></a><span data-ttu-id="34853-103">\_ \_ \_ Propriedade sendtime base MFPKEY ASFMEDIASINK</span><span class="sxs-lookup"><span data-stu-id="34853-103">MFPKEY\_ASFMEDIASINK\_BASE\_SENDTIME property</span></span>

<span data-ttu-id="34853-104">Tempo de envio base para o coletor de mídia ASF, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="34853-104">Base send time for the ASF media sink, in milliseconds.</span></span>



<span data-ttu-id="34853-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="34853-105">Data type</span></span>

<span data-ttu-id="34853-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="34853-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="34853-107">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="34853-107">PROPVARIANT member</span></span>

<span data-ttu-id="34853-108">**ULONG**</span><span class="sxs-lookup"><span data-stu-id="34853-108">**ULONG**</span></span>

<span data-ttu-id="34853-109">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="34853-109">VT\_UI4</span></span>

<span data-ttu-id="34853-110">**ulVal**</span><span class="sxs-lookup"><span data-stu-id="34853-110">**ulVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="34853-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="34853-111">Remarks</span></span>

<span data-ttu-id="34853-112">A hora de envio é a hora em que um pacote ASF é enviado pela rede.</span><span class="sxs-lookup"><span data-stu-id="34853-112">The send time is the time at which an ASF packet is sent across the network.</span></span> <span data-ttu-id="34853-113">Ele não corresponde diretamente à hora da apresentação dos dados no pacote.</span><span class="sxs-lookup"><span data-stu-id="34853-113">It does not correspond directly to the presentation time of the data in the packet.</span></span>

<span data-ttu-id="34853-114">Você pode usar essa propriedade para configurar o coletor de mídia ASF.</span><span class="sxs-lookup"><span data-stu-id="34853-114">You can use this property to configure the ASF media sink.</span></span> <span data-ttu-id="34853-115">O uso depende de qual função você chama para criar o coletor de mídia ASF:</span><span class="sxs-lookup"><span data-stu-id="34853-115">The usage depends on which function you call to create the ASF media sink:</span></span>

-   <span data-ttu-id="34853-116">[**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): consulta o ponteiro [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) recuperado para a interface **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="34853-116">[**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): Query the retrieved [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) pointer for the **IPropertyStore** interface.</span></span>

-   <span data-ttu-id="34853-117">[**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): chame [**IMFASFContentInfo:: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) no ponteiro [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) especificado no parâmetro *pContentInfo* .</span><span class="sxs-lookup"><span data-stu-id="34853-117">[**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): Call [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) on the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) pointer specified in the *pContentInfo* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="34853-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34853-118">Requirements</span></span>



| <span data-ttu-id="34853-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="34853-119">Requirement</span></span> | <span data-ttu-id="34853-120">Valor</span><span class="sxs-lookup"><span data-stu-id="34853-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="34853-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="34853-121">Minimum supported client</span></span><br/> | <span data-ttu-id="34853-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="34853-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="34853-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="34853-123">Minimum supported server</span></span><br/> | <span data-ttu-id="34853-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="34853-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="34853-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="34853-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="34853-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="34853-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34853-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="34853-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34853-128">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="34853-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




