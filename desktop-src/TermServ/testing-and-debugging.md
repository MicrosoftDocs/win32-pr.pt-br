---
title: Teste e depuração
description: Há um \ 0034; Echo \ 0034; ouvinte que é implementado pelo cliente de Conexão de Área de Trabalho Remota (RDC), que está sempre presente e escutando conexões de entrada.
ms.assetid: ae14af04-7d19-406b-998e-a0579cfe73eb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9028ccf0eea97a8651392baba094ac6dcda242f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105754163"
---
# <a name="testing-and-debugging"></a><span data-ttu-id="28f44-103">Teste e depuração</span><span class="sxs-lookup"><span data-stu-id="28f44-103">Testing and Debugging</span></span>

<span data-ttu-id="28f44-104">Há um ouvinte de "eco" que é implementado pelo cliente de Conexão de Área de Trabalho Remota (RDC), que está sempre presente e escutando conexões de entrada.</span><span class="sxs-lookup"><span data-stu-id="28f44-104">There is an "echo" listener that is implemented by the Remote Desktop Connection (RDC) client, which is always present and listening for incoming connections.</span></span> <span data-ttu-id="28f44-105">Ao gravar o lado do servidor de um módulo de canal virtual dinâmico (DVC), como um teste rápido, você pode abrir um ponto de extremidade chamado "ECHO".</span><span class="sxs-lookup"><span data-stu-id="28f44-105">When you are writing the server side of a dynamic virtual channel (DVC) module, as a quick test you can open an endpoint named "ECHO".</span></span> <span data-ttu-id="28f44-106">Qualquer gravação em um canal que é instanciado desse ponto de extremidade resultará no recebimento dos mesmos dados.</span><span class="sxs-lookup"><span data-stu-id="28f44-106">Any write to a channel that is instantiated from this endpoint will result in the receipt of the same data.</span></span>

<span data-ttu-id="28f44-107">Você pode usar essa técnica para testar uma implementação de e/s (entrada/saída) do módulo do lado do servidor, para medir o tempo de resposta para um plug-in de cliente Conexão de Área de Trabalho Remota (RDC) ou para medir o atraso de rede para o cliente Conexão de Área de Trabalho Remota (RDC).</span><span class="sxs-lookup"><span data-stu-id="28f44-107">You can use this technique to test an input/output (I/O) implementation of the server-side module, to measure the response time for a Remote Desktop Connection (RDC) client plug-in, or to measure the network delay for the Remote Desktop Connection (RDC) client.</span></span> <span data-ttu-id="28f44-108">Não há nenhuma limitação na quantidade de dados que podem ser enviados por esse canal.</span><span class="sxs-lookup"><span data-stu-id="28f44-108">There is no limitation on the amount of data that can be sent over this channel.</span></span>

 

 




