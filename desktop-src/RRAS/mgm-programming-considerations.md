---
title: Considerações sobre programação MGM
description: Ao desenvolver clientes do Gerenciador de grupos de multicast, observe as diretrizes a seguir
ms.assetid: 48451a76-81e0-4d60-acb3-c9ec55de32b4
keywords:
- Multicast, considerações de programação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e442de1dcb2da5a8664648587a88f05feaee970
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822812"
---
# <a name="mgm-programming-considerations"></a><span data-ttu-id="f0fe8-104">Considerações sobre programação MGM</span><span class="sxs-lookup"><span data-stu-id="f0fe8-104">MGM Programming Considerations</span></span>

<span data-ttu-id="f0fe8-105">Ao desenvolver clientes do Gerenciador de grupos de multicast, observe as seguintes diretrizes:</span><span class="sxs-lookup"><span data-stu-id="f0fe8-105">When you are developing multicast group manager clients, observe the following guidelines:</span></span>

-   <span data-ttu-id="f0fe8-106">As chamadas de função devem ser feitas de dentro do processo do roteador.</span><span class="sxs-lookup"><span data-stu-id="f0fe8-106">Function calls must be made from within the router process.</span></span> <span data-ttu-id="f0fe8-107">Se as funções forem chamadas de outro processo, seus resultados não serão válidos; o cliente não irá interagir com o Gerenciador do grupo de multicast.</span><span class="sxs-lookup"><span data-stu-id="f0fe8-107">If functions are called from another process, their results will not be valid; the client will not interact with the multicast group manager.</span></span>
-   <span data-ttu-id="f0fe8-108">Os clientes que usam a API MGM devem fornecer sua própria verificação de erro, garantindo que apenas os dados válidos sejam passados para o Gerenciador do grupo de multicast.</span><span class="sxs-lookup"><span data-stu-id="f0fe8-108">Clients that use the MGM API must provide their own error checking, ensuring that only valid data is passed to the multicast group manager.</span></span> <span data-ttu-id="f0fe8-109">As funções MGM não retornam mensagens de erro detalhadas sobre parâmetros inválidos; o \_ valor de parâmetro inválido do erro \_ é retornado sem explicação.</span><span class="sxs-lookup"><span data-stu-id="f0fe8-109">MGM functions do not return detailed error messages about invalid parameters; the ERROR\_INVALID\_PARAMETER value is returned without explanation.</span></span>
-   <span data-ttu-id="f0fe8-110">Os clientes devem ter cuidado ao usar bloqueios ao chamar funções MGM.</span><span class="sxs-lookup"><span data-stu-id="f0fe8-110">Clients should exercise caution in using locks while calling MGM functions.</span></span> <span data-ttu-id="f0fe8-111">Isso pode impedir deadlocks.</span><span class="sxs-lookup"><span data-stu-id="f0fe8-111">Doing so can prevent deadlocks.</span></span> <span data-ttu-id="f0fe8-112">Ao chamar as funções MGM, os clientes não devem armazenar nenhum bloqueio que possa ser mantido simultaneamente em um retorno de chamada do Gerenciador de grupos multicast.</span><span class="sxs-lookup"><span data-stu-id="f0fe8-112">When calling MGM functions, clients should not hold any locks that might simultaneously be held in a callback from the multicast group manager.</span></span>

 

 




