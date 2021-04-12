---
title: Configurando fluxos da Web
description: Configurando fluxos da Web
ms.assetid: 1eeb6243-5095-4dba-994c-2083beda7b78
keywords:
- fluxos, configurando fluxos da Web
- codecs, configurando fluxos da Web
- Fluxos da Web, configurando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27c91c36788b858b2378ebf46b553f076c5ec490
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292675"
---
# <a name="configuring-web-streams"></a><span data-ttu-id="f9643-106">Configurando fluxos da Web</span><span class="sxs-lookup"><span data-stu-id="f9643-106">Configuring Web Streams</span></span>

<span data-ttu-id="f9643-107">Os fluxos da Web são um tipo especializado de fluxo de transferência de arquivos usado para entregar os arquivos associados a um site em um único fluxo.</span><span class="sxs-lookup"><span data-stu-id="f9643-107">Web streams are a specialized type of file transfer stream used to deliver the files associated with a Web site in a single stream.</span></span> <span data-ttu-id="f9643-108">A configuração de fluxo da Web está resumida na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f9643-108">Web stream configuration is summarized in the following table.</span></span>



| <span data-ttu-id="f9643-109">Configuração</span><span class="sxs-lookup"><span data-stu-id="f9643-109">Setting</span></span>                                            | <span data-ttu-id="f9643-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="f9643-110">Description</span></span>                                                                       |
|----------------------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f9643-111">**Tipo de mídia do WM \_ \_ . majortype**</span><span class="sxs-lookup"><span data-stu-id="f9643-111">**WM\_MEDIA\_TYPE.majortype**</span></span>                      | <span data-ttu-id="f9643-112">Defina como WMMEDIATYPE \_ FileTransfer.</span><span class="sxs-lookup"><span data-stu-id="f9643-112">Set to WMMEDIATYPE\_FileTransfer.</span></span>                                                 |
| <span data-ttu-id="f9643-113">**Tipo de mídia do WM \_ \_ . subtipo**</span><span class="sxs-lookup"><span data-stu-id="f9643-113">**WM\_MEDIA\_TYPE.subtype**</span></span>                        | <span data-ttu-id="f9643-114">Defina como \_ webstream do WMMEDIASUBTYPE.</span><span class="sxs-lookup"><span data-stu-id="f9643-114">Set to WMMEDIASUBTYPE\_WebStream.</span></span>                                                 |
| <span data-ttu-id="f9643-115">**Tipo de mídia do WM \_ \_ . bFixedSizeSamples**</span><span class="sxs-lookup"><span data-stu-id="f9643-115">**WM\_MEDIA\_TYPE.bFixedSizeSamples**</span></span>              | <span data-ttu-id="f9643-116">Defina como false.</span><span class="sxs-lookup"><span data-stu-id="f9643-116">Set to False.</span></span>                                                                     |
| <span data-ttu-id="f9643-117">**Tipo de mídia do WM \_ \_ . bTemporalCompression**</span><span class="sxs-lookup"><span data-stu-id="f9643-117">**WM\_MEDIA\_TYPE.bTemporalCompression**</span></span>           | <span data-ttu-id="f9643-118">Defina como True.</span><span class="sxs-lookup"><span data-stu-id="f9643-118">Set to True.</span></span>                                                                      |
| <span data-ttu-id="f9643-119">**Tipo de mídia do WM \_ \_ . lSampleSize**</span><span class="sxs-lookup"><span data-stu-id="f9643-119">**WM\_MEDIA\_TYPE.lSampleSize**</span></span>                    | <span data-ttu-id="f9643-120">Defina como 0.</span><span class="sxs-lookup"><span data-stu-id="f9643-120">Set to 0.</span></span>                                                                         |
| <span data-ttu-id="f9643-121">**Tipo de mídia do WM \_ \_ . FormatType**</span><span class="sxs-lookup"><span data-stu-id="f9643-121">**WM\_MEDIA\_TYPE.formattype**</span></span>                     | <span data-ttu-id="f9643-122">Defina como \_ webstream do WMFORMAT.</span><span class="sxs-lookup"><span data-stu-id="f9643-122">Set to WMFORMAT\_WebStream.</span></span>                                                       |
| <span data-ttu-id="f9643-123">**Tipo de mídia do WM \_ \_ . punk**</span><span class="sxs-lookup"><span data-stu-id="f9643-123">**WM\_MEDIA\_TYPE.pUnk**</span></span>                           | <span data-ttu-id="f9643-124">Defina como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="f9643-124">Set to **NULL**.</span></span>                                                                  |
| <span data-ttu-id="f9643-125">**Tipo de mídia do WM \_ \_ . cbFormat**</span><span class="sxs-lookup"><span data-stu-id="f9643-125">**WM\_MEDIA\_TYPE.cbFormat**</span></span>                       | <span data-ttu-id="f9643-126">Defina como `sizeof(WMT_WEBSTREAM_FORMAT)`.</span><span class="sxs-lookup"><span data-stu-id="f9643-126">Set to `sizeof(WMT_WEBSTREAM_FORMAT)`.</span></span>                                            |
| <span data-ttu-id="f9643-127">**Tipo de mídia do WM \_ \_ . pbFormat**</span><span class="sxs-lookup"><span data-stu-id="f9643-127">**WM\_MEDIA\_TYPE.pbFormat**</span></span>                       | <span data-ttu-id="f9643-128">Defina como o endereço de uma estrutura de **\_ \_ formato de webstream do WMT** corretamente configurada.</span><span class="sxs-lookup"><span data-stu-id="f9643-128">Set to the address of a properly configured **WMT\_WEBSTREAM\_FORMAT** structure.</span></span> |
| <span data-ttu-id="f9643-129">**\_Formato WEBstream do WMT \_ . cbSampleHeaderFixedData**</span><span class="sxs-lookup"><span data-stu-id="f9643-129">**WMT\_WEBSTREAM\_FORMAT.cbSampleHeaderFixedData**</span></span> | <span data-ttu-id="f9643-130">Defina como `sizeof(WMT_WEBSTREAM_SAMPLE_HEADER)`.</span><span class="sxs-lookup"><span data-stu-id="f9643-130">Set to `sizeof(WMT_WEBSTREAM_SAMPLE_HEADER)`.</span></span>                                     |
| <span data-ttu-id="f9643-131">**\_Formato WEBstream do WMT \_ . wVersion**</span><span class="sxs-lookup"><span data-stu-id="f9643-131">**WMT\_WEBSTREAM\_FORMAT.wVersion**</span></span>                | <span data-ttu-id="f9643-132">defina como 1.</span><span class="sxs-lookup"><span data-stu-id="f9643-132">Set to 1.</span></span>                                                                         |
| <span data-ttu-id="f9643-133">**\_Formato WEBstream do WMT \_ . wReserved**</span><span class="sxs-lookup"><span data-stu-id="f9643-133">**WMT\_WEBSTREAM\_FORMAT.wreserved**</span></span>               | <span data-ttu-id="f9643-134">Defina como 0.</span><span class="sxs-lookup"><span data-stu-id="f9643-134">Set to 0.</span></span>                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="f9643-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f9643-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9643-136">**Configuração comum a todos os fluxos**</span><span class="sxs-lookup"><span data-stu-id="f9643-136">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="f9643-137">**Configurando tipos de fluxo arbitrários**</span><span class="sxs-lookup"><span data-stu-id="f9643-137">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> <dt>

[<span data-ttu-id="f9643-138">**Fluxos da Web**</span><span class="sxs-lookup"><span data-stu-id="f9643-138">**Web Streams**</span></span>](web-streams.md)
</dt> </dl>

 

 




