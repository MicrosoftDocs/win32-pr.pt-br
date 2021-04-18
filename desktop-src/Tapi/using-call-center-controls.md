---
description: Os controles do Call Center estendem o modelo de objeto TAPI 3 para dar suporte aos requisitos de sistemas AD (distribuição de chamada automática).
ms.assetid: cb7a4231-6249-4ab9-9de7-243768a18775
title: Usando controles do Call Center
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdc01cac4b068c5ec17ff5794e2e7ffff46dbf95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760322"
---
# <a name="using-call-center-controls"></a><span data-ttu-id="f4b51-103">Usando controles do Call Center</span><span class="sxs-lookup"><span data-stu-id="f4b51-103">Using Call Center Controls</span></span>

<span data-ttu-id="f4b51-104">Os controles do Call Center estendem o modelo de objeto TAPI 3 para dar suporte aos requisitos de sistemas AD (distribuição de chamada automática).</span><span class="sxs-lookup"><span data-stu-id="f4b51-104">Call center controls extend the TAPI 3 object model to support the requirements of Automatic Call Distribution (ACD) systems.</span></span> <span data-ttu-id="f4b51-105">Uma central de atendimento é um local com agentes ou operadores em bancos de telefones, fazendo chamadas telefônicas de saída ou campos de entrada.</span><span class="sxs-lookup"><span data-stu-id="f4b51-105">A call center is a location with agents or operators at banks of telephones either making outgoing telephone calls or fielding incoming ones.</span></span> <span data-ttu-id="f4b51-106">Por exemplo, um banco ou uma empresa de cartão de crédito usará um Call Center para processar consultas de conta.</span><span class="sxs-lookup"><span data-stu-id="f4b51-106">For example, a bank or credit card company will use a call center to process account inquiries.</span></span>

<span data-ttu-id="f4b51-107">Os aplicativos de Call Center são divididos em três tipos básicos:</span><span class="sxs-lookup"><span data-stu-id="f4b51-107">Call center applications are divided into three basic types:</span></span>

-   <span data-ttu-id="f4b51-108">[Proxy ad](acd-proxy.md): trata as sessões de entrada ou saída no servidor, que podem ser qualquer coisa de um comutador telefônico proprietário para um gateway de Internet.</span><span class="sxs-lookup"><span data-stu-id="f4b51-108">[ACD Proxy](acd-proxy.md): Handles incoming or outgoing sessions at the server, which can be anything from a proprietary telephone switch to an Internet gateway.</span></span>
-   <span data-ttu-id="f4b51-109">[Cliente do agente do AD](acd-agent-client.md): serviços um agente individual que está recebendo ou fazendo chamadas.</span><span class="sxs-lookup"><span data-stu-id="f4b51-109">[ACD Agent Client](acd-agent-client.md): Services an individual agent who is receiving or making calls.</span></span>
-   <span data-ttu-id="f4b51-110">Cliente do supervisor do AD: fornece uma visão geral das operações do agente e do AD.</span><span class="sxs-lookup"><span data-stu-id="f4b51-110">ACD Supervisor Client: Provides an overall view of agent and ACD operations.</span></span>

> [!Note]  
> <span data-ttu-id="f4b51-111">Para o Windows 2000, a funcionalidade de proxy está disponível usando a TAPI 2,2, e as funções de supervisor não são implementadas.</span><span class="sxs-lookup"><span data-stu-id="f4b51-111">For Windows 2000, proxy functionality is available using TAPI 2.2, and supervisor functions are not implemented.</span></span>

 

<span data-ttu-id="f4b51-112">A seção de exemplos do SDK do Windows contém exemplos de código AD em Netds \\ TAPI \\ Tapi2 \\ AD e Netds \\ TAPI \\ Tapi3 \\ AD.</span><span class="sxs-lookup"><span data-stu-id="f4b51-112">The samples section of the Windows SDK contains ACD code samples under Netds\\Tapi\\Tapi2\\Acd and Netds\\Tapi\\Tapi3\\Acd.</span></span>

 

 



