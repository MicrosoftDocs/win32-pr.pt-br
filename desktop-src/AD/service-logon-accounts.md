---
title: Contas de logon de serviço
description: Um serviço, como qualquer processo, tem uma identidade de segurança primária que determina os direitos de acesso e privilégios concedidos para recursos locais e de rede.
ms.assetid: c2345967-8415-4cc0-96d3-12c48e74028e
ms.tgt_platform: multiple
keywords:
- Active Directory, usando, logon de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9340fe7eebc95ec4c7ea3091c96a2539cb08dee4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822251"
---
# <a name="service-logon-accounts"></a>Contas de logon de serviço

Um serviço, como qualquer processo, tem uma identidade de segurança primária que determina os direitos de acesso e privilégios concedidos para recursos locais e de rede. Essa identidade de segurança, ou contexto de segurança, também determina o potencial que o serviço tem para danificar recursos locais e de rede.

O contexto de segurança para um serviço Microsoft Win32 é determinado pela conta de logon que é usada para iniciar o serviço. Esta seção discute problemas de programação e práticas recomendadas relacionadas à conta de logon de serviço usada pelos serviços do Win32, com foco em serviços habilitados para diretório. Esta seção inclui os tópicos a seguir:

-   [Sobre as contas de logon de serviço](about-service-logon-accounts.md)— uma visão geral das contas de logon de serviço e problemas de programação de contexto de segurança para um serviço Win32.
-   [Diretrizes para selecionar uma conta de logon de serviço](guidelines-for-selecting-a-service-logon-account.md) para um serviço Win32.
-   [Configuração da conta de usuário de um serviço](setting-up-a-serviceampaposs-user-account.md).
-   [Instalar um serviço em um computador host](installing-a-service-on-a-host-computer.md) e especificar a conta de logon do serviço.
-   [Concedendo logon como serviço diretamente no computador host](granting-logon-as-service-right-on-the-host-computer.md), concedendo à conta de usuário do serviço o direito de logon como um serviço no computador host.
-   [Testando se em execução em um controlador de domínio](testing-whether-running-on-a-domain-controller.md)— detectando no momento da instalação se a instância do serviço está sendo instalada em um controlador de domínio.
-   [Concessão de direitos de acesso à conta de logon do serviço](granting-access-rights-to-the-service-logon-account.md)— definindo e mantendo ACEs e associações de grupo para garantir que o sistema conceda acesso ao serviço em execução aos recursos locais e de rede necessários.
-   [Alterar a senha na conta de usuário de um serviço](changing-the-password-on-a-serviceampaposs-user-account.md)— alterar a senha na conta de usuário de um serviço e, ao mesmo tempo, atualizar a senha registrada com o Gerenciador de controle de serviço em cada servidor host no qual o serviço está instalado.
-   [Autenticação mútua usando Kerberos](mutual-authentication-using-kerberos.md)— mantendo o registro SPN (nome da entidade de serviço) no objeto de diretório associado à conta de logon de cada instância do serviço. Os SPNs permitem que os clientes autentiquem um serviço usando a autenticação mútua do Kerberos.
-   [Convertendo formatos de nome de conta de domínio](converting-domain-account-name-formats.md)— por exemplo, convertendo um nome diferenciado em formato de nome de ****\\*** usuário de domínio* e vice-versa.

 

 




