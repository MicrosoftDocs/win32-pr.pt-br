---
title: Funções de autorização (RPC)
description: Cada vez que um programa de servidor recebe uma solicitação de cliente para acesso a um dos procedimentos remotos de gerenciamento, a biblioteca de tempo de execução RPC invoca uma função de autorização padrão.
ms.assetid: e3edbf6f-2876-49ac-a93e-14fd0b5adf53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47234f83ae76ab6ee29ed434099ba3e4a7dbb3f9c7a01a2448d0cb0dad0267dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023406"
---
# <a name="authorization-functions"></a>Funções de autorização

Cada vez que um programa de servidor recebe uma solicitação de cliente para acesso a um dos procedimentos remotos de gerenciamento, a biblioteca de tempo de execução RPC invoca uma função de autorização padrão. Essa função usa o SSP para verificar as credenciais do cliente e autorizar ou rejeitar a solicitação.

O programa do servidor pode substituir a função de autorização fornecida pelo SSP. Invoque a função [**RpcMgmtSetAuthorizationFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn) e passe-a para o endereço da sua função de autorização. Depois que o programa do servidor define a função de autorização, a biblioteca de tempo de execução RPC a chama sempre que o programa do servidor recebe uma solicitação do cliente para uma das funções de gerenciamento. Para obter mais informações, consulte [**RpcMgmtIsServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening), [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening), [**RpcMgmtInqIfIds**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqifids), [**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname)e [**RpcMgmtInqStats**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqstats).

 

 




