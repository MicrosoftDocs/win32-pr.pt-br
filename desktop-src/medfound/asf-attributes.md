---
description: Atributos ASF
ms.assetid: c1570669-6e9c-4614-af4d-2a148f12e36f
title: Atributos ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ccf09542c8b96cc262cbe029111d3cb74e5b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763220"
---
# <a name="asf-attributes"></a><span data-ttu-id="8d906-103">Atributos ASF</span><span class="sxs-lookup"><span data-stu-id="8d906-103">ASF Attributes</span></span>

### <a name="profile-attributes"></a><span data-ttu-id="8d906-104">Atributos de perfil</span><span class="sxs-lookup"><span data-stu-id="8d906-104">Profile Attributes</span></span>

<span data-ttu-id="8d906-105">Os atributos a seguir se aplicam a perfis ASF.</span><span class="sxs-lookup"><span data-stu-id="8d906-105">The following attributes apply to ASF profiles.</span></span>



| <span data-ttu-id="8d906-106">Atributo</span><span class="sxs-lookup"><span data-stu-id="8d906-106">Attribute</span></span>                                                                      | <span data-ttu-id="8d906-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="8d906-107">Description</span></span>                                                  |
|--------------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="8d906-108">**\_ASFPROFILE MF \_ MAXPACKETSIZE**</span><span class="sxs-lookup"><span data-stu-id="8d906-108">**MF\_ASFPROFILE\_MAXPACKETSIZE**</span></span>](mf-asfprofile-maxpacketsize-attribute.md) | <span data-ttu-id="8d906-109">Especifica o tamanho máximo do pacote para um arquivo ASF, em bytes.</span><span class="sxs-lookup"><span data-stu-id="8d906-109">Specifies the maximum packet size for an ASF file, in bytes.</span></span> |
| [<span data-ttu-id="8d906-110">**\_ASFPROFILE MF \_ MINPACKETSIZE**</span><span class="sxs-lookup"><span data-stu-id="8d906-110">**MF\_ASFPROFILE\_MINPACKETSIZE**</span></span>](mf-asfprofile-minpacketsize-attribute.md) | <span data-ttu-id="8d906-111">Especifica o tamanho mínimo do pacote para um arquivo ASF, em bytes.</span><span class="sxs-lookup"><span data-stu-id="8d906-111">Specifies the minimum packet size for an ASF file, in bytes.</span></span> |



 

### <a name="stream-configuration-attributes"></a><span data-ttu-id="8d906-112">Atributos de configuração de fluxo</span><span class="sxs-lookup"><span data-stu-id="8d906-112">Stream Configuration Attributes</span></span>

<span data-ttu-id="8d906-113">Os atributos a seguir se aplicam ao objeto de configuração de fluxo ASF.</span><span class="sxs-lookup"><span data-stu-id="8d906-113">The following attributes apply to the ASF stream configuration object.</span></span>



| <span data-ttu-id="8d906-114">Atributo</span><span class="sxs-lookup"><span data-stu-id="8d906-114">Attribute</span></span>                                                                              | <span data-ttu-id="8d906-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="8d906-115">Description</span></span>                                                                   |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="8d906-116">**\_ASFSTREAMCONFIG MF \_ LEAKYBUCKET1**</span><span class="sxs-lookup"><span data-stu-id="8d906-116">**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**</span></span>](mf-asfstreamconfig-leakybucket1-attribute.md) | <span data-ttu-id="8d906-117">Define os parâmetros médios de "Bucket de vazamentos" para codificar um arquivo de mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="8d906-117">Sets the average "leaky bucket" parameters for encoding a Windows Media file.</span></span> |
| [<span data-ttu-id="8d906-118">**\_ASFSTREAMCONFIG MF \_ LEAKYBUCKET2**</span><span class="sxs-lookup"><span data-stu-id="8d906-118">**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET2**</span></span>](mf-asfstreamconfig-leakybucket2-attribute.md) | <span data-ttu-id="8d906-119">Define o pico dos parâmetros de "Bucket de vazamentos" para codificar um arquivo de mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="8d906-119">Sets the peak "leaky bucket" parameters for encoding a Windows Media file.</span></span>    |



 

### <a name="media-buffer-attributes"></a><span data-ttu-id="8d906-120">Atributos de buffer de mídia</span><span class="sxs-lookup"><span data-stu-id="8d906-120">Media Buffer Attributes</span></span>

<span data-ttu-id="8d906-121">Os atributos a seguir se aplicam a buffers de mídia para pacotes ASF.</span><span class="sxs-lookup"><span data-stu-id="8d906-121">The following attributes apply to media buffers for ASF packets.</span></span>



| <span data-ttu-id="8d906-122">Atributo</span><span class="sxs-lookup"><span data-stu-id="8d906-122">Attribute</span></span>                                                                          | <span data-ttu-id="8d906-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="8d906-123">Description</span></span>                                                                               |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8d906-124">**\_limite de pacotes MFASFSPLITTER \_**</span><span class="sxs-lookup"><span data-stu-id="8d906-124">**MFASFSPLITTER\_PACKET\_BOUNDARY**</span></span>](mfasfsplitter-packet-boundary-attribute.md) | <span data-ttu-id="8d906-125">Especifica se um buffer contém o início de um pacote ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="8d906-125">Specifies whether a buffer contains the start of an Advanced Systems Format (ASF) packet.</span></span> |



 

### <a name="presentation-descriptor-attributes"></a><span data-ttu-id="8d906-126">Atributos do descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="8d906-126">Presentation Descriptor Attributes</span></span>

<span data-ttu-id="8d906-127">Para obter uma lista de atributos que se aplicam aos descritores de apresentação do ASF, consulte [atributos de descrição de apresentação](presentation-descriptor-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="8d906-127">For a list of attributes that apply to ASF presentation descriptors, see [Presentation Descriptor Attributes](presentation-descriptor-attributes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8d906-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8d906-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d906-129">**IMFASFProfile**</span><span class="sxs-lookup"><span data-stu-id="8d906-129">**IMFASFProfile**</span></span>](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile)
</dt> <dt>

[<span data-ttu-id="8d906-130">**IMFASFStreamConfig**</span><span class="sxs-lookup"><span data-stu-id="8d906-130">**IMFASFStreamConfig**</span></span>](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig)
</dt> <dt>

[<span data-ttu-id="8d906-131">Atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8d906-131">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 



