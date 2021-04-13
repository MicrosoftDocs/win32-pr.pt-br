---
title: Roteamento de solicitações de entrada
description: A API do servidor HTTP mantém um banco de dados de roteamento para determinar qual aplicativo recebe uma solicitação de entrada.
ms.assetid: 7c613137-66bd-4375-93cb-b5562823bc12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da483030441f3a9239eef153da59212166bce9eb
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104366886"
---
# <a name="routing-incoming-requests"></a><span data-ttu-id="5288c-103">Roteamento de solicitações de entrada</span><span class="sxs-lookup"><span data-stu-id="5288c-103">Routing Incoming Requests</span></span>

<span data-ttu-id="5288c-104">A API do servidor HTTP mantém um banco de dados de roteamento para determinar qual aplicativo recebe uma solicitação de entrada.</span><span class="sxs-lookup"><span data-stu-id="5288c-104">The HTTP Server API maintains a routing database to determine which application receives an incoming request.</span></span> <span data-ttu-id="5288c-105">A tabela de roteamento é criada a partir do banco de dados de reserva e contém entradas de reserva, bem como registros atuais.</span><span class="sxs-lookup"><span data-stu-id="5288c-105">The routing table is built from the reservation database and contains reservation entries as well as current registrations.</span></span> <span data-ttu-id="5288c-106">Quando um registro ou reserva é feito, ele é colocado no Bucket do banco de dados de roteamento que corresponde ao tipo de host da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="5288c-106">When a registration or reservation is made, it is placed into the routing database bucket that corresponds to the host type as follows:</span></span>

-   <span data-ttu-id="5288c-107">\+ : os registros de porta são colocados no Bucket "curinga forte"</span><span class="sxs-lookup"><span data-stu-id="5288c-107">\+ : port registrations are placed in the "Strong Wildcard" bucket</span></span>

-   <span data-ttu-id="5288c-108">host: os registros de porta são colocados no Bucket "Explicit"</span><span class="sxs-lookup"><span data-stu-id="5288c-108">host : port registrations are placed in the "Explicit" bucket</span></span>

-   <span data-ttu-id="5288c-109">IP: os registros de porta são colocados no Bucket "curinga fraco com limite de IP"</span><span class="sxs-lookup"><span data-stu-id="5288c-109">IP : port registrations are placed in the "IP-bound Weak Wildcard" bucket</span></span>

-   <span data-ttu-id="5288c-110">\* : os registros de porta são colocados no Bucket "curinga fraco"</span><span class="sxs-lookup"><span data-stu-id="5288c-110">\* : port registrations are placed in the "Weak Wildcard" bucket</span></span>

<span data-ttu-id="5288c-111">Essas etapas também se referem à ordem em que as solicitações HTTP de entrada são processadas.</span><span class="sxs-lookup"><span data-stu-id="5288c-111">These steps also refer to the order incoming HTTP requests are processed.</span></span> <span data-ttu-id="5288c-112">As reservas de curinga fortes primeiro, em seguida, a reserva explícita são verificadas, seguidas pelo curinga fraco de IP e por curinga fraco.</span><span class="sxs-lookup"><span data-stu-id="5288c-112">The strong wildcard reservations first, then the explicit reservation are checked followed by the IP-bound weak wildcard and weak wildcard.</span></span> <span data-ttu-id="5288c-113">A pesquisa para quando uma correspondência é encontrada para que os registros em qualquer um dos buckets restantes não sejam encontrados.</span><span class="sxs-lookup"><span data-stu-id="5288c-113">The search stops when a match is found so that registrations in any of the remaining buckets are not found.</span></span>

<span data-ttu-id="5288c-114">O algoritmo de roteamento da API do servidor HTTP localiza a melhor correspondência para o [URLPrefix](urlprefix-strings.md) pesquisando as entradas de registro e as entradas de reserva do banco de dados de roteamento, começando com o Bucket curinga forte e terminando com o Bucket de curinga fraco.</span><span class="sxs-lookup"><span data-stu-id="5288c-114">The HTTP Server API routing algorithm locates the best match for the [UrlPrefix](urlprefix-strings.md) by searching both the registration entries and the reservation entries of the routing database, starting with the strong wildcard bucket and ending with the weak wildcard bucket.</span></span> <span data-ttu-id="5288c-115">A melhor correspondência, dentro de um Bucket, é a correspondência mais longa na parte do URI relativo do UrlPrefix (supondo uma correspondência exata para as partes do host, da porta e do esquema da URL).</span><span class="sxs-lookup"><span data-stu-id="5288c-115">The best match, within a bucket, is the longest match in the relative URI portion of the UrlPrefix (assuming an exact match for the host, port and scheme portions of the URL).</span></span> <span data-ttu-id="5288c-116">Depois que uma correspondência for encontrada em um Bucket, o algoritmo de roteamento interromperá sua pesquisa e ignorará todos os buckets de prioridade mais baixa.</span><span class="sxs-lookup"><span data-stu-id="5288c-116">After a match is found in a bucket, the routing algorithm stops its search and skips all lower priority buckets.</span></span>

