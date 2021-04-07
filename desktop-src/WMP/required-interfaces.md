---
title: Interfaces necessárias (SDK do Windows Media Player)
description: Interfaces necessárias
ms.assetid: 202d5769-edff-46df-bc05-bbb630a8f3f4
keywords:
- Plug-ins do Windows Media Player, interfaces
- plug-ins, interfaces
- plug-ins de processamento de sinal digital, interfaces
- Plug-ins do DSP, interfaces
- interfaces, plug-ins do DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e9c6923af513f2d241955b508f0872f85a4b020
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103824116"
---
# <a name="required-interfaces-windows-media-player-sdk"></a><span data-ttu-id="05f0b-108">Interfaces necessárias (SDK do Windows Media Player)</span><span class="sxs-lookup"><span data-stu-id="05f0b-108">Required Interfaces (Windows Media Player SDK)</span></span>

<span data-ttu-id="05f0b-109">O Windows Media Player renderiza áudio e vídeo usando um dos pipelines a seguir.</span><span class="sxs-lookup"><span data-stu-id="05f0b-109">Windows Media Player renders audio and video by using one of the following pipelines.</span></span>

-   <span data-ttu-id="05f0b-110">DirectShow</span><span class="sxs-lookup"><span data-stu-id="05f0b-110">DirectShow</span></span>
-   <span data-ttu-id="05f0b-111">Media Foundation</span><span class="sxs-lookup"><span data-stu-id="05f0b-111">Media Foundation</span></span>

<span data-ttu-id="05f0b-112">No Microsoft Windows XP e versões anteriores, o Player usa o DirectShow.</span><span class="sxs-lookup"><span data-stu-id="05f0b-112">In Microsoft Windows XP and earlier, the Player uses DirectShow.</span></span> <span data-ttu-id="05f0b-113">No Windows Vista, às vezes o Player usa o DirectShow e, às vezes, usa Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="05f0b-113">In Windows Vista, the Player sometimes uses DirectShow and sometimes uses Media Foundation.</span></span>

<span data-ttu-id="05f0b-114">Um plug-in do DSP implementa algumas ou todas as seguintes interfaces:</span><span class="sxs-lookup"><span data-stu-id="05f0b-114">A DSP plug-in implements some or all of the following interfaces:</span></span>

-   <span data-ttu-id="05f0b-115">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="05f0b-115">**IMediaObject**</span></span>
-   <span data-ttu-id="05f0b-116">**IWMPPluginEnable**</span><span class="sxs-lookup"><span data-stu-id="05f0b-116">**IWMPPluginEnable**</span></span>
-   <span data-ttu-id="05f0b-117">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="05f0b-117">**IMFTransform**</span></span>
-   <span data-ttu-id="05f0b-118">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="05f0b-118">**IMFGetService**</span></span>
-   <span data-ttu-id="05f0b-119">**ISpecifyPropertyPages**</span><span class="sxs-lookup"><span data-stu-id="05f0b-119">**ISpecifyPropertyPages**</span></span>

<span data-ttu-id="05f0b-120">Um plug-in que implementa **IMediaObject** e **IWMPPluginEnable** pode ser executado no pipeline do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="05f0b-120">A plug-in that implements **IMediaObject** and **IWMPPluginEnable** can run in the DirectShow pipeline.</span></span> <span data-ttu-id="05f0b-121">Ele também pode ser executado no pipeline de Media Foundation dentro de um wrapper fornecido pelo Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="05f0b-121">It can also run in the Media Foundation Pipeline inside a wrapper provided by Media Foundation.</span></span> <span data-ttu-id="05f0b-122">Um plug-in desse tipo é chamado de Microsoft DirectX Media Object (DMO).</span><span class="sxs-lookup"><span data-stu-id="05f0b-122">A plug-in of this type is called a Microsoft DirectX Media Object (DMO).</span></span> <span data-ttu-id="05f0b-123">É comum considerar um DMO como sendo análogo a um objeto de filtro no DirectShow.</span><span class="sxs-lookup"><span data-stu-id="05f0b-123">It is common to think of a DMO as being analogous to a filter object in DirectShow.</span></span> <span data-ttu-id="05f0b-124">A documentação do DMO está na seção do DirectShow do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="05f0b-124">The DMO documentation is in the DirectShow section of the Windows SDK.</span></span>

