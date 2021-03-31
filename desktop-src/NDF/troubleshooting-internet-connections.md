---
title: Solucionando problemas de conexões com a Internet
description: Nesse cenário, um usuário está tentando navegar até www.msn.com usando o protocolo HTTPS, mas não consegue se conectar. Você pode usar o netsh e o Monitor de Rede para coletar e exibir rastreamentos a fim de ajudar a determinar por que a conexão falhou.
ms.assetid: e10fcc24-4670-461c-a145-3910c102e81f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 753636c1186243a96e3cef5a4ab73244556daec4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822516"
---
# <a name="troubleshooting-internet-connections"></a><span data-ttu-id="a1fc1-104">Solucionando problemas de conexões com a Internet</span><span class="sxs-lookup"><span data-stu-id="a1fc1-104">Troubleshooting Internet Connections</span></span>

<span data-ttu-id="a1fc1-105">Nesse cenário, um usuário está tentando navegar até www.msn.com usando o protocolo HTTPS, mas não consegue se conectar.</span><span class="sxs-lookup"><span data-stu-id="a1fc1-105">In this scenario, a user is attempting to browse to www.msn.com using the https protocol, but is unable to connect.</span></span> <span data-ttu-id="a1fc1-106">Você pode usar o netsh e o Monitor de Rede para coletar e exibir rastreamentos a fim de ajudar a determinar por que a conexão falhou.</span><span class="sxs-lookup"><span data-stu-id="a1fc1-106">You can use Netsh and Network Monitor to collect and view traces in order to help determine why the connection failed.</span></span>

<span data-ttu-id="a1fc1-107">Primeiro, você pode usar o netsh para iniciar um rastreamento.</span><span class="sxs-lookup"><span data-stu-id="a1fc1-107">First, you can use netsh to start a trace.</span></span> <span data-ttu-id="a1fc1-108">Digitando **netsh trace iniciar cenário = InternetClient TraceFile = MSN. etl** inicia o rastreamento para todos os provedores habilitados no cenário InternetClient, salvando os resultados em um arquivo chamado MSN. etl.</span><span class="sxs-lookup"><span data-stu-id="a1fc1-108">Typing **netsh trace start scenario = InternetClient tracefile=msn.etl** starts tracing for all of the providers enabled under the InternetClient scenario, saving the results to a file named msn.etl.</span></span> <span data-ttu-id="a1fc1-109">Depois de usar um navegador da Web para tentar acessar o www.msn.com, digitar **netsh trace stop** termina e correlaciona o arquivo de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="a1fc1-109">After using a web browser to attempt to reach www.msn.com, typing **netsh trace stop** terminates and correlates the trace file.</span></span>

<span data-ttu-id="a1fc1-110">Em seguida, você pode abrir o arquivo MSN. etl em Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="a1fc1-110">You can then open the msn.etl file in Network Monitor.</span></span> <span data-ttu-id="a1fc1-111">Os eventos são agrupados por ID de atividade no painel esquerdo.</span><span class="sxs-lookup"><span data-stu-id="a1fc1-111">The events are grouped by activity ID in the left pane.</span></span> <span data-ttu-id="a1fc1-112">Usando a descrição do filtro **. Contains ("MSN")** mostrará somente os eventos que incluem a cadeia de caracteres "MSN" em sua descrição de protocolo.</span><span class="sxs-lookup"><span data-stu-id="a1fc1-112">Using the filter **description.contains("msn")** will show only those events which include the string "msn" in their protocol description.</span></span>

![Solucionando problemas de conexões de Internet usando o monitor de rede (1)](images/internetclient1.png)

<span data-ttu-id="a1fc1-114">Em seguida, você pode examinar os eventos no resumo do quadro para identificar um evento que é relevante.</span><span class="sxs-lookup"><span data-stu-id="a1fc1-114">Next, you can review the events in the frame summary to identify an event which looks relevant.</span></span> <span data-ttu-id="a1fc1-115">Depois de selecionar o evento, clique com o botão direito do mouse e aponte para localizar conversas e clique em UTEvent para selecionar a conversa no nível de UTEvent.</span><span class="sxs-lookup"><span data-stu-id="a1fc1-115">After you select the event, right-click and point to Find Conversations, then click UTEvent to select the conversation at the UTEvent level.</span></span>

![Solucionando problemas de conexões de Internet usando o monitor de rede (2)](images/internetclient2.png)

<span data-ttu-id="a1fc1-117">A atividade normalizada associada no painel esquerdo é realçada, nesse caso, UTEvent ActivityId 397.</span><span class="sxs-lookup"><span data-stu-id="a1fc1-117">The associated normalized activity in the left pane is then highlighted, in this case UTEvent ActivityID 397.</span></span>

![Solucionando problemas de conexões de Internet usando o monitor de rede (3)](images/internetclient3.png)

<span data-ttu-id="a1fc1-119">Usando Monitor de Rede para exibir e filtrar as informações de rastreamento, o número de eventos a serem examinados foi reduzido de 1989 para 96.</span><span class="sxs-lookup"><span data-stu-id="a1fc1-119">By using Network Monitor to view and filter the trace information, the number of events to examine has been reduced from 1989 to 96.</span></span>

 

 




