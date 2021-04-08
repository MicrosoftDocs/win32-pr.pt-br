---
description: Requisitos mínimos do DMO
ms.assetid: cd342f0f-a3dc-4623-a18f-c45071795ef4
title: Requisitos mínimos do DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1c26267f50619062fb8396f93b7578db4d3d8c4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103919976"
---
# <a name="dmo-minimum-requirements"></a><span data-ttu-id="bd517-103">Requisitos mínimos do DMO</span><span class="sxs-lookup"><span data-stu-id="bd517-103">DMO Minimum Requirements</span></span>

<span data-ttu-id="bd517-104">Cada DMO deve atender aos seguintes requisitos mínimos:</span><span class="sxs-lookup"><span data-stu-id="bd517-104">Every DMO should meet the following minimum requirements:</span></span>

-   <span data-ttu-id="bd517-105">Ele deve dar suporte à agregação.</span><span class="sxs-lookup"><span data-stu-id="bd517-105">It must support aggregation.</span></span>
-   <span data-ttu-id="bd517-106">Ele deve expor a interface [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) .</span><span class="sxs-lookup"><span data-stu-id="bd517-106">It must expose the [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) interface.</span></span>
-   <span data-ttu-id="bd517-107">O modelo de Threading deve ser ' both '.</span><span class="sxs-lookup"><span data-stu-id="bd517-107">The threading model must be 'both'.</span></span> <span data-ttu-id="bd517-108">DMOs deve funcionar corretamente em um ambiente de thread livre.</span><span class="sxs-lookup"><span data-stu-id="bd517-108">DMOs must function correctly in a free-threaded environment.</span></span>

<span data-ttu-id="bd517-109">O efeito de áudio DMOs deve dar suporte à interface [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) , para uso no DirectMusic e no DirectSound.</span><span class="sxs-lookup"><span data-stu-id="bd517-109">Audio effect DMOs should support the [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) interface, for use in DirectMusic and DirectSound.</span></span>

<span data-ttu-id="bd517-110">As interfaces a seguir estão documentadas em outro lugar, mas são úteis para muitas DMOs.</span><span class="sxs-lookup"><span data-stu-id="bd517-110">The following interfaces are documented elsewhere, but are useful for many DMOs.</span></span> <span data-ttu-id="bd517-111">No entanto, eles não são necessários.</span><span class="sxs-lookup"><span data-stu-id="bd517-111">They are not required, however.</span></span>

-   <span data-ttu-id="bd517-112">**ISpecifyPropertyPages**, **IPropertyPage**: essas interfaces permitem que um DMO forneça uma página de propriedades para que o usuário defina propriedades.</span><span class="sxs-lookup"><span data-stu-id="bd517-112">**ISpecifyPropertyPages**, **IPropertyPage**: These interfaces enable a DMO to provide a property page, for the user to set properties.</span></span>
-   <span data-ttu-id="bd517-113">**IPersistStream**: essa interface permite que o DMO salve seu estado no armazenamento persistente.</span><span class="sxs-lookup"><span data-stu-id="bd517-113">**IPersistStream**: This interface enables the DMO to save its state to persistent storage.</span></span>
-   <span data-ttu-id="bd517-114">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression): essas interfaces permitem que um cliente configure o formato de saída do codificador e as configurações de compactação.</span><span class="sxs-lookup"><span data-stu-id="bd517-114">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression): These interfaces enable a client to configure an encoder's output format and compression settings.</span></span> <span data-ttu-id="bd517-115">(Essas duas interfaces fazem parte da API do DirectShow, mas também são recomendadas para DMOs.)</span><span class="sxs-lookup"><span data-stu-id="bd517-115">(These two interfaces are part of the DirectShow API, but are also recommended for DMOs.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd517-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bd517-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd517-117">Escrevendo um DMO</span><span class="sxs-lookup"><span data-stu-id="bd517-117">Writing a DMO</span></span>](writing-a-dmo.md)
</dt> </dl>

 

 



