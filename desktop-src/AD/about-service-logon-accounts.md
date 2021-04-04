---
title: Sobre contas de logon de serviço
description: Quando um serviço baseado em Win32 é iniciado, ele faz logon no computador local.
ms.assetid: 637ad0c0-118f-43e8-9d21-a93f6886f546
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 328b33d5dab36ccc5a803eb7c43ca3112e96ecf8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104084425"
---
# <a name="about-service-logon-accounts"></a>Sobre contas de logon de serviço

Quando um serviço baseado em Win32 é iniciado, ele faz logon no computador local. Ele pode fazer logon como:

-   Uma conta de usuário local ou de domínio.
-   A conta LocalSystem.

A conta de logon determina a identidade de segurança do serviço em tempo de execução, ou seja, o contexto de segurança principal do serviço. O contexto de segurança determina a capacidade do serviço de acessar recursos locais e de rede. Por exemplo, um serviço em execução no contexto de segurança de uma conta de usuário local não pode acessar recursos de rede. Por outro lado, um serviço em execução no contexto de segurança da conta LocalSystem em um controlador de domínio (DC) do Windows 2000 teria acesso irrestrito ao DC. Para obter mais informações e uma discussão sobre os benefícios e as limitações entre contas de usuário e LocalSystem, consulte [contextos de segurança e Active Directory Domain Services](security-contexts-and-active-directory-domain-services.md).

Por fim, os administradores no sistema em que o serviço está instalado têm controle sobre a conta de logon do serviço. Por motivos de segurança, alguns administradores podem não permitir que você instale seu serviço na conta LocalSystem. Seu serviço deve ser capaz de ser executado em uma conta de usuário de domínio. Como programador, você pode exercer algum controle sobre a conta de logon de seu serviço. O instalador do serviço especifica a conta de logon do serviço ao chamar a função [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) para instalar o serviço em um computador host. O instalador pode sugerir uma conta de logon padrão, mas deve permitir que um administrador especifique a conta real.

O instalador também pode executar as seguintes tarefas relacionadas à conta de logon do seu serviço:

-   Instalação. Se você estiver instalando seu serviço para ser executado em uma conta de usuário, a conta deverá existir antes de você chamar [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea). Você pode usar uma conta existente ou criar uma como parte do computador host installrt. Para obter mais informações, consulte [Configurando a conta de usuário de um serviço](setting-up-a-serviceampaposs-user-account.md).
-   Autenticação. Se você quiser que os clientes usem a autenticação mútua Kerberos, registre os SPNs na conta de logon do serviço. Se o serviço for executado na conta LocalSystem, a conta de logon do serviço será a conta de computador do computador host. Para saber mais, confira [Service Principal Names](service-principal-names.md) (Nomes da entidade de serviço).
-   Conceder acesso. Verifique se o serviço em tempo de execução tem os direitos de acesso e os privilégios necessários para executar suas tarefas. Isso pode exigir a definição de ACEs (entradas de controle de acesso) nos descritores de segurança de vários recursos, que são objetos de diretório, compartilhamentos de arquivos e assim por diante, para permitir os direitos de acesso necessários à conta de usuário ou de computador. Para obter mais informações, consulte [concedendo direitos de acesso à conta de logon do serviço](granting-access-rights-to-the-service-logon-account.md).
-   Definir privilégios. Atribua privilégios à conta de logon especificada, como o direito de fazer logon como um serviço no computador host. Para obter mais informações, consulte [concedendo logon como serviço diretamente no computador host](granting-logon-as-service-right-on-the-host-computer.md).

Depois que um serviço é instalado, há tarefas de manutenção relacionadas à sua conta de logon de serviço. Para obter mais informações, consulte [tarefas de manutenção de conta de logon](logon-account-maintenance-tasks.md).

-   Manutenção de senha. Para um serviço que é executado em uma conta de usuário, você deve alterar periodicamente a senha e manter a senha em sincronia com a senha usada por um ou mais gerenciadores de controle de serviço local para iniciar o serviço.
-   Manutenção de SPN. Se uma conta de logon de serviço for alterada, remova os SPNs registrados na conta antiga e registre-os na nova conta. Lembre-se de que, quando um serviço é instalado, um administrador de domínio pode alterar a conta sob a qual seu serviço é executado; Use o Win32 Functions ou a interface do usuário da ferramenta administrativa de gerenciamento do computador.
-   Manutenção da ACE. Se uma conta de logon de serviço for alterada, você precisará atualizar ACEs e associações de grupo para garantir que o serviço ainda possa acessar os recursos necessários.

 

 