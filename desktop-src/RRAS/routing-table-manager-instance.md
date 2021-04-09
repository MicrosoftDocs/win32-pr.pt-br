---
title: Instância do Gerenciador de tabela de roteamento
description: Uma instância é uma tabela separada que o Gerenciador de tabela de roteamento usa para manter informações de roteamento sobre um subconjunto de interfaces.
ms.assetid: a17233fc-2c40-4d00-8a6b-86f08fef5690
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d209f254bb9111c786bde6635b43895604785d5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005420"
---
# <a name="routing-table-manager-instance"></a><span data-ttu-id="da02c-103">Instância do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="da02c-103">Routing Table Manager Instance</span></span>

<span data-ttu-id="da02c-104">Uma instância é uma tabela separada que o Gerenciador de tabela de roteamento usa para manter informações de roteamento sobre um subconjunto de interfaces.</span><span class="sxs-lookup"><span data-stu-id="da02c-104">An instance is a separate table that the routing table manager uses to maintain routing information about a subset of interfaces.</span></span> <span data-ttu-id="da02c-105">Normalmente, as instâncias são usadas para permitir que um roteador físico atue como um conjunto de roteadores virtuais – um roteador virtual por rede lógica.</span><span class="sxs-lookup"><span data-stu-id="da02c-105">Instances are typically used to enable a physical router to act as a set of virtual routers – one virtual router per logical network.</span></span>

<span data-ttu-id="da02c-106">Atualmente, o Gerenciador de tabela de roteamento dá suporte a apenas uma instância (identificada como zero, o padrão).</span><span class="sxs-lookup"><span data-stu-id="da02c-106">Currently, the routing table manager supports only one instance (identified as zero, the default).</span></span> <span data-ttu-id="da02c-107">O cliente pode se registrar em outras instâncias, mas nenhum roteador virtual, exceto o padrão, é reconhecido ou usado pelo Gerenciador de roteador.</span><span class="sxs-lookup"><span data-stu-id="da02c-107">The client can register with other instances, but no virtual router except the default one is recognized or used by the router manager.</span></span>

 

 




