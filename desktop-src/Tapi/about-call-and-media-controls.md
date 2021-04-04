---
description: Os controles de mídia e de chamada TAPI 3 são um conjunto genérico de objetos COM, interfaces e métodos para fazer chamadas entre dois ou mais computadores.
ms.assetid: e345df2f-1b68-41be-ac2d-b771136ee831
title: Sobre controles de chamada e de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae65d1a10d004cb16e0ba8753c27665cb7a30ff3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103837662"
---
# <a name="about-call-and-media-controls"></a><span data-ttu-id="d99d8-103">Sobre controles de chamada e de mídia</span><span class="sxs-lookup"><span data-stu-id="d99d8-103">About Call And Media Controls</span></span>

<span data-ttu-id="d99d8-104">Os controles de mídia e de chamada TAPI 3 são um conjunto genérico de objetos COM, interfaces e métodos para fazer chamadas entre dois ou mais computadores.</span><span class="sxs-lookup"><span data-stu-id="d99d8-104">TAPI 3 call and media controls are a generic set of COM objects, interfaces, and methods for making calls between two or more machines.</span></span> <span data-ttu-id="d99d8-105">No contexto da TAPI 3, a *chamada* se refere não apenas à transmissão de voz pela PSTN (rede telefônica pública comutada), mas a qualquer mecanismo de médio e transporte para o qual os provedores de serviço existem: por exemplo, uma conferência de multicast de multimídia em execução em uma intranet corporativa.</span><span class="sxs-lookup"><span data-stu-id="d99d8-105">In the context of TAPI 3, *call* refers not just to voice transmission over the public switched telephone network (PSTN) but to any medium and transport mechanism for which service providers exist: for example, a multimedia multicast conference running on a corporate intranet.</span></span>

<span data-ttu-id="d99d8-106">Os cinco objetos principais na arquitetura de controle de mídia e chamada TAPI 3 são [TAPI](tapi-object.md), [endereço](address-object.md), [terminal](terminal-object.md), [Call](call-object.md)e [CallHub](callhub-object.md).</span><span class="sxs-lookup"><span data-stu-id="d99d8-106">The five main objects in the TAPI 3 call and media control architecture are [TAPI](tapi-object.md), [Address](address-object.md), [Terminal](terminal-object.md), [Call](call-object.md), and [CallHub](callhub-object.md).</span></span> <span data-ttu-id="d99d8-107">Além disso, o provisionamento foi feito para [interfaces específicas do provedor](provider-specific-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="d99d8-107">In addition, provision has been made for [provider-specific interfaces](provider-specific-interfaces.md).</span></span>

<span data-ttu-id="d99d8-108">O diagrama a seguir ilustra como esses objetos interagem.</span><span class="sxs-lookup"><span data-stu-id="d99d8-108">The following diagram illustrates how these objects interact.</span></span>

![interações entre os objetos de controle de mídia e de chamada TAPI 3,0](images/sdkobj2.png)

## <a name="features"></a><span data-ttu-id="d99d8-110">Recursos</span><span class="sxs-lookup"><span data-stu-id="d99d8-110">Features</span></span>

-   <span data-ttu-id="d99d8-111">Abstrai a funcionalidade de chamada e de mídia para permitir que protocolos de comunicação diferentes e aparentemente incompatíveis exponham uma interface comum aos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="d99d8-111">Abstracts both call and media functionality to allow different and seemingly incompatible communication protocols to expose a common interface to applications.</span></span>
-   <span data-ttu-id="d99d8-112">Com base no Component Object Model (COM), para que os aplicativos possam ser escritos em praticamente qualquer linguagem.</span><span class="sxs-lookup"><span data-stu-id="d99d8-112">Based on the Component Object Model (COM) so applications can be written in nearly any language.</span></span> <span data-ttu-id="d99d8-113">Se você precisar de informações adicionais sobre COM, consulte o SDK (Software Development Kit) da plataforma.</span><span class="sxs-lookup"><span data-stu-id="d99d8-113">If you require additional information on COM, please consult the Platform Software Development Kit (SDK).</span></span>
-   <span data-ttu-id="d99d8-114">Controle de chamada fornecido por TSPs (provedores de serviços de telefonia), que implementam mecanismos específicos de transporte.</span><span class="sxs-lookup"><span data-stu-id="d99d8-114">Call control provided by Telephony Service Providers (TSPs), which implement transport-specific mechanisms.</span></span>
-   <span data-ttu-id="d99d8-115">Controle de mídia fornecido pelos provedores de serviços de mídia (MSPs).</span><span class="sxs-lookup"><span data-stu-id="d99d8-115">Media control provided by Media Service providers (MSPs).</span></span> <span data-ttu-id="d99d8-116">O MSPs atual usa o DirectShow.</span><span class="sxs-lookup"><span data-stu-id="d99d8-116">Current MSPs use DirectShow.</span></span> <span data-ttu-id="d99d8-117">O DirectShow é um sistema modular de componentes conectáveis chamados filtros, organizados em uma configuração chamada de grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="d99d8-117">DirectShow is a modular system of pluggable components called filters, arranged in a configuration called a filter graph.</span></span> <span data-ttu-id="d99d8-118">O Gerenciador de gráfico de filtro supervisiona a conexão desses filtros e controla o fluxo de dados do fluxo.</span><span class="sxs-lookup"><span data-stu-id="d99d8-118">The filter graph manager oversees the connection of these filters and controls the stream's data flow.</span></span> <span data-ttu-id="d99d8-119">Se você precisar de informações adicionais sobre o DirectShow, consulte o SDK da plataforma.</span><span class="sxs-lookup"><span data-stu-id="d99d8-119">If you require additional information on DirectShow, please consult the Platform SDK.</span></span>

 

 



