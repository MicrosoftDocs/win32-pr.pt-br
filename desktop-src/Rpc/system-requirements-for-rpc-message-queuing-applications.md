---
title: Requisitos do sistema para aplicativos de enfileiramento RPC-Message
description: Para usar o transporte de enfileiramento de mensagens em um aplicativo cliente/servidor RPC, o servidor e os computadores cliente devem ter a plataforma de sistema operacional e o software de enfileiramento de mensagens apropriados instalados.
ms.assetid: f90318a6-0be6-4e1a-a1a5-1709808b5d3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1274c888506a6868eb7ded5ba96c5f1ea8dc8b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366527"
---
# <a name="system-requirements-for-rpc-message-queuing-applications"></a>Requisitos do sistema para aplicativos de enfileiramento RPC-Message

Para usar o transporte de enfileiramento de mensagens em um aplicativo cliente/servidor RPC, o servidor e os computadores cliente devem ter a plataforma de sistema operacional e o software de enfileiramento de mensagens apropriados instalados.

Os requisitos para computadores servidores são:

-   Microsoft Windows Server 2003, Windows XP ou Windows 2000 ou posterior.
-   SQL Server versão 6,5 ou posterior.
-   Controlador corporativo primário do enfileiramento de mensagens ou controlador de site primário.
-   DLL de transporte do lado do servidor RPC (RpcMqSvr.dll).

Os requisitos para computadores cliente são:

-   Microsoft Windows Server 2003, Windows XP ou Windows 2000 ou posterior.
-   Cliente de enfileiramento de mensagens da Microsoft.
-   DLL de transporte do lado do cliente RPC (RpcMqCl.dll).

Quando os componentes do MSMQ são instalados nos computadores cliente e servidor, os registros do sistema são configurados automaticamente para incluir o protocolo de transporte de enfileiramento de mensagens do [ncadg \_ MQ](/windows/desktop/Midl/ncadg-mq) para chamadas de procedimento remoto.

Para criar seu aplicativo RPC-MSMQ, você precisará do seguinte:

-   Microsoft Windows Server 2003, Windows XP ou Windows 2000 ou posterior
-   MIDL versão 3.1.76 ou posterior.

 

 