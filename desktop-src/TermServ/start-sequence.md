---
title: Iniciar sequência
description: Etapas para iniciar o protocolo personalizado.
ms.assetid: 34c6eb08-668b-43b7-b49b-9ab7536ab658
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5af0716e39d1df96bbdf29f4a3abbb14e32bc752
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159403"
---
# <a name="start-sequence"></a><span data-ttu-id="28c70-103">Iniciar sequência</span><span class="sxs-lookup"><span data-stu-id="28c70-103">Start Sequence</span></span>

<span data-ttu-id="28c70-104">Para iniciar seu provedor de protocolo, o serviço de Serviços de Área de Trabalho Remota:</span><span class="sxs-lookup"><span data-stu-id="28c70-104">To start your protocol provider, the Remote Desktop Services service:</span></span>

-   <span data-ttu-id="28c70-105">Recupera o nome do ouvinte e o CLSID do seu objeto do Gerenciador de protocolos ([**IWRdsProtocolManager**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager)) do registro.</span><span class="sxs-lookup"><span data-stu-id="28c70-105">Retrieves the name of the listener and the CLSID of your protocol manager object ([**IWRdsProtocolManager**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager)) from the registry.</span></span> <span data-ttu-id="28c70-106">Para obter mais informações, consulte [registrando o Gerenciador de protocolos](registering-the-custom-protocol.md).</span><span class="sxs-lookup"><span data-stu-id="28c70-106">For more information, see [Registering the Protocol Manager](registering-the-custom-protocol.md).</span></span>
-   <span data-ttu-id="28c70-107">Chama [**Initialize**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-initialize) para inicializar o Gerenciador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="28c70-107">Calls [**Initialize**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-initialize) to initialize the protocol manager.</span></span>
-   <span data-ttu-id="28c70-108">Cria um objeto Gerenciador de protocolos usando o CLSID.</span><span class="sxs-lookup"><span data-stu-id="28c70-108">Creates a protocol manager object using the CLSID.</span></span> <span data-ttu-id="28c70-109">Mesmo se houver vários ouvintes registrados para o mesmo provedor de protocolo, o serviço criará apenas um objeto Gerenciador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="28c70-109">Even if there are multiple listeners registered for the same protocol provider, the service only creates one protocol manager object.</span></span>
-   <span data-ttu-id="28c70-110">Chama [**CreateListener**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) para instruir o objeto Gerenciador de protocolos a criar um objeto de ouvinte [**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener) e retorná-lo ao serviço.</span><span class="sxs-lookup"><span data-stu-id="28c70-110">Calls [**CreateListener**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) to instruct the protocol manager object to create an [**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener) listener object and return it to the service.</span></span> <span data-ttu-id="28c70-111">O objeto Gerenciador de protocolo deve adicionar uma referência ao objeto de ouvinte antes de retorná-lo para o serviço.</span><span class="sxs-lookup"><span data-stu-id="28c70-111">The protocol manager object must add a reference to the listener object before returning it to the service.</span></span> <span data-ttu-id="28c70-112">O serviço liberará o objeto quando o serviço for interrompido ou o ouvinte for excluído.</span><span class="sxs-lookup"><span data-stu-id="28c70-112">The service will release the object when the service stops or the listener is deleted.</span></span>
-   <span data-ttu-id="28c70-113">Chama [**StartListen**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-startlisten) no objeto de ouvinte para que o ouvinte possa começar a escutar conexões de entrada.</span><span class="sxs-lookup"><span data-stu-id="28c70-113">Calls [**StartListen**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-startlisten) on the listener object so that the listener can start listening for incoming connections.</span></span>
-   <span data-ttu-id="28c70-114">Chama [**StopListen**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-stoplisten) para interromper a escuta do objeto de ouvinte.</span><span class="sxs-lookup"><span data-stu-id="28c70-114">Calls [**StopListen**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-stoplisten) to stop the listener object from listening.</span></span>
-   <span data-ttu-id="28c70-115">Chama [**Uninitialize**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-uninitialize) para cancelar a inicialização do Gerenciador de protocolos.</span><span class="sxs-lookup"><span data-stu-id="28c70-115">Calls [**Uninitialize**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-uninitialize) to uninitialize the protocol manager.</span></span>

<span data-ttu-id="28c70-116">O ouvinte cria um objeto [**IWRdsProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection) quando um cliente tenta se conectar.</span><span class="sxs-lookup"><span data-stu-id="28c70-116">The listener creates an [**IWRdsProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection) object when a client tries to connect.</span></span> <span data-ttu-id="28c70-117">O objeto de ouvinte chama [**Onconnected**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistenercallback-onconnected) para notificar o serviço de serviços de área de trabalho remota que um novo cliente está tentando se conectar ou reconectar e passa o objeto **IWRdsProtocolConnection** nessa chamada.</span><span class="sxs-lookup"><span data-stu-id="28c70-117">The listener object calls [**OnConnected**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistenercallback-onconnected) to notify the Remote Desktop Services service that a new client is trying to connect or reconnect, and passes the **IWRdsProtocolConnection** object in that call.</span></span> <span data-ttu-id="28c70-118">O serviço de Serviços de Área de Trabalho Remota, por sua vez, retornará um objeto [**IWRdsProtocolConnectionCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback) nessa chamada para que o protocolo possa se comunicar com o serviço serviços de área de trabalho remota, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="28c70-118">The Remote Desktop Services service will in turn return an [**IWRdsProtocolConnectionCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback) object in that call so that the protocol can communicate with the Remote Desktop Services service as needed.</span></span> <span data-ttu-id="28c70-119">O serviço adiciona uma referência ao objeto de retorno de chamada antes de retornar, e o protocolo deve liberar essa referência quando a conexão for fechada.</span><span class="sxs-lookup"><span data-stu-id="28c70-119">The service adds a reference to the callback object before returning, and the protocol must release that reference when the connection closes.</span></span>

<span data-ttu-id="28c70-120">A ilustração a seguir mostra a interação entre os vários objetos durante a inicialização.</span><span class="sxs-lookup"><span data-stu-id="28c70-120">The following illustration shows the interaction between the various objects during startup.</span></span>

![RCM iniciar sequência](images/protocol-startsequence.png)

## <a name="related-topics"></a><span data-ttu-id="28c70-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="28c70-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28c70-123">Sequência de chamada de método</span><span class="sxs-lookup"><span data-stu-id="28c70-123">Method Call Sequence</span></span>](method-call-sequence.md)
</dt> <dt>

[<span data-ttu-id="28c70-124">Sequência de conexão</span><span class="sxs-lookup"><span data-stu-id="28c70-124">Connection Sequence</span></span>](connection-sequence.md)
</dt> </dl>

 

 




