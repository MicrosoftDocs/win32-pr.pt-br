---
description: Alguns aplicativos precisam receber a notificação de eventos de conexão, seja antes do evento, logo após a ocorrência, ou ambos. Você pode criar uma DLL para receber a notificação de adiantamento e após o fato dos eventos de conexão.
ms.assetid: 692eb8f2-1c53-4535-b44d-babb30eecd9c
title: Recebendo notificações de conexão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c054d4f7bb78f610afe6c1cbdf028416de7b5596
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501263"
---
# <a name="receiving-connection-notifications"></a><span data-ttu-id="90f5e-104">Recebendo notificações de conexão</span><span class="sxs-lookup"><span data-stu-id="90f5e-104">Receiving Connection Notifications</span></span>

<span data-ttu-id="90f5e-105">Alguns aplicativos precisam receber a notificação de eventos de conexão, seja antes do evento, logo após a ocorrência, ou ambos.</span><span class="sxs-lookup"><span data-stu-id="90f5e-105">Some applications need to receive notification of connection events, either before the event, just after it occurs, or both.</span></span> <span data-ttu-id="90f5e-106">Você pode criar uma DLL para receber a notificação de adiantamento e após o fato dos eventos de conexão.</span><span class="sxs-lookup"><span data-stu-id="90f5e-106">You can create a DLL to receive advance and after-the-fact notification of connection events.</span></span>

<span data-ttu-id="90f5e-107">Um exemplo de um aplicativo que precisa receber notificações antecipadas de um evento de conexão é o RAS (serviço de acesso remoto).</span><span class="sxs-lookup"><span data-stu-id="90f5e-107">An example of an application that needs to receive advance notification of a connection event is the Remote Access Service (RAS).</span></span> <span data-ttu-id="90f5e-108">O RAS precisa ser informado antes que uma conexão seja feita porque pode ser necessário estabelecer uma conexão de modem antes de fazer a conexão de rede.</span><span class="sxs-lookup"><span data-stu-id="90f5e-108">RAS needs to be informed before a connection is made because it may be necessary to establish a modem connection before making the network connection.</span></span>

<span data-ttu-id="90f5e-109">Da mesma forma, os aplicativos podem precisar limpar os recursos depois que a conexão é feita, portanto, exigindo uma notificação pós-conexão.</span><span class="sxs-lookup"><span data-stu-id="90f5e-109">Similarly, applications may need to clean up resources after the connection is made, therefore requiring a post-connection notification.</span></span>

<span data-ttu-id="90f5e-110">Os aplicativos interessados em receber o adiantamento e a notificação após o fato dos eventos de conexão devem fornecer uma DLL que exporta duas funções, [**AddConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) e [**CancelConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify).</span><span class="sxs-lookup"><span data-stu-id="90f5e-110">Applications interested in receiving advance and after-the-fact notification of connection events must supply a DLL that exports two functions, [**AddConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) and [**CancelConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify).</span></span>

<span data-ttu-id="90f5e-111">Depois de implementar essas funções, você deve registrar sua DLL, conforme descrito em [registrando para receber notificações de conexão](registering-to-receive-connection-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="90f5e-111">After you implement these functions, you must register your DLL as described in [Registering to Receive Connection Notifications](registering-to-receive-connection-notifications.md).</span></span>

 

 



