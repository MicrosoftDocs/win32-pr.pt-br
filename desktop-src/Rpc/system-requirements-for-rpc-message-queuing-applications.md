---
title: Requisitos do sistema para RPC-Message aplicativos de en fila
description: Para usar o transporte de enxuamento de mensagens em um aplicativo de cliente/servidor RPC, os computadores cliente e servidor devem ter a plataforma do sistema operacional apropriada e o software de Enxuamento de Mensagens instalados.
ms.assetid: f90318a6-0be6-4e1a-a1a5-1709808b5d3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46d9775e720c725ad3b0d06a0be0cf67aa438f739c6a0d1162f4940ac59e561e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924643"
---
# <a name="system-requirements-for-rpc-message-queuing-applications"></a>Requisitos do sistema para RPC-Message aplicativos de en fila

Para usar o transporte de enxuamento de mensagens em um aplicativo de cliente/servidor RPC, os computadores cliente e servidor devem ter a plataforma do sistema operacional apropriada e o software de Enxuamento de Mensagens instalados.

Os requisitos para computadores servidores são:

-   Microsoft Windows Server 2003, Windows XP ou Windows 2000 ou posterior.
-   SQL Server versão 6.5 ou posterior.
-   Controlador primário de Enterprise de mensagens ou controlador de site primário.
-   DLL de transporte do servidor RPC (RpcMqSvr.dll).

Os requisitos para computadores cliente são:

-   Microsoft Windows Server 2003, Windows XP ou Windows 2000 ou posterior.
-   Microsoft Message Queuing Client.
-   DLL de transporte do lado do cliente RPC (RpcMqCl.dll).

Quando os componentes do MSMQ são instalados nos computadores cliente e servidor, os registros do sistema são configurados automaticamente para incluir o protocolo de transporte [ncadg \_ mq](/windows/desktop/Midl/ncadg-mq) message-queuing para chamadas de procedimento remoto.

Para criar seu aplicativo RPC-MSMQ, você precisa do seguinte:

-   Microsoft Windows Server 2003, Windows XP ou Windows 2000 ou posterior
-   MIDL versão 3.1.76 ou posterior.

 

 