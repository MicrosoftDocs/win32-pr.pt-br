---
description: Linha do tempo
ms.assetid: 6cc36034-224c-4126-873b-0cfeceec9781
title: Linha do tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10d1f802f12df6ca3469b8283bd4fe8b27e22412
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787126"
---
# <a name="timeline"></a><span data-ttu-id="cbd6e-103">Linha do tempo</span><span class="sxs-lookup"><span data-stu-id="cbd6e-103">Timeline</span></span>

> [!Note]  
> <span data-ttu-id="cbd6e-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-104">\[Deprecated.</span></span> <span data-ttu-id="cbd6e-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cbd6e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="cbd6e-106">O objeto Timeline gerencia todos os objetos em um projeto de edição de vídeo.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-106">The timeline object manages all of the objects in a video editing project.</span></span> <span data-ttu-id="cbd6e-107">Para criar esse objeto, chame **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-107">To create this object, call **CoCreateInstance**.</span></span> <span data-ttu-id="cbd6e-108">O identificador de classe é CLSID \_ AMTimeline.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-108">The class identifier is CLSID\_AMTimeline.</span></span>

<span data-ttu-id="cbd6e-109">Para ler arquivos do Windows Media™, o aplicativo deve fornecer um certificado de software, também chamado de chave.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-109">To read Windows Media™ files, the application must provide a software certificate, also called a key.</span></span> <span data-ttu-id="cbd6e-110">Registre o aplicativo como um provedor de chaves por meio da interface **IObjectWithSite** da linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-110">Register the application as a key provider through the timeline's **IObjectWithSite** interface.</span></span> <span data-ttu-id="cbd6e-111">Para obter mais informações, consulte [desbloqueando o SDK do Windows Media Format](unlocking-the-windows-media-format-sdk.md).</span><span class="sxs-lookup"><span data-stu-id="cbd6e-111">For more information, see [Unlocking the Windows Media Format SDK](unlocking-the-windows-media-format-sdk.md).</span></span>

<span data-ttu-id="cbd6e-112">O objeto Timeline expõe as seguintes interfaces:</span><span class="sxs-lookup"><span data-stu-id="cbd6e-112">The timeline object exposes the following interfaces:</span></span>

-   [<span data-ttu-id="cbd6e-113">**IAMSetErrorLog**</span><span class="sxs-lookup"><span data-stu-id="cbd6e-113">**IAMSetErrorLog**</span></span>](iamseterrorlog.md)
-   [<span data-ttu-id="cbd6e-114">**IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="cbd6e-114">**IAMTimeline**</span></span>](iamtimeline.md)
-   <span data-ttu-id="cbd6e-115">**IObjectWithSite**</span><span class="sxs-lookup"><span data-stu-id="cbd6e-115">**IObjectWithSite**</span></span>
-   <span data-ttu-id="cbd6e-116">**IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="cbd6e-116">**IPersistStream**</span></span>

## <a name="related-topics"></a><span data-ttu-id="cbd6e-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cbd6e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbd6e-118">O modelo de linha do tempo</span><span class="sxs-lookup"><span data-stu-id="cbd6e-118">The Timeline Model</span></span>](the-timeline-model.md)
</dt> <dt>

[<span data-ttu-id="cbd6e-119">Construindo uma linha do tempo</span><span class="sxs-lookup"><span data-stu-id="cbd6e-119">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 



