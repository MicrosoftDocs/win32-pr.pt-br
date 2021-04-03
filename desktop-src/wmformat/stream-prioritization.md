---
title: Priorização de fluxo
description: Priorização de fluxo
ms.assetid: 6b3e9b03-62ef-422b-97ab-197d1cd15beb
keywords:
- SDK do Windows Media Format, priorização de fluxo
- ASF (Advanced Systems Format), priorização de fluxo
- ASF (formato de sistemas avançados), priorização de fluxo
- SDK do Windows Media Format, ordem de prioridade para fluxos
- ASF (Advanced Systems Format), ordem de prioridade para fluxos
- ASF (formato de sistemas avançados), ordem de prioridade para fluxos
- fluxos, priorização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abe1628ef050d393cd2d98e73708d5a9ad6c3be4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007128"
---
# <a name="stream-prioritization"></a><span data-ttu-id="a5711-110">Priorização de fluxo</span><span class="sxs-lookup"><span data-stu-id="a5711-110">Stream Prioritization</span></span>

<span data-ttu-id="a5711-111">Ao criar um arquivo ASF, você pode especificar uma ordem de prioridade para seus fluxos de constituintes.</span><span class="sxs-lookup"><span data-stu-id="a5711-111">When you create an ASF file, you can specify a priority order for its constituent streams.</span></span> <span data-ttu-id="a5711-112">Se você transmitir um arquivo priorizado e a largura de banda disponível não for suficiente para fornecer todos os fluxos, o leitor removerá os fluxos na ordem de prioridade inversa.</span><span class="sxs-lookup"><span data-stu-id="a5711-112">If you stream a prioritized file and the available bandwidth is not enough to deliver all of the streams, the reader will drop streams in reverse priority order.</span></span> <span data-ttu-id="a5711-113">Dessa forma, você pode garantir que os fluxos mais importantes em seu arquivo não serão descartados devido a problemas de rede.</span><span class="sxs-lookup"><span data-stu-id="a5711-113">In this way you can guarantee that the most important streams in your file will not be dropped due to network difficulties.</span></span>

<span data-ttu-id="a5711-114">A priorização de fluxo é configurada com um objeto de priorização de fluxo e adicionada ao perfil.</span><span class="sxs-lookup"><span data-stu-id="a5711-114">Stream prioritization is configured with a stream prioritization object and added to the profile.</span></span> <span data-ttu-id="a5711-115">Um perfil pode conter apenas um objeto de priorização de fluxo.</span><span class="sxs-lookup"><span data-stu-id="a5711-115">A profile can contain only one stream prioritization object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5711-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a5711-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5711-117">**Recursos de arquivo ASF**</span><span class="sxs-lookup"><span data-stu-id="a5711-117">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="a5711-118">**IWMProfile3::CreateNewStreamPrioritization**</span><span class="sxs-lookup"><span data-stu-id="a5711-118">**IWMProfile3::CreateNewStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewstreamprioritization)
</dt> <dt>

[<span data-ttu-id="a5711-119">**IWMProfile3::GetStreamPrioritization**</span><span class="sxs-lookup"><span data-stu-id="a5711-119">**IWMProfile3::GetStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getstreamprioritization)
</dt> <dt>

[<span data-ttu-id="a5711-120">**IWMProfile3::RemoveStreamPrioritization**</span><span class="sxs-lookup"><span data-stu-id="a5711-120">**IWMProfile3::RemoveStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-removestreamprioritization)
</dt> <dt>

[<span data-ttu-id="a5711-121">**IWMProfile3::SetStreamPrioritization**</span><span class="sxs-lookup"><span data-stu-id="a5711-121">**IWMProfile3::SetStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-setstreamprioritization)
</dt> <dt>

[<span data-ttu-id="a5711-122">**Interface IWMStreamPrioritization**</span><span class="sxs-lookup"><span data-stu-id="a5711-122">**IWMStreamPrioritization Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamprioritization)
</dt> <dt>

[<span data-ttu-id="a5711-123">**Usando a priorização de fluxo**</span><span class="sxs-lookup"><span data-stu-id="a5711-123">**Using Stream Prioritization**</span></span>](using-stream-prioritization.md)
</dt> </dl>

 

 




