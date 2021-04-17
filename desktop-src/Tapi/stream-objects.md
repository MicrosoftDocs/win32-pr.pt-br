---
description: Os objetos Stream são uma abstração do fluxo de mídia ou dos fluxos associados a uma sessão de chamada.
ms.assetid: 4bd7a305-69ff-4892-bf03-df9c6479adab
title: Objetos de fluxo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeb89dbacf73baaffbca9aa3791aa73937a69e80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105784080"
---
# <a name="stream-objects"></a><span data-ttu-id="cc3c5-103">Objetos de fluxo</span><span class="sxs-lookup"><span data-stu-id="cc3c5-103">Stream Objects</span></span>

<span data-ttu-id="cc3c5-104">Os objetos Stream são uma abstração do fluxo de mídia ou dos fluxos associados a uma sessão de chamada.</span><span class="sxs-lookup"><span data-stu-id="cc3c5-104">Stream objects are an abstraction of the media stream or streams associated with a call session.</span></span> <span data-ttu-id="cc3c5-105">As interfaces e os métodos expostos nos objetos Stream e substream permitem que um aplicativo exerça controles muito detalhados, como pausar um fluxo, adicionar novos tipos de mídia a uma sessão de comunicações ou ajustar o volume de áudio de um participante de conferência específico.</span><span class="sxs-lookup"><span data-stu-id="cc3c5-105">The interfaces and methods exposed on stream and substream objects allow an application to exercise very detailed controls such as pausing a stream, adding new media types to a communications session, or adjusting the audio volume of a particular conference participant.</span></span>

<span data-ttu-id="cc3c5-106">Os dois tipos principais de fluxo são o fluxo e o Subfluxo.</span><span class="sxs-lookup"><span data-stu-id="cc3c5-106">The two main types of stream are the stream and the substream.</span></span> <span data-ttu-id="cc3c5-107">As interfaces e os métodos de uma implementação padrão são semelhantes para ambos, mas o Subfluxo permite um nível inferior de controle.</span><span class="sxs-lookup"><span data-stu-id="cc3c5-107">The interfaces and methods of a standard implementation are similar for both, but substreaming allowing a lower level of control.</span></span> <span data-ttu-id="cc3c5-108">Todos os provedores de serviços de mídia (MSPs) devem implementar as interfaces básicas de controle de fluxo, mas o suporte a subfluxos é opcional.</span><span class="sxs-lookup"><span data-stu-id="cc3c5-108">All media service providers (MSPs) must implement the basic stream control interfaces, but support for substreams is optional.</span></span>

<span data-ttu-id="cc3c5-109">Além disso, alguns provedores de serviços implementam [interfaces específicas do provedor](provider-specific-interfaces.md) para fluxos.</span><span class="sxs-lookup"><span data-stu-id="cc3c5-109">In addition, some service providers implement [provider-specific interfaces](provider-specific-interfaces.md) for streams.</span></span> <span data-ttu-id="cc3c5-110">Por exemplo, o IPConf MSP fornece controles de nível de participante.</span><span class="sxs-lookup"><span data-stu-id="cc3c5-110">For example, the IPConf MSP provides participant level controls.</span></span> <span data-ttu-id="cc3c5-111">Consulte [IPConf MSP interfaces](ipconf-msp-interfaces.md) para obter um resumo.</span><span class="sxs-lookup"><span data-stu-id="cc3c5-111">See [IPConf MSP Interfaces](ipconf-msp-interfaces.md) for a summary.</span></span> <span data-ttu-id="cc3c5-112">Para outras interfaces que podem ser implementadas, consulte a documentação do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="cc3c5-112">For other interfaces that might be implemented, see the service provider's documentation.</span></span>

<span data-ttu-id="cc3c5-113">O MSP e a TAPI criam objetos Stream para uma chamada durante a configuração inicial de uma sessão de saída ou de entrada.</span><span class="sxs-lookup"><span data-stu-id="cc3c5-113">The MSP and TAPI create stream objects for a call during initial setup of an outgoing or incoming session.</span></span> <span data-ttu-id="cc3c5-114">O aplicativo é responsável por identificar os terminais apropriados para esses fluxos e selecionar os terminais nos fluxos.</span><span class="sxs-lookup"><span data-stu-id="cc3c5-114">The application is responsible for identifying appropriate terminals for these streams, and selecting the terminals onto the streams.</span></span>

<span data-ttu-id="cc3c5-115">Observe que, em alguns casos, um MSP pode exigir que o aplicativo pare ou PAUSE fluxos antes de determinadas operações de sessão de chamada.</span><span class="sxs-lookup"><span data-stu-id="cc3c5-115">Note that in some cases an MSP may require that the application stop or pause streams prior to certain call session operations.</span></span>

<span data-ttu-id="cc3c5-116">As interfaces de fluxo são documentadas na [referência de MSPI (interface do provedor de serviço de mídia)](media-service-provider-interface-mspi-reference.md).</span><span class="sxs-lookup"><span data-stu-id="cc3c5-116">The stream interfaces are documented in the [Media Service Provider Interface (MSPI) Reference](media-service-provider-interface-mspi-reference.md).</span></span>

<span data-ttu-id="cc3c5-117">O exemplo [selecionar um](select-a-terminal.md) código de terminal mostra um exemplo de como enumerar fluxos e selecionar os terminais neles.</span><span class="sxs-lookup"><span data-stu-id="cc3c5-117">The [Select a Terminal](select-a-terminal.md) code example shows an example of enumerating streams and selecting terminals onto them.</span></span>

 

 



