---
title: Mantendo o estado no servidor entre as chamadas
description: Geralmente, é necessário manter o estado no servidor entre chamadas RPC separadas \ 8212; usar identificadores de contexto é a melhor maneira de fazer isso. Algumas palavras sobre como os identificadores de contexto operam internamente ajudam a entender quando os identificadores de contexto funcionam melhor.
ms.assetid: f76ec489-f48e-473d-b519-3ac143d41fa4
keywords:
- RPC de chamada de procedimento remoto, práticas recomendadas, manutenção do estado entre chamadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00090fb317cba8c33e7b60ac81762d7d21dd4dc9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634797"
---
# <a name="maintaining-state-on-the-server-between-calls"></a><span data-ttu-id="7bfce-105">Mantendo o estado no servidor entre as chamadas</span><span class="sxs-lookup"><span data-stu-id="7bfce-105">Maintaining State on the Server Between Calls</span></span>

<span data-ttu-id="7bfce-106">Geralmente, é necessário manter o estado no servidor entre chamadas RPC separadas — o uso de identificadores de contexto é a melhor maneira de fazer isso.</span><span class="sxs-lookup"><span data-stu-id="7bfce-106">It is often necessary to maintain state on the server between separate RPC calls—using context handles is the best way to do so.</span></span> <span data-ttu-id="7bfce-107">Algumas palavras sobre como os identificadores de contexto operam internamente ajudam a entender quando os identificadores de contexto funcionam melhor.</span><span class="sxs-lookup"><span data-stu-id="7bfce-107">A few words about how context handles operate internally helps in understanding when context handles work best.</span></span>

<span data-ttu-id="7bfce-108">O cliente nunca recebe o estado mantido no servidor.</span><span class="sxs-lookup"><span data-stu-id="7bfce-108">The client never receives the state kept on the server.</span></span> <span data-ttu-id="7bfce-109">Geralmente, o estado no servidor é um ponteiro para um bloco de memória e o cliente não tem informações sobre ele.</span><span class="sxs-lookup"><span data-stu-id="7bfce-109">Most often the state on the server is a pointer to a memory block, and the client has no information about it.</span></span> <span data-ttu-id="7bfce-110">Tudo o que o cliente recebe é um grande número exclusivo, com outras informações associadas a ele, que o servidor envia para o cliente e que representa o identificador de contexto em todas as operações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="7bfce-110">All the client receives is a large unique number, with other information associated with it, that the server sends to the client and which represents the context handle in all subsequent operations.</span></span> <span data-ttu-id="7bfce-111">Sempre que o cliente se refere a um identificador aberto, ele envia o grande número recebido do servidor quando esse identificador de contexto foi aberto.</span><span class="sxs-lookup"><span data-stu-id="7bfce-111">Whenever the client refers to an opened handle, it sends the large number it received from the server when that context handle was opened.</span></span>

<span data-ttu-id="7bfce-112">O servidor mantém o controle de todos os grandes números que envia a um cliente.</span><span class="sxs-lookup"><span data-stu-id="7bfce-112">The server keeps track of all large numbers it sends to a client.</span></span> <span data-ttu-id="7bfce-113">Quando o servidor recebe um grande número que representa um identificador de contexto, ele pesquisa o número na coleção de identificadores de contexto válidos e pendentes para esse cliente e localiza o contexto do lado do servidor correspondente a um determinado número grande.</span><span class="sxs-lookup"><span data-stu-id="7bfce-113">When the server receives a large number representing a context handle, it looks up the number in the collection of valid, outstanding context handles for that client, and finds the server-side context corresponding to a given large number.</span></span> <span data-ttu-id="7bfce-114">Isso é passado para a rotina do servidor.</span><span class="sxs-lookup"><span data-stu-id="7bfce-114">This is passed to the server routine.</span></span> <span data-ttu-id="7bfce-115">Se o número grande não for encontrado, uma \_ exceção de \_ incompatibilidade de contexto X SS de RPC \_ \_ será gerada e propagada para o cliente.</span><span class="sxs-lookup"><span data-stu-id="7bfce-115">If the large number is not found, an RPC\_X\_SS\_CONTEXT\_MISMATCH exception is raised and propagated to the client.</span></span>

<span data-ttu-id="7bfce-116">Os coregistros desse design são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="7bfce-116">The corollaries of this design are as follows:</span></span>

-   <span data-ttu-id="7bfce-117">Um identificador de contexto é válido somente no contexto da sessão de cliente/servidor existente.</span><span class="sxs-lookup"><span data-stu-id="7bfce-117">A context handle is valid only in the context of the existing client/server session.</span></span> <span data-ttu-id="7bfce-118">Ele não pode ser passado para outro cliente.</span><span class="sxs-lookup"><span data-stu-id="7bfce-118">It cannot be passed to another client.</span></span>
-   <span data-ttu-id="7bfce-119">Um identificador de contexto torna-se inválido se o servidor for reinicializado ou perder sua conexão com o cliente.</span><span class="sxs-lookup"><span data-stu-id="7bfce-119">A context handle becomes invalid if the server is rebooted, or otherwise loses its connection to the client.</span></span>
-   <span data-ttu-id="7bfce-120">O cliente não pode interpretar o que o identificador de contexto representa no servidor.</span><span class="sxs-lookup"><span data-stu-id="7bfce-120">The client cannot interpret what the context handle represents on the server.</span></span> <span data-ttu-id="7bfce-121">Para um cliente, todos os identificadores de contexto são simplesmente números grandes.</span><span class="sxs-lookup"><span data-stu-id="7bfce-121">To a client, all context handles are simply large numbers.</span></span>

<span data-ttu-id="7bfce-122">Se o cliente falhar, o servidor receberá uma notificação e limpará seus identificadores de contexto usando o mecanismo de execução.</span><span class="sxs-lookup"><span data-stu-id="7bfce-122">If the client fails, the server will get a notification and will clean up its context handles using the run-down mechanism.</span></span>

 

 




