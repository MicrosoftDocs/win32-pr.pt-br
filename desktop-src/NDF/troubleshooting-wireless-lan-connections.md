---
title: Solucionando problemas de conexões de LAN sem fio
description: Nesse cenário, um usuário está tentando se conectar a uma LAN sem fio, mas não consegue se conectar. Você pode usar o netsh e o Monitor de Rede para coletar e exibir rastreamentos a fim de ajudar a determinar por que a conexão falhou.
ms.assetid: 558dae83-aa16-4751-a497-d7a0da01ce5d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55878afcee0091634415d4dbc465d1b143f46057
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005991"
---
# <a name="troubleshooting-wireless-lan-connections"></a><span data-ttu-id="ebb6a-104">Solucionando problemas de conexões de LAN sem fio</span><span class="sxs-lookup"><span data-stu-id="ebb6a-104">Troubleshooting Wireless LAN Connections</span></span>

<span data-ttu-id="ebb6a-105">Nesse cenário, um usuário está tentando se conectar a uma LAN sem fio, mas não consegue se conectar.</span><span class="sxs-lookup"><span data-stu-id="ebb6a-105">In this scenario, a user is attempting to connect to a wireless LAN, but is unable to connect.</span></span> <span data-ttu-id="ebb6a-106">Você pode usar o netsh e o Monitor de Rede para coletar e exibir rastreamentos a fim de ajudar a determinar por que a conexão falhou.</span><span class="sxs-lookup"><span data-stu-id="ebb6a-106">You can use Netsh and Network Monitor to collect and view traces in order to help determine why the connection failed.</span></span>

<span data-ttu-id="ebb6a-107">Primeiro, você pode usar o netsh para iniciar um rastreamento.</span><span class="sxs-lookup"><span data-stu-id="ebb6a-107">First, you can use netsh to start a trace.</span></span> <span data-ttu-id="ebb6a-108">Digitando **netsh trace iniciar cenário = WLAN TraceFile = wlanwpp. etl** inicia o rastreamento para todos os provedores habilitados no cenário de WLAN, salvando os resultados em um arquivo chamado wlanwpp. etl.</span><span class="sxs-lookup"><span data-stu-id="ebb6a-108">Typing **netsh trace start scenario = wlan tracefile=wlanwpp.etl** starts tracing for all of the providers enabled under the WLAN scenario, saving the results to a file named wlanwpp.etl.</span></span> <span data-ttu-id="ebb6a-109">Depois de tentar se conectar à LAN sem fio, digitar **netsh trace stop** terminará e correlacionará o arquivo de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="ebb6a-109">After attempting to connect to the wireless LAN, typing **netsh trace stop** terminates and correlates the trace file.</span></span>

<span data-ttu-id="ebb6a-110">Em seguida, você pode abrir o arquivo wlanwpp. etl em Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="ebb6a-110">You can then open the wlanwpp.etl file in Network Monitor.</span></span> <span data-ttu-id="ebb6a-111">Os eventos são agrupados por ID de atividade no painel esquerdo.</span><span class="sxs-lookup"><span data-stu-id="ebb6a-111">The events are grouped by activity ID in the left pane.</span></span>

![Solucionando problemas de conexões LAN sem fio usando o monitor de rede (1)](images/1wlan.png)

<span data-ttu-id="ebb6a-113">O ETL contém muitos rastreamentos de outros provedores de rede que estão habilitados.</span><span class="sxs-lookup"><span data-stu-id="ebb6a-113">The ETL contains lot of traces from other network providers that are enabled.</span></span> <span data-ttu-id="ebb6a-114">Você pode aplicar um filtro para exibir somente os eventos que são relevantes para o provedor de **\_ MicrosoftWindowsWlanAutoConfig de WLAN** .</span><span class="sxs-lookup"><span data-stu-id="ebb6a-114">You can apply a filter to display only those events which are relevant to the **WLAN\_MicrosoftWindowsWlanAutoConfig** provider.</span></span>

![Solucionando problemas de conexões LAN sem fio usando o monitor de rede (2)](images/2wlan.png)

<span data-ttu-id="ebb6a-116">Depois que o filtro tiver sido aplicado, você poderá examinar os eventos no resumo do quadro para identificar um evento que pareça relevante.</span><span class="sxs-lookup"><span data-stu-id="ebb6a-116">After the filter has been applied, you can review the events in the frame summary to identify an event which looks relevant.</span></span> <span data-ttu-id="ebb6a-117">Depois de selecionar o evento, clique com o botão direito do mouse e aponte para localizar conversas e clique em netevent.</span><span class="sxs-lookup"><span data-stu-id="ebb6a-117">After you select the event, right-click and point to Find Conversations, then click NetEvent.</span></span>

![Solucionando problemas de conexões LAN sem fio usando o monitor de rede (3)](images/3wlan.png)

<span data-ttu-id="ebb6a-119">Expandir os itens em uma ID de atividade no painel esquerdo permitirá que você exiba todos os outros provedores relevantes para a tentativa de conexão.</span><span class="sxs-lookup"><span data-stu-id="ebb6a-119">Expanding the items under an activity ID in the left pane will allow you to view all of the other relevant providers for the connection attempt.</span></span> <span data-ttu-id="ebb6a-120">Para exibir os eventos de outros provedores, todos os filtros são removidos clicando em **remover** no painel **filtro de exibição** .</span><span class="sxs-lookup"><span data-stu-id="ebb6a-120">To view the events from other providers, all filters are removed by clicking **Remove** in the **Display Filter** pane.</span></span> <span data-ttu-id="ebb6a-121">Os rastreamentos podem ser analisados rolando o resumo do quadro, selecionando eventos adicionais conforme necessário para coletar mais informações.</span><span class="sxs-lookup"><span data-stu-id="ebb6a-121">The traces can be analyzed by scrolling through the frame summary, selecting additional events as needed to gather more information.</span></span> <span data-ttu-id="ebb6a-122">Nesse caso, o painel detalhes do quadro fornece informações de que a falha ocorre devido a uma falha de troca de chave, provavelmente devido ao usuário entrando na chave de passagem incorreta.</span><span class="sxs-lookup"><span data-stu-id="ebb6a-122">In this case, the Frame Details pane provides information that the failure is due to key exchange failure, most likely due to the user entering the wrong pass key.</span></span>

 

 




