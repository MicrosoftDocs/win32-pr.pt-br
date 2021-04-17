---
title: Registro em log (plataforma de filtragem do Windows)
description: A WFP (Windows Filtering Platform) fornece registro em log de quedas de pacotes e falhas de IKE/AuthIP.
ms.assetid: 607b7664-6be4-4ae6-991b-58ac9175405a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a27868c76a643a8e1b7b478152c100a2026bfc20
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105757163"
---
# <a name="logging-windows-filtering-platform"></a><span data-ttu-id="224ed-103">Registro em log (plataforma de filtragem do Windows)</span><span class="sxs-lookup"><span data-stu-id="224ed-103">Logging (Windows Filtering Platform)</span></span>

<span data-ttu-id="224ed-104">A WFP (Windows Filtering Platform) fornece registro em log de quedas de pacotes e falhas de IKE/AuthIP.</span><span class="sxs-lookup"><span data-stu-id="224ed-104">The Windows Filtering Platform (WFP) provides logging of packet drops and IKE/AuthIP failures.</span></span>

<span data-ttu-id="224ed-105">Os eventos registrados são definidos no tipo enumerado [**\_ tipo de \_ evento \_ FWPM net**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_net_event_type) e são os seguintes.</span><span class="sxs-lookup"><span data-stu-id="224ed-105">The logged events are defined in the [**FWPM\_NET\_EVENT\_TYPE**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_net_event_type) enumerated type and are as follows.</span></span>

-   <span data-ttu-id="224ed-106">Falhas no modo principal IKE/AuthIP.</span><span class="sxs-lookup"><span data-stu-id="224ed-106">IKE/AuthIP main mode failures.</span></span>
-   <span data-ttu-id="224ed-107">Falhas de modo rápido IKE/AuthIP.</span><span class="sxs-lookup"><span data-stu-id="224ed-107">IKE/AuthIP quick mode failures.</span></span>
-   <span data-ttu-id="224ed-108">Falhas de modo estendido AuthIP.</span><span class="sxs-lookup"><span data-stu-id="224ed-108">AuthIP extended mode failures.</span></span>
-   <span data-ttu-id="224ed-109">Pacotes removidos durante a classificação.</span><span class="sxs-lookup"><span data-stu-id="224ed-109">Packets dropped during classification.</span></span>
-   <span data-ttu-id="224ed-110">Pacotes removidos pelo IPsec.</span><span class="sxs-lookup"><span data-stu-id="224ed-110">Packets dropped by IPsec.</span></span>

<span data-ttu-id="224ed-111">Por padrão, o log para WFP é habilitado para pacotes de entrada unicast e para todos os pacotes de saída (unicast, multicast e difusão).</span><span class="sxs-lookup"><span data-stu-id="224ed-111">By default, logging for WFP is enabled for unicast inbound packets and for all outbound packets (unicast, multicast, and broadcast).</span></span> <span data-ttu-id="224ed-112">O registro em log pode ser habilitado para o restante dos pacotes ou desabilitado para todos os pacotes, por meio da função de gerenciamento [**FwpmEngineSetOptions0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0) .</span><span class="sxs-lookup"><span data-stu-id="224ed-112">Logging can be enabled for the rest of the packets, or disabled for all packets, through the [**FwpmEngineSetOptions0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0) management function.</span></span> <span data-ttu-id="224ed-113">As configurações de evento persistem entre reinicializações.</span><span class="sxs-lookup"><span data-stu-id="224ed-113">Event settings persist across reboots.</span></span>

<span data-ttu-id="224ed-114">Os eventos registrados são armazenados em um log circular, que são novos eventos que substituem os antigos quando o log atinge seu tamanho máximo e podem ser analisados usando as funções de [Gerenciamento de eventos](fwp-mgmt-functions.md) fornecidas pela WFP.</span><span class="sxs-lookup"><span data-stu-id="224ed-114">Logged events are stored in a circular log, that is new events override old ones when the log reaches its maximum size, and can be analyzed using the [event management](fwp-mgmt-functions.md) functions provided by WFP.</span></span> <span data-ttu-id="224ed-115">O log de eventos tem um tamanho máximo de 128 KB e pode conter cerca de 100 a 150 eventos.</span><span class="sxs-lookup"><span data-stu-id="224ed-115">The event log has a maximum size of 128 KB and it can hold about 100 to 150 events.</span></span>

<span data-ttu-id="224ed-116">As funções de enumeração em geral e [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) / [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) em particular fazem um instantâneo do log no momento em que o identificador de enumeração é criado.</span><span class="sxs-lookup"><span data-stu-id="224ed-116">Enumeration functions in general, and [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0)/[**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) in particular, take a snapshot of the log at the time the enumeration handle is created.</span></span> <span data-ttu-id="224ed-117">As chamadas subsequentes usando o mesmo identificador de enumeração retornam o próximo conjunto de itens após aqueles no último buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="224ed-117">Subsequent calls using the same enumeration handle return the next set of items following those in the last output buffer.</span></span>

<span data-ttu-id="224ed-118">Quando um aplicativo desabilita o log de WFP (chamando [**FwpmEngineSetOptions0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)), todos os aplicativos são afetados.</span><span class="sxs-lookup"><span data-stu-id="224ed-118">When an application disables WFP logging (by calling [**FwpmEngineSetOptions0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)) all applications are affected.</span></span> <span data-ttu-id="224ed-119">O log de eventos não é limpo até que um aplicativo habilite novamente o log WFP, mas o log de eventos não pode ser consultado antes.</span><span class="sxs-lookup"><span data-stu-id="224ed-119">The event log is not cleaned up until an application re-enables WFP logging, but the event log cannot be queried before then.</span></span>

<span data-ttu-id="224ed-120">O log de eventos do WFP é esvaziado após uma reinicialização.</span><span class="sxs-lookup"><span data-stu-id="224ed-120">The WFP event log is emptied after a reboot.</span></span>

 

 