<span data-ttu-id="5288c-117">Por exemplo, considere os seguintes registros (listados em ordem decrescente de prioridade com base em tipos de Bucket:</span><span class="sxs-lookup"><span data-stu-id="5288c-117">For example, consider the following registrations (listed in descending order of priority based on bucket types:</span></span>

-   <span data-ttu-id="5288c-118">Registro: `https://+:80/vroot/` é registrado pelo aplicativo 1</span><span class="sxs-lookup"><span data-stu-id="5288c-118">Registration: `https://+:80/vroot/` is registered by application 1</span></span>

-   <span data-ttu-id="5288c-119">Registro: `https://adatum.com:80/` é registrado pelo aplicativo 2</span><span class="sxs-lookup"><span data-stu-id="5288c-119">Registration: `https://adatum.com:80/` is registered by application 2</span></span>

-   <span data-ttu-id="5288c-120">Registro: `https://\*:80/` é registrado pelo aplicativo 3</span><span class="sxs-lookup"><span data-stu-id="5288c-120">Registration: `https://\*:80/` is registered by application 3</span></span>

<span data-ttu-id="5288c-121">Uma solicitação de entrada para `https://adatum.com:80/vroot/subdir/file.htm/` é entregue ao aplicativo 1.</span><span class="sxs-lookup"><span data-stu-id="5288c-121">An incoming request for `https://adatum.com:80/vroot/subdir/file.htm/` is delivered to application 1.</span></span> <span data-ttu-id="5288c-122">Uma solicitação de entrada para `https://adatum.com:80/default.htm/` é entregue ao aplicativo 2.</span><span class="sxs-lookup"><span data-stu-id="5288c-122">An incoming request for `https://adatum.com:80/default.htm/` is delivered to application 2.</span></span> <span data-ttu-id="5288c-123">Uma solicitação de entrada para `https://otheradatum.com:80/file.htm/` é entregue ao aplicativo 3.</span><span class="sxs-lookup"><span data-stu-id="5288c-123">An incoming request for `https://otheradatum.com:80/file.htm/` is delivered to application 3.</span></span>

<span data-ttu-id="5288c-124">Se a melhor correspondência for uma entrada de reserva, isso significa que o aplicativo que deve receber a solicitação não está em execução.</span><span class="sxs-lookup"><span data-stu-id="5288c-124">If the best match is a reservation entry, this means that the application that should receive the request is not running.</span></span> <span data-ttu-id="5288c-125">Por exemplo, considere o seguinte registro e reserva:</span><span class="sxs-lookup"><span data-stu-id="5288c-125">For example, consider the following registration and reservation:</span></span>

-   <span data-ttu-id="5288c-126">Registro: `https://\*:80/vroot/` é registrado pelo aplicativo 1, usuário A</span><span class="sxs-lookup"><span data-stu-id="5288c-126">Registration: `https://\*:80/vroot/` is registered by application 1, user A</span></span>

-   <span data-ttu-id="5288c-127">Reserva: `https://adatum.com:80/` foi reservado para o usuário B</span><span class="sxs-lookup"><span data-stu-id="5288c-127">Reservation: `https://adatum.com:80/` has been reserved for user B</span></span>

<span data-ttu-id="5288c-128">Uma solicitação de entrada para `https://adatum.com:80/vroot/file.htm/` o não é entregue ao aplicativo 1 porque a melhor correspondência leva à entrada de reserva para o usuário B. As regras de precedência são aplicadas nesse caso à reserva que tem uma prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="5288c-128">An incoming request for `https://adatum.com:80/vroot/file.htm/` is not delivered to application 1 because the best match leads to the reservation entry for user B. The precedence rules are applied in this case to the reservation which has a higher priority.</span></span> <span data-ttu-id="5288c-129">Se nenhum processo estiver ativo que seja autorizado e registrado para solicitações de serviço para a URL recebida, a solicitação será rejeitada com um código de status 400 (solicitação inadequada).</span><span class="sxs-lookup"><span data-stu-id="5288c-129">If no process is active that is authorized and registered to service requests for the URL received, the request is rejected with a 400 status code (Bad Request).</span></span>

 

 




