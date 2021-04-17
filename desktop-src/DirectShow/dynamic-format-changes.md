---
description: Alterações de formato dinâmico
ms.assetid: ff60de5a-3edc-405d-aa02-8704b96d5e87
title: Alterações de formato dinâmico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49496e0b43d9b120f6daf27007cde98191a7765b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105789902"
---
# <a name="dynamic-format-changes"></a><span data-ttu-id="3373e-103">Alterações de formato dinâmico</span><span class="sxs-lookup"><span data-stu-id="3373e-103">Dynamic Format Changes</span></span>

<span data-ttu-id="3373e-104">Quando dois filtros se conectam, eles concordam em um tipo de mídia, que descreve o formato dos dados que o filtro upstream fornecerá.</span><span class="sxs-lookup"><span data-stu-id="3373e-104">When two filters connect, they agree on a media type, which describes the format of the data that the upstream filter will deliver.</span></span> <span data-ttu-id="3373e-105">Na maioria dos casos, o tipo de mídia é fixo pela duração da conexão.</span><span class="sxs-lookup"><span data-stu-id="3373e-105">In most cases, the media type is fixed for the duration of the connection.</span></span> <span data-ttu-id="3373e-106">No entanto, o DirectShow oferece suporte limitado para filtros para alterar o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="3373e-106">However, DirectShow does offer limited support for filters to change the media type.</span></span> <span data-ttu-id="3373e-107">Quando um filtro alterna os tipos de mídia, ele é chamado de *alteração de formato dinâmico*.</span><span class="sxs-lookup"><span data-stu-id="3373e-107">When a filter switches media types, it is called a *dynamic format change*.</span></span> <span data-ttu-id="3373e-108">Se estiver escrevendo um filtro do DirectShow, você deve estar ciente dos mecanismos para alterações de formato dinâmico.</span><span class="sxs-lookup"><span data-stu-id="3373e-108">If you are writing a DirectShow filter, you should be aware of the mechanisms for dynamic format changes.</span></span> <span data-ttu-id="3373e-109">Mesmo que o filtro não ofereça suporte a essas alterações, ele deverá responder corretamente se outro filtro solicitar um novo formato.</span><span class="sxs-lookup"><span data-stu-id="3373e-109">Even if your filter does not support such changes, it should respond correctly if another filter requests a new format.</span></span>

<span data-ttu-id="3373e-110">O DirectShow define vários mecanismos distintos para alterações de formato dinâmico, dependendo do estado do grafo de filtro e do tipo de alteração necessário.</span><span class="sxs-lookup"><span data-stu-id="3373e-110">DirectShow defines several distinct mechanisms for dynamic format changes, depending on the state of filter graph and the type of change that is required.</span></span>

-   <span data-ttu-id="3373e-111">Se o grafo for interrompido, os Pins poderão se reconectar e renegociar o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="3373e-111">If the graph is stopped, the pins can reconnect and renegotiate the media type.</span></span> <span data-ttu-id="3373e-112">Para obter mais informações, consulte [reconectando Pins](reconnecting-pins.md).</span><span class="sxs-lookup"><span data-stu-id="3373e-112">For more information, see [Reconnecting Pins](reconnecting-pins.md).</span></span>
-   <span data-ttu-id="3373e-113">Alguns filtros podem reconectar Pins mesmo enquanto o grafo estiver ativo (em execução ou em pausa).</span><span class="sxs-lookup"><span data-stu-id="3373e-113">Some filters can reconnect pins even while the graph is active (running or paused).</span></span> <span data-ttu-id="3373e-114">Para obter mais informações sobre esse mecanismo, consulte [reconexão dinâmica](dynamic-reconnection.md).</span><span class="sxs-lookup"><span data-stu-id="3373e-114">For more information about this mechanism, see [Dynamic Reconnection](dynamic-reconnection.md).</span></span>

<span data-ttu-id="3373e-115">Caso contrário, se o grafo estiver ativo, mas os filtros em questão não oferecerem suporte a reconexões de PIN dinâmico, haverá três mecanismos possíveis para alterar o formato:</span><span class="sxs-lookup"><span data-stu-id="3373e-115">Otherwise, if the graph is active, but the filters in question do not support dynamic pin reconnections, there are three possible mechanisms for changing the format:</span></span>

-   <span data-ttu-id="3373e-116">O [QueryAccept (downstream)](queryaccept--downstream.md) é usado quando um PIN de saída propõe uma alteração de formato para seu par downstream, mas somente se o novo formato não exigir um buffer maior.</span><span class="sxs-lookup"><span data-stu-id="3373e-116">[QueryAccept (Downstream)](queryaccept--downstream.md) is used when If an output pin proposes a format change to its downstream peer, but only if the new format does not require a larger buffer.</span></span>
-   <span data-ttu-id="3373e-117">[QueryAccept (upstream)](queryaccept--upstream.md) é usado quando um PIN de entrada propõe uma alteração de formato para seu ponto de upstream.</span><span class="sxs-lookup"><span data-stu-id="3373e-117">[QueryAccept (Upstream)](queryaccept--upstream.md) is used when an input pin proposes a format change to its upstream peer.</span></span> <span data-ttu-id="3373e-118">O novo formato pode ter o mesmo tamanho ou pode ser maior.</span><span class="sxs-lookup"><span data-stu-id="3373e-118">The new format can be the same size, or it can be larger.</span></span>
-   <span data-ttu-id="3373e-119">[ReceiveConnection](receiveconnection.md) é usado quando um PIN de saída propõe uma alteração de formato ao seu par downstream, e o novo formato requer um buffer maior.</span><span class="sxs-lookup"><span data-stu-id="3373e-119">[ReceiveConnection](receiveconnection.md) is used when an output pin proposes a format change to its downstream peer, and the new format requires a larger buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3373e-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3373e-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3373e-121">Manipulando alterações de formato do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="3373e-121">Handling Format Changes from the Video Renderer</span></span>](handling-format-changes-from-the-video-renderer.md)
</dt> </dl>

 

 



