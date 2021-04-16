---
description: Especifica o tempo, em unidades de 100 a nanossegundos, necessário para enviar um arquivo ASF (Advanced Systems Format). Uma hora de envio dos pacotes é a hora em que o pacote deve ser entregue pela rede. Não é a hora da apresentação do pacote.
ms.assetid: 2bd427e2-106d-4997-86aa-fae221e429eb
title: Atributo MF_PD_ASF_FILEPROPERTIES_SEND_DURATION (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: deed3f78208a0f0c7e555e8113f05ac0800cdb97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765361"
---
# <a name="mf_pd_asf_fileproperties_send_duration-attribute"></a><span data-ttu-id="c58d2-105">\_Atributo de \_ \_ duração de envio de FileProperties do MF PD ASF \_ \_</span><span class="sxs-lookup"><span data-stu-id="c58d2-105">MF\_PD\_ASF\_FILEPROPERTIES\_SEND\_DURATION attribute</span></span>

<span data-ttu-id="c58d2-106">Especifica o tempo, em unidades de 100 a nanossegundos, necessário para enviar um arquivo ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="c58d2-106">Specifies the time, in 100-nanosecond units, needed to send an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="c58d2-107">A hora de *envio* de um pacote é a hora em que o pacote deve ser entregue pela rede.</span><span class="sxs-lookup"><span data-stu-id="c58d2-107">A packet's *send time* is the time when the packet should be delivered over the network.</span></span> <span data-ttu-id="c58d2-108">Não é a hora da apresentação do pacote.</span><span class="sxs-lookup"><span data-stu-id="c58d2-108">It is not the presentation time of the packet.</span></span>

## <a name="data-type"></a><span data-ttu-id="c58d2-109">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="c58d2-109">Data type</span></span>

<span data-ttu-id="c58d2-110">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="c58d2-110">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="c58d2-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="c58d2-111">Remarks</span></span>

<span data-ttu-id="c58d2-112">Esse atributo se aplica a descritores de apresentação para conteúdo ASF.</span><span class="sxs-lookup"><span data-stu-id="c58d2-112">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="c58d2-113">O método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) gera esse atributo dos metadados do ASF.</span><span class="sxs-lookup"><span data-stu-id="c58d2-113">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="c58d2-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c58d2-114">Requirements</span></span>



| <span data-ttu-id="c58d2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c58d2-115">Requirement</span></span> | <span data-ttu-id="c58d2-116">Valor</span><span class="sxs-lookup"><span data-stu-id="c58d2-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c58d2-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c58d2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c58d2-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c58d2-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c58d2-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c58d2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c58d2-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c58d2-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c58d2-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c58d2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c58d2-122"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="c58d2-122"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c58d2-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="c58d2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c58d2-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c58d2-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c58d2-125">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="c58d2-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="c58d2-126">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="c58d2-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="c58d2-127">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="c58d2-127">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="c58d2-128">Atributos do descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="c58d2-128">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="c58d2-129">Objeto de cabeçalho ASF</span><span class="sxs-lookup"><span data-stu-id="c58d2-129">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="c58d2-130">Descritores de apresentação</span><span class="sxs-lookup"><span data-stu-id="c58d2-130">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




