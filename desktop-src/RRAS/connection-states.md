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
# <a name="connection-states"></a>Estado da conexão

Durante o processo de conexão com um servidor remoto, o Gerenciador de conexões de acesso remoto e o servidor RAS no computador remoto executam várias etapas para estabelecer a conexão. Cada uma dessas etapas é identificada por um estado de conexão. A enumeração [**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) é um conjunto de valores que correspondem a esses Estados de conexão. Os Estados de conexão podem ser divididos em três grupos a seguir:

<dl> <dt>

<span id="Running_states"></span><span id="running_states"></span><span id="RUNNING_STATES"></span>Estados em execução
</dt> <dd>

Os Estados em execução são as partes da operação de conexão que o RAS manipula automaticamente, como conectar-se aos dispositivos necessários, autenticar o usuário e aguardar um retorno de chamada do servidor remoto. A menos que ocorra um erro, o cliente RAS não precisa executar nenhuma ação além de passar a notificação para o usuário.

</dd> <dt>

<span id="Paused_states"></span><span id="paused_states"></span><span id="PAUSED_STATES"></span>Estados em pausa
</dt> <dd>

Os [Estados pausados](paused-states.md) ocorrem quando o servidor remoto pausa a operação de conexão para obter entrada adicional do usuário. Durante um estado de pausa, o usuário pode digitar um número de [retorno de chamada](callback-connections.md) , um nome de usuário e uma senha diferentes se a autenticação do usuário falhar, ou uma nova senha se a antiga tiver expirado.

</dd> <dt>

<span id="Terminal_states"></span><span id="terminal_states"></span><span id="TERMINAL_STATES"></span>Estados de terminal
</dt> <dd>

Os Estados de terminal ocorrem quando a conexão foi estabelecida com êxito, a operação de conexão falhou ou a conexão foi quebrada por uma chamada [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) .

</dd> </dl>

Há vários mecanismos que um cliente RAS pode usar para determinar o estado atual de uma operação de conexão. Quando um cliente RAS executa a função [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) de forma assíncrona, o Gerenciador de conexão de acesso remoto envia notificações de progresso para o [manipulador de notificação](notification-handlers.md) do cliente sempre que o estado da conexão é alterado. Além disso, o cliente pode usar a função [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) para obter o estado atual de qualquer operação de conexão RAS.

 

 