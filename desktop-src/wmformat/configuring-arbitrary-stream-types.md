---
title: Configurando tipos de fluxo arbitrários
description: Configurando tipos de fluxo arbitrários
ms.assetid: d745ec4b-9ce5-4288-bc24-0c1220c4d510
keywords:
- fluxos, configurando tipos de fluxo arbitrários
- codecs, configurando tipos de fluxo arbitrários
- fluxos, GenProfile
- codecs, GenProfile
- GenProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59e04751bd33da6599fd7ff3766c4dc8350889c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105780363"
---
# <a name="configuring-arbitrary-stream-types"></a><span data-ttu-id="c476e-108">Configurando tipos de fluxo arbitrários</span><span class="sxs-lookup"><span data-stu-id="c476e-108">Configuring Arbitrary Stream Types</span></span>

<span data-ttu-id="c476e-109">A maioria dos tipos de fluxo arbitrários precisa apenas de uma taxa de bits, uma janela de buffer e um tipo de mídia principal adequado na estrutura do [**\_ \_ tipo de mídia do WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) .</span><span class="sxs-lookup"><span data-stu-id="c476e-109">Most arbitrary stream types just need a bit rate, a buffer window, and a proper major media type in the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure.</span></span> <span data-ttu-id="c476e-110">No entanto, alguns tipos arbitrários exigem configuração adicional.</span><span class="sxs-lookup"><span data-stu-id="c476e-110">However, some arbitrary types require additional configuration.</span></span>

<span data-ttu-id="c476e-111">Se você tiver problemas para configurar um fluxo, consulte o aplicativo de exemplo chamado GenProfile, que está incluído neste SDK.</span><span class="sxs-lookup"><span data-stu-id="c476e-111">If you have trouble configuring a stream, refer to the sample application called GenProfile, which is included with this SDK.</span></span> <span data-ttu-id="c476e-112">A biblioteca definida em GenProfile contém código para incluir todos os tipos de fluxos.</span><span class="sxs-lookup"><span data-stu-id="c476e-112">The library defined in GenProfile contains code for including all types of streams.</span></span> <span data-ttu-id="c476e-113">Para obter mais informações sobre GenProfile e outros exemplos, consulte [aplicativos de exemplo](sample-applications.md).</span><span class="sxs-lookup"><span data-stu-id="c476e-113">For more information about GenProfile and the other samples, see [Sample Applications](sample-applications.md).</span></span>

<span data-ttu-id="c476e-114">As seções a seguir descrevem como configurar tipos de fluxo arbitrários.</span><span class="sxs-lookup"><span data-stu-id="c476e-114">The following sections describe how to configure arbitrary stream types.</span></span>



| <span data-ttu-id="c476e-115">Seção</span><span class="sxs-lookup"><span data-stu-id="c476e-115">Section</span></span>                                                                                                                                        | <span data-ttu-id="c476e-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="c476e-116">Description</span></span>                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c476e-117">Configurando fluxos de script</span><span class="sxs-lookup"><span data-stu-id="c476e-117">Configuring Script Streams</span></span>](configuring-script-streams.md)                                                                                   | <span data-ttu-id="c476e-118">Descreve como configurar fluxos de script.</span><span class="sxs-lookup"><span data-stu-id="c476e-118">Describes how to configure script streams.</span></span>                                                  |
| [<span data-ttu-id="c476e-119">Configurando fluxos de transferência de arquivo</span><span class="sxs-lookup"><span data-stu-id="c476e-119">Configuring File Transfer Streams</span></span>](configuring-file-transfer-streams.md)                                                                     | <span data-ttu-id="c476e-120">Descreve como configurar fluxos de transferência de arquivo.</span><span class="sxs-lookup"><span data-stu-id="c476e-120">Describes how to configure file transfer streams.</span></span>                                           |
| [<span data-ttu-id="c476e-121">Configurando fluxos da Web</span><span class="sxs-lookup"><span data-stu-id="c476e-121">Configuring Web Streams</span></span>](configuring-web-streams.md)                                                                                         | <span data-ttu-id="c476e-122">Descreve como configurar fluxos da Web.</span><span class="sxs-lookup"><span data-stu-id="c476e-122">Describes how to configure Web streams.</span></span>                                                     |
| [<span data-ttu-id="c476e-123">Configurando fluxos de texto</span><span class="sxs-lookup"><span data-stu-id="c476e-123">Configuring Text Streams</span></span>](configuring-text-streams.md)                                                                                       | <span data-ttu-id="c476e-124">Descreve como configurar fluxos de texto.</span><span class="sxs-lookup"><span data-stu-id="c476e-124">Describes how to configure text streams.</span></span>                                                    |
| [<span data-ttu-id="c476e-125">Configurando fluxos arbitrários personalizados</span><span class="sxs-lookup"><span data-stu-id="c476e-125">Configuring Custom Arbitrary Streams</span></span>](configuring-custom-arbitrary-streams.md)                                                               | <span data-ttu-id="c476e-126">Descreve como configurar fluxos para tipos de fluxos arbitrários personalizados.</span><span class="sxs-lookup"><span data-stu-id="c476e-126">Describes how to configure streams for custom arbitrary stream types.</span></span>                       |
| [<span data-ttu-id="c476e-127">Calculando valores de taxa de bits e de janela de buffer para fluxos arbitrários</span><span class="sxs-lookup"><span data-stu-id="c476e-127">Calculating Bit Rate and Buffer Window Values for Arbitrary Streams</span></span>](calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams.md) | <span data-ttu-id="c476e-128">Descreve como calcular a taxa de bits e as configurações de janela de buffer para um fluxo arbitrário.</span><span class="sxs-lookup"><span data-stu-id="c476e-128">Describes how to calculate the bit rate and buffer window settings for an arbitrary stream.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="c476e-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c476e-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c476e-130">**Fluxos arbitrários**</span><span class="sxs-lookup"><span data-stu-id="c476e-130">**Arbitrary Streams**</span></span>](arbitrary-streams.md)
</dt> <dt>

[<span data-ttu-id="c476e-131">**Configurando fluxos**</span><span class="sxs-lookup"><span data-stu-id="c476e-131">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> </dl>

 

 




