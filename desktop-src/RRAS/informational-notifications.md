---
title: Notificações informativas
description: Para os Estados de conexão conhecidos como Estados em execução, nenhuma ação é necessária para o manipulador de notificação, a menos que ocorra um erro.
ms.assetid: 3f5ea9e0-f75a-4b02-a0dc-86cb5012c242
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6223c808309fcac3afc563f02c160412c80c88
ms.sourcegitcommit: dc13cc13522097188392392d85f99de48a213984
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/28/2020
ms.locfileid: "104453885"
---
# <a name="informational-notifications"></a><span data-ttu-id="fc112-103">Notificações informativas</span><span class="sxs-lookup"><span data-stu-id="fc112-103">Informational Notifications</span></span>

<span data-ttu-id="fc112-104">Para os [Estados de conexão](connection-states.md) conhecidos como Estados em execução, nenhuma ação é necessária para o manipulador de notificação, a menos que ocorra um erro.</span><span class="sxs-lookup"><span data-stu-id="fc112-104">For the [connection states](connection-states.md) known as running states, no action is required of the notification handler unless an error occurs.</span></span> <span data-ttu-id="fc112-105">Os Estados em execução ocorrem durante as partes da operação de conexão que o RAS manipula automaticamente, como conectar-se aos dispositivos necessários, autenticar o usuário e aguardar um retorno de chamada do servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="fc112-105">Running states occur during the parts of the connection operation that RAS handles automatically, such as connecting to the necessary devices, authenticating the user, and waiting for a callback from the remote server.</span></span> <span data-ttu-id="fc112-106">A notificação é simplesmente um relatório de progresso para o cliente.</span><span class="sxs-lookup"><span data-stu-id="fc112-106">The notification is simply a progress report to the client.</span></span>

<span data-ttu-id="fc112-107">O cliente pode optar por passar essas notificações informativas para o usuário.</span><span class="sxs-lookup"><span data-stu-id="fc112-107">The client can choose to pass these informational notifications on to the user.</span></span> <span data-ttu-id="fc112-108">Em alguns Estados em execução, o cliente talvez queira exibir informações adicionais.</span><span class="sxs-lookup"><span data-stu-id="fc112-108">In some running states, the client may want to display additional information.</span></span> <span data-ttu-id="fc112-109">Por exemplo, um manipulador de notificação que recebe uma \_ notificação RASCS ConnectDevice pode chamar a função [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) para obter o nome e o tipo do dispositivo que está sendo conectado.</span><span class="sxs-lookup"><span data-stu-id="fc112-109">For example, a notification handler that receives a RASCS\_ConnectDevice notification can call the [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) function to get the name and type of the device being connected to.</span></span> <span data-ttu-id="fc112-110">Outro exemplo é quando o cliente recebe uma \_ notificação projetada de RASCS.</span><span class="sxs-lookup"><span data-stu-id="fc112-110">Another example is when the client receives a RASCS\_Projected notification.</span></span> <span data-ttu-id="fc112-111">Isso ocorre quando a fase de projeção de RAS da operação de conexão foi concluída.</span><span class="sxs-lookup"><span data-stu-id="fc112-111">This occurs when the RAS projection phase of the connection operation has been completed.</span></span> <span data-ttu-id="fc112-112">O cliente pode chamar a função [**RasGetProjectionInfo**](/previous-versions/windows/embedded/ms897107(v=msdn.10)) para obter informações adicionais sobre a projeção.</span><span class="sxs-lookup"><span data-stu-id="fc112-112">The client can call the [**RasGetProjectionInfo**](/previous-versions/windows/embedded/ms897107(v=msdn.10)) function to get additional information about the projection.</span></span> <span data-ttu-id="fc112-113">O cliente pode usar essas informações para notificar o usuário sobre quais protocolos de rede podem ser usados por essa conexão.</span><span class="sxs-lookup"><span data-stu-id="fc112-113">The client can use this information to notify the user as to which network protocols can be used by this connection.</span></span>

<span data-ttu-id="fc112-114">Você deve evitar escrever código que dependa da ordem ou ocorrência de determinados Estados informativos, pois isso pode variar entre plataformas.</span><span class="sxs-lookup"><span data-stu-id="fc112-114">You should avoid writing code that depends on the order or occurrence of particular informational states, because this may vary between platforms.</span></span>

 

 




