---
title: RPC assíncrono sobre o protocolo de Named-Pipe
description: Se você usar pipes nomeados (ncacn \_ NP) como seu protocolo de transporte, evite permitir um grande número de chamadas pendentes ociosas no servidor.
ms.assetid: a1d0f758-91bc-4821-9a82-64ba6ce575ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf46f9e1c2ea5eb3fe20203db274233f5c10dec5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917602"
---
# <a name="asynchronous-rpc-over-the-named-pipe-protocol"></a>RPC assíncrono sobre o protocolo de Named-Pipe

Se você usar pipes nomeados ([**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np)) como seu protocolo de transporte, evite permitir um grande número de chamadas pendentes ociosas no servidor. Com pipes nomeados, cada cliente aguardando uma resposta terá um pipe nomeado pendente lido no servidor, cada um deles requer uma determinada quantidade de memória do kernel.

Por exemplo, você não desejaria usar uma chamada de notificação para novos emails com o transporte de pipe nomeado, porque essa chamada permaneceria pendente mesmo quando os clientes estiverem ociosos e a memória do kernel puder ser esgotada. Observe que isso não é um problema com os outros protocolos orientados à conexão, como [**ncacn \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp).

Como os pipes nomeados são um protocolo de transporte, seu aplicativo pode usá-los especificando [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np) como o protocolo em uma associação de cadeia de caracteres. Para obter mais informações sobre pipes nomeados, consulte [pipes nomeados](/windows/desktop/ipc/named-pipes). Para obter detalhes sobre como criar associações de cadeia de caracteres, consulte [usando associações de cadeia de caracteres](finding-server-host-systems.md).

 

 