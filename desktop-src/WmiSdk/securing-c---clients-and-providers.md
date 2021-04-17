---
description: Tanto os provedores de C++ quanto os aplicativos cliente devem executar muitas das mesmas operações para manter a segurança do WMI.
ms.assetid: 0199f469-2666-4794-b364-36c54aa360a8
ms.tgt_platform: multiple
title: Protegendo clientes e provedores do C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac93ee88f710bf17a2b6199b3a9b2e89279b4651
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782542"
---
# <a name="securing-c-clients-and-providers"></a>Protegendo clientes e provedores do C++

Tanto os provedores de C++ quanto os aplicativos cliente devem executar muitas das mesmas operações para manter a segurança do WMI.

Os aplicativos cliente devem definir a [representação](setting-the-default-process-security-level-using-c-.md) DCOM e os níveis de [autenticação](setting-authentication-in-wmi.md) corretamente ao se conectar ao WMI. Os retornos de chamada de [chamadas assíncronas](setting-security-on-an-asynchronous-call.md) têm riscos de segurança, portanto, os aplicativos cliente devem [executar verificações de acesso](performing-access-checks.md) para garantir que o retorno de chamada seja de uma fonte confiável. Os clientes precisam proteger os [consumidores de eventos temporários e permanentes](securing-wmi-events.md).

Um provedor pode [executar verificações de acesso](performing-access-checks.md) para garantir que os recursos que ele cria sejam acessados somente por clientes apropriados.

Os provedores e os clientes também podem definir a segurança em uma conexão de [proxy específica](setting-the-security-on-iwbemservices-and-other-proxies.md) . Ambos também podem habilitar [privilégios](executing-privileged-operations.md). Um provedor de eventos deve garantir que o consumidor do cliente tenha privilégios para [receber um evento solicitado](providing-events-securely.md).

Um cliente ou provedor pode precisar fazer uma conexão remota que exige um serviço de autenticação diferente, NTLM em vez de Kerberos, por exemplo.

 

 



