---
description: Detector de mídia (MediaDet)
ms.assetid: 5cdbb6ca-d2c3-4123-b545-198863fed25f
title: Detector de mídia (MediaDet)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90f34b1dc267480d3d6ea9efe9b9a743623a917b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104091883"
---
# <a name="media-detector-mediadet"></a><span data-ttu-id="815b4-103">Detector de mídia (MediaDet)</span><span class="sxs-lookup"><span data-stu-id="815b4-103">Media Detector (MediaDet)</span></span>

> [!Note]  
> <span data-ttu-id="815b4-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="815b4-104">\[Deprecated.</span></span> <span data-ttu-id="815b4-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="815b4-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="815b4-106">O objeto detector de mídia (MediaDet) recupera informações de formato e ainda quadros de fontes de arquivo.</span><span class="sxs-lookup"><span data-stu-id="815b4-106">The Media Detector (MediaDet) object retrieves format information and still frames from file sources.</span></span> <span data-ttu-id="815b4-107">O detector de mídia não exige que o Gerenciador de gráficos de filtro funcione.</span><span class="sxs-lookup"><span data-stu-id="815b4-107">The Media Detector does not require the Filter Graph Manager to function.</span></span> <span data-ttu-id="815b4-108">Para criar esse objeto, chame **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="815b4-108">To create this object, call **CoCreateInstance**.</span></span> <span data-ttu-id="815b4-109">O identificador de classe é CLSID \_ MediaDet.</span><span class="sxs-lookup"><span data-stu-id="815b4-109">The class identifier is CLSID\_MediaDet.</span></span>

<span data-ttu-id="815b4-110">Para ler arquivos do Windows Media™, o aplicativo deve fornecer um certificado de software, também chamado de chave.</span><span class="sxs-lookup"><span data-stu-id="815b4-110">To read Windows Media™ files, the application must provide a software certificate, also called a key.</span></span> <span data-ttu-id="815b4-111">Registre o aplicativo como um provedor de chaves por meio da interface **IObjectWithSite** do detector de mídia.</span><span class="sxs-lookup"><span data-stu-id="815b4-111">Register the application as a key provider through the Media Detector's **IObjectWithSite** interface.</span></span> <span data-ttu-id="815b4-112">Para obter mais informações, consulte [desbloqueando o SDK do Windows Media Format](unlocking-the-windows-media-format-sdk.md).</span><span class="sxs-lookup"><span data-stu-id="815b4-112">For more information, see [Unlocking the Windows Media Format SDK](unlocking-the-windows-media-format-sdk.md).</span></span>

<span data-ttu-id="815b4-113">O objeto MediaDet expõe as seguintes interfaces:</span><span class="sxs-lookup"><span data-stu-id="815b4-113">The MediaDet object exposes the following interfaces:</span></span>

-   [<span data-ttu-id="815b4-114">**IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="815b4-114">**IMediaDet**</span></span>](imediadet.md)
-   <span data-ttu-id="815b4-115">**IObjectWithSite**</span><span class="sxs-lookup"><span data-stu-id="815b4-115">**IObjectWithSite**</span></span>

## <a name="related-topics"></a><span data-ttu-id="815b4-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="815b4-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="815b4-117">Trabalhando com fontes</span><span class="sxs-lookup"><span data-stu-id="815b4-117">Working with Sources</span></span>](working-with-sources.md)
</dt> </dl>

 

 



