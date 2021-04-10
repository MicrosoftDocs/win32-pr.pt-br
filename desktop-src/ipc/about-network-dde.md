---
description: O DDE de rede é usado para iniciar e manter as conexões de rede necessárias para conversas DDE entre aplicativos em execução em computadores diferentes em uma rede.
ms.assetid: f9eee391-2b4a-4c17-bea5-72cda5124e1c
title: Sobre o DDE de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 412971f6bef8d2782dce38b5aef413e4d073f6b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296666"
---
# <a name="about-network-dde"></a><span data-ttu-id="6917b-103">Sobre o DDE de rede</span><span class="sxs-lookup"><span data-stu-id="6917b-103">About Network DDE</span></span>

<span data-ttu-id="6917b-104">\[Não há mais suporte para DDE de rede.</span><span class="sxs-lookup"><span data-stu-id="6917b-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="6917b-105">Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ não \_ implementado.\]</span><span class="sxs-lookup"><span data-stu-id="6917b-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="6917b-106">O DDE de rede é usado para iniciar e manter as conexões de rede necessárias para conversas DDE entre aplicativos em execução em computadores diferentes em uma rede.</span><span class="sxs-lookup"><span data-stu-id="6917b-106">Network DDE is used to initiate and maintain the network connections needed for DDE conversations between applications running on different computers in a network.</span></span> <span data-ttu-id="6917b-107">Uma *conversa* DDE é a interação entre aplicativos cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="6917b-107">A DDE *conversation* is the interaction between client and server applications.</span></span> <span data-ttu-id="6917b-108">Você usa o DDE de rede junto com o DDE e a DDEML (biblioteca de gerenciamento de DDE) em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6917b-108">You use network DDE along with DDE and the DDE management library (DDEML) in your application.</span></span>

<span data-ttu-id="6917b-109">O DDE é uma forma de comunicação entre processos que usa memória compartilhada para trocar dados entre aplicativos.</span><span class="sxs-lookup"><span data-stu-id="6917b-109">DDE is a form of interprocess communication that uses shared memory to exchange data between applications.</span></span> <span data-ttu-id="6917b-110">Os aplicativos podem usar o DDE para transferências de dados de uma vez ou para trocas contínuas e atualizar dados.</span><span class="sxs-lookup"><span data-stu-id="6917b-110">Applications can use DDE for one time data transfers or for ongoing exchanges and updating data.</span></span> <span data-ttu-id="6917b-111">Para obter mais informações sobre o DDE, consulte [troca dinâmica de dados](../dataxchg/dynamic-data-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="6917b-111">For more information on DDE, see [Dynamic Data Exchange](../dataxchg/dynamic-data-exchange.md).</span></span>

<span data-ttu-id="6917b-112">O DDEML simplifica a tarefa de adicionar capacidade de DDE a um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6917b-112">DDEML simplifies the task of adding DDE capability to an application.</span></span> <span data-ttu-id="6917b-113">Em vez de enviar, postar e processar mensagens DDE diretamente, um aplicativo usa as funções fornecidas pelo DDEML para gerenciar conversas DDE.</span><span class="sxs-lookup"><span data-stu-id="6917b-113">Instead of sending, posting, and processing DDE messages directly, an application uses the functions provided by the DDEML to manage DDE conversations.</span></span> <span data-ttu-id="6917b-114">Para obter mais informações sobre DDEML, consulte [troca dinâmica de dados biblioteca de gerenciamento](../dataxchg/dynamic-data-exchange-management-library.md).</span><span class="sxs-lookup"><span data-stu-id="6917b-114">For more information on DDEML, see [Dynamic Data Exchange Management Library](../dataxchg/dynamic-data-exchange-management-library.md).</span></span>

## <a name="network-dde-files"></a><span data-ttu-id="6917b-115">Arquivos DDE de rede</span><span class="sxs-lookup"><span data-stu-id="6917b-115">Network DDE Files</span></span>

<span data-ttu-id="6917b-116">Para usar os elementos de API do DDE de rede, você deve incluir o arquivo de cabeçalho NDDEApi. h em seus arquivos de origem e incluir o arquivo NDDEApi. lib na linha de link.</span><span class="sxs-lookup"><span data-stu-id="6917b-116">To use the API elements of network DDE, you must include the NDDEApi.h header file in your source files and include NDDEApi.lib file on your link line.</span></span> <span data-ttu-id="6917b-117">Você também deve verificar se o arquivo de NDDEApi.dll está carregado.</span><span class="sxs-lookup"><span data-stu-id="6917b-117">You must also make sure that the NDDEApi.dll file is loaded.</span></span>

<span data-ttu-id="6917b-118">Para mais informações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="6917b-118">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="6917b-119">Agente DDE de rede</span><span class="sxs-lookup"><span data-stu-id="6917b-119">Network DDE Agent</span></span>](network-dde-agent.md)
-   [<span data-ttu-id="6917b-120">Compartilhamentos DDE</span><span class="sxs-lookup"><span data-stu-id="6917b-120">DDE Shares</span></span>](dde-shares.md)
-   [<span data-ttu-id="6917b-121">Compartilhamentos e segurança confiáveis</span><span class="sxs-lookup"><span data-stu-id="6917b-121">Trusted Shares and Security</span></span>](trusted-shares-and-security.md)
-   [<span data-ttu-id="6917b-122">Gerenciando compartilhamentos DDE</span><span class="sxs-lookup"><span data-stu-id="6917b-122">Managing DDE Shares</span></span>](managing-dde-shares.md)

 

 