<span data-ttu-id="05f0b-125">Um plug-in que implementa **IMFTransform** e **IMFGetService** pode ser executado nativamente (nenhum wrapper é necessário) no pipeline de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="05f0b-125">A plug-in that implements **IMFTransform** and **IMFGetService** can run natively (no wrapper required) in the Media Foundation pipeline.</span></span> <span data-ttu-id="05f0b-126">Um plug-in desse tipo é chamado de Media Foundation transformação (MFT).</span><span class="sxs-lookup"><span data-stu-id="05f0b-126">A plug-in of this type is called a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="05f0b-127">A documentação do MFT está na seção Media Foundation do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="05f0b-127">The MFT documentation is in the Media Foundation section of the Windows SDK.</span></span>

<span data-ttu-id="05f0b-128">Um plug-in que implementa **IMediaObject**, **IWMPPluginEnable**, **IMFTransform** e **IMFGetService** pode ser executado no pipeline do DirectShow e também pode ser executado nativamente no pipeline de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="05f0b-128">A plug-in that implements **IMediaObject**, **IWMPPluginEnable**, **IMFTransform**, and **IMFGetService** can run in the DirectShow pipeline and can also run natively in the Media Foundation pipeline.</span></span> <span data-ttu-id="05f0b-129">Esse tipo de plug-in, chamado de plug-in de *DSP de modo duplo*, pode desempenhar a função de um DMO ou MFT.</span><span class="sxs-lookup"><span data-stu-id="05f0b-129">This type of plug-in, which is called a *dual-mode DSP plug-in*, can play the role of a DMO or an MFT.</span></span>

<span data-ttu-id="05f0b-130">Quando o Windows Media Player usa um plug-in de DSP de modo duplo no pipeline de Media Foundation, ele primeiro consulta a interface **IMFTransform** .</span><span class="sxs-lookup"><span data-stu-id="05f0b-130">When Windows Media Player uses a dual-mode DSP plug-in in the Media Foundation pipeline, it first queries for the **IMFTransform** interface.</span></span> <span data-ttu-id="05f0b-131">Se essa consulta falhar, o Windows Media Player consultará a interface **IMediaObject** .</span><span class="sxs-lookup"><span data-stu-id="05f0b-131">If that query fails, Windows Media Player queries for the **IMediaObject** interface.</span></span> <span data-ttu-id="05f0b-132">Se a consulta **IMediaObject** for bem-sucedida, o plug-in será encapsulado e adicionado ao pipeline de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="05f0b-132">If the **IMediaObject** query is successful, the plug-in is wrapped and added to the Media Foundation pipeline.</span></span>

<span data-ttu-id="05f0b-133">Independentemente do pipeline, qualquer plug-in de DSP que permita ao usuário definir propriedades deve implementar **ISpecifyPropertyPages**.</span><span class="sxs-lookup"><span data-stu-id="05f0b-133">Regardless of the pipeline, any DSP plug-in that allows the user to set properties must implement **ISpecifyPropertyPages**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="05f0b-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="05f0b-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05f0b-135">**Visão geral do desenvolvedor de plug-in do DSP**</span><span class="sxs-lookup"><span data-stu-id="05f0b-135">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> <dt>

[<span data-ttu-id="05f0b-136">**Interfaces de plug-in do DSP**</span><span class="sxs-lookup"><span data-stu-id="05f0b-136">**DSP Plug-in Interfaces**</span></span>](dsp-plug-in-interfaces.md)
</dt> <dt>

[<span data-ttu-id="05f0b-137">**Empacotamento de plug-in do DSP**</span><span class="sxs-lookup"><span data-stu-id="05f0b-137">**DSP Plug-in Packaging**</span></span>](dsp-plug-in-packaging.md)
</dt> </dl>

 

 




