---
description: Trabalhando com efeitos e transições
ms.assetid: 00e97d02-ff43-4e1f-9806-abaeb9288058
title: Trabalhando com efeitos e transições
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99029269ac86e17246fd641341b071654582bc4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922917"
---
# <a name="working-with-effects-and-transitions"></a><span data-ttu-id="bcc36-103">Trabalhando com efeitos e transições</span><span class="sxs-lookup"><span data-stu-id="bcc36-103">Working with Effects and Transitions</span></span>

<span data-ttu-id="bcc36-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="bcc36-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="bcc36-105">Os efeitos modificam um único clipe, faixa ou composição.</span><span class="sxs-lookup"><span data-stu-id="bcc36-105">Effects modify a single clip, track, or composition.</span></span> <span data-ttu-id="bcc36-106">As transições criam seques de uma faixa ou composições para outra.</span><span class="sxs-lookup"><span data-stu-id="bcc36-106">Transitions create seques from one track or compositionsto another.</span></span>

<span data-ttu-id="bcc36-107">Os [serviços de edição do DirectShow](directshow-editing-services.md) usam objetos de transformação do DirectX para suas transições de vídeo e efeitos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="bcc36-107">[DirectShow Editing Services](directshow-editing-services.md) uses DirectX Transform objects for its video transitions and video effects.</span></span> <span data-ttu-id="bcc36-108">Para transições de vídeo, use qualquer objeto de transformação DirectX de duas entradas 2D.</span><span class="sxs-lookup"><span data-stu-id="bcc36-108">For video transitions, use any 2-D two-input DirectX Transform object.</span></span> <span data-ttu-id="bcc36-109">Para efeitos de vídeo, use qualquer objeto de transformação DirectX de entrada One 2-D.</span><span class="sxs-lookup"><span data-stu-id="bcc36-109">For video effects, use any 2-D one-input DirectX Transform object.</span></span> <span data-ttu-id="bcc36-110">A Microsoft não dá mais suporte ao desenvolvimento de objetos de transformação DirectX de terceiros.</span><span class="sxs-lookup"><span data-stu-id="bcc36-110">Microsoft no longer supports the development of third-party DirectX Transform objects.</span></span> <span data-ttu-id="bcc36-111">No entanto, vários são fornecidos com o DirectShow e outros são fornecidos com o Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="bcc36-111">However, several are provided with DirectShow and others are provided with Microsoft Internet Explorer.</span></span> <span data-ttu-id="bcc36-112">Para obter mais informações sobre as transições fornecidas com o Internet Explorer, consulte [referência de filtros visuais e transições](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms532853(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bcc36-112">For more information about the transitions provided with Internet Explorer, see [Visual Filters and Transitions Reference](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms532853(v=vs.85)).</span></span>

<span data-ttu-id="bcc36-113">Para efeitos de áudio, você pode usar qualquer filtro de efeito de áudio do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="bcc36-113">For audio effects, you can use any DirectShow audio effect filter.</span></span> <span data-ttu-id="bcc36-114">O DES também fornece um [efeito de envelope de volume](volume-envelope-effect.md) para definir o volume em um roteiro ou um clipe.</span><span class="sxs-lookup"><span data-stu-id="bcc36-114">DES also provides a [Volume Envelope Effect](volume-envelope-effect.md) for setting the volume on a track or clip.</span></span> <span data-ttu-id="bcc36-115">O DES não oferece suporte a transições de áudio.</span><span class="sxs-lookup"><span data-stu-id="bcc36-115">DES does not support audio transitions.</span></span>

<span data-ttu-id="bcc36-116">Esta seção contém os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="bcc36-116">This section contains the following topics:</span></span>

-   [<span data-ttu-id="bcc36-117">Adicionando objetos de efeito e transição</span><span class="sxs-lookup"><span data-stu-id="bcc36-117">Adding Effect and Transition Objects</span></span>](adding-effect-and-transition-objects.md)
-   [<span data-ttu-id="bcc36-118">Visualização de efeitos e transições</span><span class="sxs-lookup"><span data-stu-id="bcc36-118">Previewing Effects and Transitions</span></span>](previewing-effects-and-transitions.md)
-   [<span data-ttu-id="bcc36-119">Enumerando efeitos e transições</span><span class="sxs-lookup"><span data-stu-id="bcc36-119">Enumerating Effects and Transitions</span></span>](enumerating-effects-and-transitions.md)
-   [<span data-ttu-id="bcc36-120">Definindo propriedades em efeitos e transições</span><span class="sxs-lookup"><span data-stu-id="bcc36-120">Setting Properties on Effects and Transitions</span></span>](setting-properties-on-effects-and-transitions.md)
-   [<span data-ttu-id="bcc36-121">Direção da transição</span><span class="sxs-lookup"><span data-stu-id="bcc36-121">Transition Direction</span></span>](transition-direction.md)

## <a name="related-topics"></a><span data-ttu-id="bcc36-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bcc36-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bcc36-123">Usando os serviços de edição do DirectShow</span><span class="sxs-lookup"><span data-stu-id="bcc36-123">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 
