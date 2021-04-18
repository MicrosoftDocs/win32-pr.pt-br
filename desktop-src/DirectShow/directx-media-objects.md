---
description: Objetos de mídia do DirectX
ms.assetid: e4424740-31b9-4317-8791-6a9aebb0c7e6
title: Objetos de mídia do DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2119fc8cce602bc1cc085886edd6852320aca180
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105778484"
---
# <a name="directx-media-objects"></a><span data-ttu-id="3b08b-103">Objetos de mídia do DirectX</span><span class="sxs-lookup"><span data-stu-id="3b08b-103">DirectX Media Objects</span></span>

> [!Note]  
> <span data-ttu-id="3b08b-104">DMOs foram substituídas por [Media Foundation transformações](/windows/desktop/medfound/media-foundation-transforms) (MFTs).</span><span class="sxs-lookup"><span data-stu-id="3b08b-104">DMOs have been superseded by [Media Foundation Transforms](/windows/desktop/medfound/media-foundation-transforms) (MFTs).</span></span> <span data-ttu-id="3b08b-105">As interfaces DMO ainda têm suporte.</span><span class="sxs-lookup"><span data-stu-id="3b08b-105">The DMO interfaces are still supported.</span></span> <span data-ttu-id="3b08b-106">No entanto, se você estiver escrevendo um codec personalizado ou um plug-in de processamento de áudio/vídeo, considere implementá-lo como um MFT.</span><span class="sxs-lookup"><span data-stu-id="3b08b-106">However, if you are writing a custom codec or audio/video processing plug-in, you should consider implementing it as an MFT.</span></span>

 

<span data-ttu-id="3b08b-107">Os DMOs (objetos de mídia do DirectX) são componentes de streaming de dados baseados em COM.</span><span class="sxs-lookup"><span data-stu-id="3b08b-107">DirectX Media Objects (DMOs) are COM-based data-streaming components.</span></span> <span data-ttu-id="3b08b-108">Em alguns aspectos, DMOs são semelhantes aos filtros do Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="3b08b-108">In some respects, DMOs are similar to Microsoft DirectShow filters.</span></span> <span data-ttu-id="3b08b-109">Como os filtros do DirectShow, DMOs pegar dados de entrada e usá-los para produzir dados de saída.</span><span class="sxs-lookup"><span data-stu-id="3b08b-109">Like DirectShow filters, DMOs take input data and use it to produce output data.</span></span> <span data-ttu-id="3b08b-110">No entanto, as APIs (interfaces de programação de aplicativo) para DMOs são muito mais simples do que as APIs correspondentes para o DirectShow.</span><span class="sxs-lookup"><span data-stu-id="3b08b-110">However, the application programming interfaces (APIs) for DMOs are much simpler than the corresponding APIs for DirectShow.</span></span> <span data-ttu-id="3b08b-111">Como resultado, DMOs são mais fáceis de criar, testar e usar.</span><span class="sxs-lookup"><span data-stu-id="3b08b-111">As a result, DMOs are easier to create, test, and use.</span></span> <span data-ttu-id="3b08b-112">DMOs pode ser usado em muitos cenários:</span><span class="sxs-lookup"><span data-stu-id="3b08b-112">DMOs can be used in many scenarios:</span></span>

-   <span data-ttu-id="3b08b-113">Aplicativos baseados no DirectShow podem usar o DMOs por meio de um filtro do DirectShow chamado de filtro de [invólucro do DMO](dmo-wrapper-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="3b08b-113">Applications based on DirectShow can use DMOs through a DirectShow filter called the [DMO Wrapper](dmo-wrapper-filter.md) filter.</span></span> <span data-ttu-id="3b08b-114">A distinção entre filtros e DMOs é transparente para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3b08b-114">The distinction between filters and DMOs is transparent to the application.</span></span> <span data-ttu-id="3b08b-115">O aplicativo não chama diretamente as APIs de DMO.</span><span class="sxs-lookup"><span data-stu-id="3b08b-115">The application does not directly call the DMO APIs.</span></span>
-   <span data-ttu-id="3b08b-116">Os aplicativos baseados no Microsoft DirectSound podem usar o efeito de áudio DMOs.</span><span class="sxs-lookup"><span data-stu-id="3b08b-116">Applications based on Microsoft DirectSound can use audio effect DMOs.</span></span> <span data-ttu-id="3b08b-117">Novamente, o aplicativo é blindado das APIs de nível inferior de DMO pelas APIs do DirectSound de nível superior.</span><span class="sxs-lookup"><span data-stu-id="3b08b-117">Again, the application is shielded from the low-level DMO APIs by the higher-level DirectSound APIs.</span></span>
-   <span data-ttu-id="3b08b-118">Os aplicativos podem usar o DMOs diretamente.</span><span class="sxs-lookup"><span data-stu-id="3b08b-118">Applications can use DMOs directly.</span></span>

<span data-ttu-id="3b08b-119">Assim, escrevendo um DMO, você cria um componente que pode ser usado em uma ampla variedade de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="3b08b-119">Thus, by writing a DMO, you create a component that can be used in a wide range of applications.</span></span> <span data-ttu-id="3b08b-120">Esta documentação contém as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="3b08b-120">This documentation contains the following sections:</span></span>

-   [<span data-ttu-id="3b08b-121">Sobre o DMOs</span><span class="sxs-lookup"><span data-stu-id="3b08b-121">About DMOs</span></span>](about-dmos.md)
-   [<span data-ttu-id="3b08b-122">Usando DMOs</span><span class="sxs-lookup"><span data-stu-id="3b08b-122">Using DMOs</span></span>](using-dmos.md)
-   [<span data-ttu-id="3b08b-123">Escrevendo um DMO</span><span class="sxs-lookup"><span data-stu-id="3b08b-123">Writing a DMO</span></span>](writing-a-dmo.md)
-   [<span data-ttu-id="3b08b-124">Parâmetros de mídia</span><span class="sxs-lookup"><span data-stu-id="3b08b-124">Media Parameters</span></span>](media-parameters.md)
-   [<span data-ttu-id="3b08b-125">Referência de DMO</span><span class="sxs-lookup"><span data-stu-id="3b08b-125">DMO Reference</span></span>](dmo-reference.md)

## <a name="related-topics"></a><span data-ttu-id="3b08b-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3b08b-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b08b-127">DirectShow</span><span class="sxs-lookup"><span data-stu-id="3b08b-127">DirectShow</span></span>](directshow.md)
</dt> </dl>

 

 
