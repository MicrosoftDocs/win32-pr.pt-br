---
title: Limpeza da entrada do serviço de nome
description: Uma entrada de serviço de nome deve conter informações que não são alteradas com frequência.
ms.assetid: b581bc10-e537-4714-b89a-d998fec23360
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cf0ed6a21074a49a472d7505dcfea37cf182026
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005851"
---
# <a name="name-service-entry-cleanup"></a><span data-ttu-id="a5c9b-103">Limpeza da entrada do serviço de nome</span><span class="sxs-lookup"><span data-stu-id="a5c9b-103">Name Service Entry Cleanup</span></span>

<span data-ttu-id="a5c9b-104">Uma entrada de serviço de nome deve conter informações que não são alteradas com frequência.</span><span class="sxs-lookup"><span data-stu-id="a5c9b-104">A name service entry should contain information that does not change frequently.</span></span> <span data-ttu-id="a5c9b-105">Por esse motivo, não inclua pontos de extremidade dinâmicos em seus identificadores de associação exportados porque eles serão alterados em cada invocação do servidor e abrirão sua entrada de serviço de nome.</span><span class="sxs-lookup"><span data-stu-id="a5c9b-105">For this reason, do not include dynamic endpoints in your exported binding handles because they will change at each invocation of the server and will clutter up your name service entry.</span></span> <span data-ttu-id="a5c9b-106">Para remover esses identificadores de ligação, use [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset).</span><span class="sxs-lookup"><span data-stu-id="a5c9b-106">To remove these binding handles, use [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset).</span></span>

<span data-ttu-id="a5c9b-107">Por exemplo, uma sequência razoável de operações de servidor seria:</span><span class="sxs-lookup"><span data-stu-id="a5c9b-107">For example, a reasonable sequence of server operations would be:</span></span>

<span data-ttu-id="a5c9b-108">Para mais de um transporte:</span><span class="sxs-lookup"><span data-stu-id="a5c9b-108">For more than one transport:</span></span>

``` syntax
RpcServerUseProtseq();
RpcServerUseProtseq();
```

<span data-ttu-id="a5c9b-109">Para posicionar associações no mapeador de ponto de extremidade:</span><span class="sxs-lookup"><span data-stu-id="a5c9b-109">To place bindings in the endpoint mapper:</span></span>

``` syntax
RpcServerInqBindings(&Vector);
RpcEpRegister(Interface, Vector);
```

<span data-ttu-id="a5c9b-110">Para remover pontos de extremidade de associações:</span><span class="sxs-lookup"><span data-stu-id="a5c9b-110">To remove endpoints from bindings:</span></span>

``` syntax
for (i=0; i < Vector- > Count; + + i)
{
    RpcBindingReset(Vector->BindingH[i];
}
```

<span data-ttu-id="a5c9b-111">Para adicionar associações ao serviço de nome:</span><span class="sxs-lookup"><span data-stu-id="a5c9b-111">To add bindings to the name service:</span></span>

``` syntax
RpcNsBindingExport(RPC_C_NS_SYNTAX_DEFAULT, EntryName, Interface
                   Vector);
RpcServerListen();
```

 

 




