---
title: Estado da conexão
description: Durante o processo de conexão com um servidor remoto, o Gerenciador de conexões de acesso remoto e o servidor RAS no computador remoto executam várias etapas para estabelecer a conexão.
ms.assetid: 7a8b0086-308b-47d2-888e-69ff473c6015
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df4488cc020a8a1b2a7da93384a4a5be1edb5182
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823878"
---
# <a name="connection-states"></a><span data-ttu-id="8775a-103">Estado da conexão</span><span class="sxs-lookup"><span data-stu-id="8775a-103">Connection States</span></span>

<span data-ttu-id="8775a-104">Durante o processo de conexão com um servidor remoto, o Gerenciador de conexões de acesso remoto e o servidor RAS no computador remoto executam várias etapas para estabelecer a conexão.</span><span class="sxs-lookup"><span data-stu-id="8775a-104">During the process of connecting to a remote server, the Remote Access Connection Manager and the RAS server on the remote computer perform several steps to establish the connection.</span></span> <span data-ttu-id="8775a-105">Cada uma dessas etapas é identificada por um estado de conexão.</span><span class="sxs-lookup"><span data-stu-id="8775a-105">Each of these steps is identified by a connection state.</span></span> <span data-ttu-id="8775a-106">A enumeração [**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) é um conjunto de valores que correspondem a esses Estados de conexão.</span><span class="sxs-lookup"><span data-stu-id="8775a-106">The [**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) enumeration is a set of values that correspond to these connection states.</span></span> <span data-ttu-id="8775a-107">Os Estados de conexão podem ser divididos em três grupos a seguir:</span><span class="sxs-lookup"><span data-stu-id="8775a-107">The connection states can be divided into the following three groups:</span></span>

<dl> <dt>

<span data-ttu-id="8775a-108"><span id="Running_states"></span><span id="running_states"></span><span id="RUNNING_STATES"></span>Estados em execução</span><span class="sxs-lookup"><span data-stu-id="8775a-108"><span id="Running_states"></span><span id="running_states"></span><span id="RUNNING_STATES"></span>Running states</span></span>
</dt> <dd>

<span data-ttu-id="8775a-109">Os Estados em execução são as partes da operação de conexão que o RAS manipula automaticamente, como conectar-se aos dispositivos necessários, autenticar o usuário e aguardar um retorno de chamada do servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="8775a-109">The running states are the parts of the connection operation that RAS handles automatically, such as connecting to the necessary devices, authenticating the user, and waiting for a callback from the remote server.</span></span> <span data-ttu-id="8775a-110">A menos que ocorra um erro, o cliente RAS não precisa executar nenhuma ação além de passar a notificação para o usuário.</span><span class="sxs-lookup"><span data-stu-id="8775a-110">Unless an error occurs, the RAS client need take no action other than to pass the notification on to the user.</span></span>

</dd> <dt>

<span data-ttu-id="8775a-111"><span id="Paused_states"></span><span id="paused_states"></span><span id="PAUSED_STATES"></span>Estados em pausa</span><span class="sxs-lookup"><span data-stu-id="8775a-111"><span id="Paused_states"></span><span id="paused_states"></span><span id="PAUSED_STATES"></span>Paused states</span></span>
</dt> <dd>

<span data-ttu-id="8775a-112">Os [Estados pausados](paused-states.md) ocorrem quando o servidor remoto pausa a operação de conexão para obter entrada adicional do usuário.</span><span class="sxs-lookup"><span data-stu-id="8775a-112">The [paused states](paused-states.md) occur when the remote server pauses the connection operation to get additional input from the user.</span></span> <span data-ttu-id="8775a-113">Durante um estado de pausa, o usuário pode digitar um número de [retorno de chamada](callback-connections.md) , um nome de usuário e uma senha diferentes se a autenticação do usuário falhar, ou uma nova senha se a antiga tiver expirado.</span><span class="sxs-lookup"><span data-stu-id="8775a-113">During a paused state, the user can type a [callback](callback-connections.md) number, a different user name and password if the user authentication fails, or a new password if the old one has expired.</span></span>

</dd> <dt>

<span data-ttu-id="8775a-114"><span id="Terminal_states"></span><span id="terminal_states"></span><span id="TERMINAL_STATES"></span>Estados de terminal</span><span class="sxs-lookup"><span data-stu-id="8775a-114"><span id="Terminal_states"></span><span id="terminal_states"></span><span id="TERMINAL_STATES"></span>Terminal states</span></span>
</dt> <dd>

<span data-ttu-id="8775a-115">Os Estados de terminal ocorrem quando a conexão foi estabelecida com êxito, a operação de conexão falhou ou a conexão foi quebrada por uma chamada [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) .</span><span class="sxs-lookup"><span data-stu-id="8775a-115">The terminal states occur when the connection has been successfully established, the connection operation has failed, or the connection has been broken by a [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) call.</span></span>

</dd> </dl>

<span data-ttu-id="8775a-116">Há vários mecanismos que um cliente RAS pode usar para determinar o estado atual de uma operação de conexão.</span><span class="sxs-lookup"><span data-stu-id="8775a-116">There are several mechanisms that a RAS client can use to determine the current state of a connection operation.</span></span> <span data-ttu-id="8775a-117">Quando um cliente RAS executa a função [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) de forma assíncrona, o Gerenciador de conexão de acesso remoto envia notificações de progresso para o [manipulador de notificação](notification-handlers.md) do cliente sempre que o estado da conexão é alterado.</span><span class="sxs-lookup"><span data-stu-id="8775a-117">When a RAS client executes the [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) function asynchronously, the Remote Access Connection Manager sends progress notifications to the client's [notification handler](notification-handlers.md) whenever the connection state changes.</span></span> <span data-ttu-id="8775a-118">Além disso, o cliente pode usar a função [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) para obter o estado atual de qualquer operação de conexão RAS.</span><span class="sxs-lookup"><span data-stu-id="8775a-118">In addition, the client can use the [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) function to get the current state of any RAS connection operation.</span></span>

 

 