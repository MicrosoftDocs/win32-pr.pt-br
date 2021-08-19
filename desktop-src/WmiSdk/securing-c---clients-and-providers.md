---
description: Os provedores C++ e os aplicativos cliente devem executar muitas das mesmas operações para manter a segurança do WMI.
ms.assetid: 0199f469-2666-4794-b364-36c54aa360a8
ms.tgt_platform: multiple
title: Proteger clientes e provedores C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4151440f9e85f7cd9e6590842ffd3d103242410b38f52287dba83ba3bb3faec5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316155"
---
# <a name="securing-c-clients-and-providers"></a>Proteger clientes e provedores C++

Os provedores C++ e os aplicativos cliente devem executar muitas das mesmas operações para manter a segurança do WMI.

Os aplicativos cliente devem definir [os](setting-the-default-process-security-level-using-c-.md) níveis de representação e [autenticação](setting-authentication-in-wmi.md) do DCOM corretamente ao se conectar ao WMI. Retornos de chamada de [chamadas assíncronas](setting-security-on-an-asynchronous-call.md) têm [](performing-access-checks.md) riscos de segurança, portanto, os aplicativos cliente devem executar verificações de acesso para garantir que o retorno de chamada seja de uma fonte confiável. Os clientes precisam proteger os consumidores [de eventos temporários e permanentes.](securing-wmi-events.md)

Um provedor pode [executar verificações de](performing-access-checks.md) acesso para garantir que os recursos que ele cria sejam acessados apenas por clientes apropriados.

Os provedores e os clientes também podem definir a segurança em uma [conexão de proxy](setting-the-security-on-iwbemservices-and-other-proxies.md) específica. Ambos também podem habilitar [privilégios](executing-privileged-operations.md). Um provedor de eventos deve garantir que o consumidor cliente tenha privilégios para [receber um evento solicitado.](providing-events-securely.md)

Um cliente ou provedor pode precisar fazer uma conexão remota que exija um serviço de autenticação diferente, NTLM em vez de Kerberos, por exemplo.

 

 



