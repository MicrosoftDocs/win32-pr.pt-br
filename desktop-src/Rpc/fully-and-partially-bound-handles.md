---
title: Identificadores totalmente e parcialmente ligados
description: Quando você usa pontos de extremidade dinâmicos, as bibliotecas de tempo de execução obtêm as informações de Endpoint conforme elas precisam.
ms.assetid: 13f2f783-2c10-4122-ba4d-a97b9c0378c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc1f434ec53ebcfd992b0090ed9066dce2ec627
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453616"
---
# <a name="fully-and-partially-bound-handles"></a><span data-ttu-id="02206-103">Identificadores totalmente e parcialmente ligados</span><span class="sxs-lookup"><span data-stu-id="02206-103">Fully and Partially Bound Handles</span></span>

<span data-ttu-id="02206-104">Quando você usa pontos de extremidade dinâmicos, as bibliotecas de tempo de execução obtêm as informações de Endpoint conforme elas precisam.</span><span class="sxs-lookup"><span data-stu-id="02206-104">When you use dynamic endpoints, the run-time libraries obtain endpoint information as they need it.</span></span> <span data-ttu-id="02206-105">As bibliotecas de tempo de execução fazem a distinção entre um *identificador totalmente associado* (um que inclui informações de ponto de extremidade) e um *identificador parcialmente associado* (um que não inclui informações de ponto de extremidade).</span><span class="sxs-lookup"><span data-stu-id="02206-105">The run-time libraries make the distinction between a *fully bound handle* (one that includes endpoint information) and a *partially bound handle* (one that does not include endpoint information).</span></span>

<span data-ttu-id="02206-106">A biblioteca de tempo de execução do cliente deve converter o identificador parcialmente associado em um identificador totalmente associado antes que o cliente possa se associar ao servidor.</span><span class="sxs-lookup"><span data-stu-id="02206-106">The client run-time library must convert the partially bound handle to a fully bound handle before the client can bind to the server.</span></span> <span data-ttu-id="02206-107">A biblioteca de tempo de execução do cliente tenta converter o identificador de associação parcial para o aplicativo cliente obtendo as informações do ponto de extremidade conforme mostrado:</span><span class="sxs-lookup"><span data-stu-id="02206-107">The client run-time library tries to convert the partially bound handle for the client application by obtaining the endpoint information as shown:</span></span>

-   <span data-ttu-id="02206-108">Da especificação da interface do cliente</span><span class="sxs-lookup"><span data-stu-id="02206-108">From the client's interface specification</span></span>
-   <span data-ttu-id="02206-109">De um serviço de mapeamento de ponto de extremidade em execução no servidor</span><span class="sxs-lookup"><span data-stu-id="02206-109">From an endpoint-mapping service running on the server</span></span>

<span data-ttu-id="02206-110">Se o cliente tentar usar um identificador parcialmente associado quando as informações do ponto de extremidade não estiverem disponíveis na especificação de interface e o mapeador de ponto de extremidade do servidor não tiver informações sobre o ponto de extremidade do servidor, o cliente não terá informações suficientes para fazer sua chamada de procedimento remoto e essa chamada falhará.</span><span class="sxs-lookup"><span data-stu-id="02206-110">If the client tries to use a partially bound handle when the endpoint information is not available in the interface specification and the server's endpoint-mapper does not have information about the server endpoint, the client will not have enough information to make its remote procedure call and that call will fail.</span></span> <span data-ttu-id="02206-111">Para evitar isso, você deve registrar o ponto de extremidade no mapeador de ponto de extremidade quando seu aplicativo distribuído usa identificadores parcialmente associados.</span><span class="sxs-lookup"><span data-stu-id="02206-111">To prevent this, you must register the endpoint in the endpoint mapper when your distributed application uses partially bound handles.</span></span> <span data-ttu-id="02206-112">Para obter mais informações sobre o mapeador de ponto de extremidade, consulte [especificando pontos de extremidades dinâmicos](specifying-endpoints.md).</span><span class="sxs-lookup"><span data-stu-id="02206-112">For more information about the endpoint mapper, see [Specifying Dynamic Endpoints](specifying-endpoints.md).</span></span>

<span data-ttu-id="02206-113">Quando uma chamada de procedimento remoto falha, o aplicativo cliente pode chamar [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset) para remover informações de ponto de extremidade desatualizadas.</span><span class="sxs-lookup"><span data-stu-id="02206-113">When a remote procedure call fails, the client application can call [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset) to remove out-of-date endpoint information.</span></span> <span data-ttu-id="02206-114">Quando o cliente tenta chamar o procedimento remoto, a biblioteca de tempo de execução do cliente tenta novamente converter o identificador totalmente associado em um identificador parcialmente associado.</span><span class="sxs-lookup"><span data-stu-id="02206-114">When the client tries to call the remote procedure, the client run-time library again tries to convert the fully bound handle to a partially bound handle.</span></span> <span data-ttu-id="02206-115">Isso é útil quando o servidor foi interrompido e reiniciado usando um ponto de extremidade dinâmico diferente.</span><span class="sxs-lookup"><span data-stu-id="02206-115">This is useful when the server has been stopped and restarted using a different dynamic endpoint.</span></span>

 

 




