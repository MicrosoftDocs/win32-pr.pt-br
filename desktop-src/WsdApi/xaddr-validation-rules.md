---
description: Os endereços de transporte (XAddrs) incluídos nas mensagens ProbeMatches e ResolveMatches estão sujeitos à validação básica antes de o WSDAPI enviar uma mensagem HTTP, como uma solicitação de metadados.
ms.assetid: 6b5139b5-aa31-42bc-a281-8784006edfbe
title: Regras de validação do XAddr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc91ce8a0e1bba267ea92fa79a6680b481297f24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165180"
---
# <a name="xaddr-validation-rules"></a><span data-ttu-id="496c1-103">Regras de validação do XAddr</span><span class="sxs-lookup"><span data-stu-id="496c1-103">XAddr Validation Rules</span></span>

<span data-ttu-id="496c1-104">Os endereços de transporte (XAddrs) incluídos nas mensagens [ProbeMatches](probematches-message.md) e [ResolveMatches](resolvematches-message.md) estão sujeitos à validação básica antes de o WSDAPI enviar uma mensagem http, como uma solicitação de metadados.</span><span class="sxs-lookup"><span data-stu-id="496c1-104">Transport addresses (XAddrs) included in [ProbeMatches](probematches-message.md) and [ResolveMatches](resolvematches-message.md) messages are subject to basic validation before WSDAPI sends an HTTP message, such as a metadata request.</span></span>

<span data-ttu-id="496c1-105">Isso é para garantir que os XAddrs estejam na mesma sub-rede que o cliente.</span><span class="sxs-lookup"><span data-stu-id="496c1-105">This is in order to ensure that the XAddrs are on the same subnet as the client.</span></span>

<span data-ttu-id="496c1-106">O XML a seguir mostra um exemplo de elemento XAddrs.</span><span class="sxs-lookup"><span data-stu-id="496c1-106">The following XML shows a sample XAddrs element.</span></span> <span data-ttu-id="496c1-107">O prefixo WSD refere-se ao namespace `https://schemas.xmlsoap.org/ws/2005/04/discovery` .</span><span class="sxs-lookup"><span data-stu-id="496c1-107">The wsd prefix refers to the namespace `https://schemas.xmlsoap.org/ws/2005/04/discovery`.</span></span>

``` syntax
<wsd:XAddrs>
    https://192.168.0.2:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsd:XAddrs>
```

<span data-ttu-id="496c1-108">Todas as condições a seguir devem ser atendidas antes que a mensagem HTTP seja transmitida pela conexão.</span><span class="sxs-lookup"><span data-stu-id="496c1-108">All of the following conditions must be met before the HTTP message will go out over the wire.</span></span>

-   <span data-ttu-id="496c1-109">XAddrs devem ser endereços HTTP ou HTTPS.</span><span class="sxs-lookup"><span data-stu-id="496c1-109">XAddrs must be HTTP or HTTPS addresses.</span></span> <span data-ttu-id="496c1-110">XAddrs de outros esquemas são ignorados.</span><span class="sxs-lookup"><span data-stu-id="496c1-110">XAddrs of other schemes are ignored.</span></span>
-   <span data-ttu-id="496c1-111">Se qualquer XAddrs HTTPS estiver presente, todos os XAddrs deverão ser HTTPS.</span><span class="sxs-lookup"><span data-stu-id="496c1-111">If any HTTPS XAddrs are present, all XAddrs must be HTTPS.</span></span> <span data-ttu-id="496c1-112">As seções XAddr que incluem endereços HTTP e HTTPS são completamente ignoradas.</span><span class="sxs-lookup"><span data-stu-id="496c1-112">XAddr sections which include both HTTP and HTTPS addresses are completely ignored.</span></span> <span data-ttu-id="496c1-113">Além disso, o endereço do ponto de extremidade do dispositivo deve corresponder exatamente ao XAddrs HTTPS.</span><span class="sxs-lookup"><span data-stu-id="496c1-113">Additionally, the device's endpoint address must match the HTTPS XAddrs exactly.</span></span>
-   <span data-ttu-id="496c1-114">XAddrs devem ser endereços IP ou nomes de host que poderão ser resolvidos por meio do DNS.</span><span class="sxs-lookup"><span data-stu-id="496c1-114">XAddrs must be IP addresses or hostnames resolvable through DNS.</span></span> <span data-ttu-id="496c1-115">Normalmente, os endereços IP são usados.</span><span class="sxs-lookup"><span data-stu-id="496c1-115">Usually, IP addresses are used.</span></span>
-   <span data-ttu-id="496c1-116">Pelo menos um endereço IP incluído no XAddrs (ou o endereço IP resolvido de um nome de host incluído no XAddrs) deve estar na mesma sub-rede que o adaptador no qual a mensagem [ProbeMatches](probematches-message.md) ou [ResolveMatches](resolvematches-message.md) foi recebida.</span><span class="sxs-lookup"><span data-stu-id="496c1-116">At least one IP address included in the XAddrs (or IP address resolved from a hostname included in the XAddrs) must be on the same subnet as the adapter over which the [ProbeMatches](probematches-message.md) or [ResolveMatches](resolvematches-message.md) message was received.</span></span>
-   <span data-ttu-id="496c1-117">O endereço e a porta especificados no primeiro XAddr devem estar acessíveis.</span><span class="sxs-lookup"><span data-stu-id="496c1-117">The address and port specified in the first XAddr must be accessible.</span></span> <span data-ttu-id="496c1-118">O WSDAPI tenta se conectar a esse endereço ao estabelecer uma conexão HTTP.</span><span class="sxs-lookup"><span data-stu-id="496c1-118">WSDAPI attempts to connect to this address when establishing an HTTP connection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="496c1-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="496c1-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="496c1-120">ProbeMatches</span><span class="sxs-lookup"><span data-stu-id="496c1-120">ProbeMatches</span></span>](probematches-message.md)
</dt> <dt>

[<span data-ttu-id="496c1-121">ResolveMatches</span><span class="sxs-lookup"><span data-stu-id="496c1-121">ResolveMatches</span></span>](resolvematches-message.md)
</dt> <dt>

[<span data-ttu-id="496c1-122">Padrões de mensagem de troca de metadados e descoberta</span><span class="sxs-lookup"><span data-stu-id="496c1-122">Discovery and Metadata Exchange Message Patterns</span></span>](discovery-and-metadata-exchange-message-patterns.md)
</dt> </dl>

 

 



