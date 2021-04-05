---
title: Quão seguro é o meu servidor RPC agora
description: Seguir a segurança descrita nesta seção, fornecida em outro lugar no SDK do RPC e geralmente aceita como práticas de segurança adequadas, resultará em um servidor muito seguro. Esses servidores são protegidos contra ataques de penetração ou violações de privacidade.
ms.assetid: 528ff35c-f37c-43d8-8cc1-dbc36a9a826c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34279e4fb8899db6b7e980a0e868e91c6edb8166
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916323"
---
# <a name="how-secure-is-my-rpc-server-now"></a><span data-ttu-id="6560d-104">Qual a segurança do meu servidor RPC agora?</span><span class="sxs-lookup"><span data-stu-id="6560d-104">How Secure is My RPC Server Now?</span></span>

<span data-ttu-id="6560d-105">Seguir a segurança descrita nesta seção, fornecida em outro lugar no SDK do RPC e geralmente aceita como práticas de segurança adequadas, resultará em um servidor muito seguro.</span><span class="sxs-lookup"><span data-stu-id="6560d-105">Following the security outlined in this section, provided elsewhere in the RPC SDK, and generally accepted as proper security practices, will result in a server that is very secure.</span></span> <span data-ttu-id="6560d-106">Esses servidores são protegidos contra ataques de penetração ou violações de privacidade.</span><span class="sxs-lookup"><span data-stu-id="6560d-106">Such servers are protected from penetration attacks or privacy breaches.</span></span>

<span data-ttu-id="6560d-107">Se o estado for mantido entre chamadas RPC, verifique se um único cliente não causa a alocação de recursos excessivos, o que pode negar o serviço a outros clientes.</span><span class="sxs-lookup"><span data-stu-id="6560d-107">If state is kept between RPC calls, make sure a single client does not cause the allocation of excessive resources, which could potentially deny service to other clients.</span></span>

 

 




