---
description: Geralmente considerado mais amigável de rede do que uma difusão de todas as rotas, uma difusão direcionada limita-se à rede local que você especificar.
ms.assetid: e2358580-5a65-434d-ba4c-a6b0615bccc3
title: Difusão direcionada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f3a47bd47e9800e1f9c93cffa555b76feb77373
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810916"
---
# <a name="directed-broadcast"></a><span data-ttu-id="62af7-103">Difusão direcionada</span><span class="sxs-lookup"><span data-stu-id="62af7-103">Directed Broadcast</span></span>

<span data-ttu-id="62af7-104">Geralmente considerado mais amigável de rede do que uma difusão de todas as rotas, uma difusão direcionada limita-se à rede local que você especificar.</span><span class="sxs-lookup"><span data-stu-id="62af7-104">Generally considered more network friendly than an all-routes broadcast, a directed broadcast limits itself to the local network that you specify.</span></span> <span data-ttu-id="62af7-105">Preencha o **SA \_ netnum** com o número de rede de destino e o **\_ nodenum SA** com binários.</span><span class="sxs-lookup"><span data-stu-id="62af7-105">Fill **sa\_netnum** with the target network number and **sa\_nodenum** with binary ones.</span></span> <span data-ttu-id="62af7-106">Os roteadores encaminham essa solicitação para a rede de destino onde se torna uma difusão local.</span><span class="sxs-lookup"><span data-stu-id="62af7-106">Routers forward this request to the destination network where it becomes a local broadcast.</span></span> <span data-ttu-id="62af7-107">Redes intermediárias não veem este pacote como uma difusão.</span><span class="sxs-lookup"><span data-stu-id="62af7-107">Intermediate networks do not see this packet as a broadcast.</span></span>

 

 



