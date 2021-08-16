---
title: Sobre contas de logon de serviço
description: Quando um serviço baseado em Win32 é iniciado, ele faz o login no computador local.
ms.assetid: 637ad0c0-118f-43e8-9d21-a93f6886f546
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49ba72ffca4362f42c6a5ad6ee494e36e9698d7883c19e3fe2a157e153ce556b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117841016"
---
# <a name="about-service-logon-accounts"></a>Sobre contas de logon de serviço

Quando um serviço baseado em Win32 é iniciado, ele faz o login no computador local. Ele pode fazer logoff como:

-   Uma conta de usuário local ou de domínio.
-   A conta LocalSystem.

A conta de logon determina a identidade de segurança do serviço em tempo de executar, ou seja, o contexto de segurança principal do serviço. O contexto de segurança determina a capacidade do serviço de acessar recursos locais e de rede. Por exemplo, um serviço em execução no contexto de segurança de uma conta de usuário local não pode acessar recursos de rede. Por outro lado, um serviço em execução no contexto de segurança da conta LocalSystem em um controlador de domínio Windows 2000 (DC), teria acesso irrestrito ao controlador de domínio. Para obter mais informações e uma discussão sobre os benefícios e limitações entre contas de usuário e LocalSystem, consulte [Contextos](security-contexts-and-active-directory-domain-services.md)de segurança e Active Directory Domain Services .

Por fim, os administradores no sistema em que o serviço está instalado têm controle sobre a conta de logon do serviço. Por motivos de segurança, alguns administradores podem não permitir que você instale seu serviço na conta LocalSystem. Seu serviço deve ser capaz de ser executado em uma conta de usuário de domínio. Como programador, você pode ter algum controle sobre a conta de logon do serviço. O instalador de serviço especifica a conta de logon do serviço quando chama a [**função CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) para instalar o serviço em um computador host. O instalador pode sugerir uma conta de logon padrão, mas deve permitir que um administrador especifique a conta real.

O instalador também pode executar as seguintes tarefas relacionadas à conta de logon do serviço:

-   Instalação. Se estiver instalando seu serviço para ser executado em uma conta de usuário, a conta deverá existir antes de você [**chamar CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea). Você pode usar uma conta existente ou criar uma como parte do host-computer installrt. Para obter mais informações, [consulte Configurando a conta de usuário de um serviço](setting-up-a-serviceampaposs-user-account.md).
-   Autenticação. Se você quiser que os clientes usem a autenticação mútua Kerberos, registre os SPNs na conta de logon do serviço. Se o serviço for executado na conta LocalSystem, a conta de logon do serviço será a conta de computador do computador host. Para saber mais, confira [Service Principal Names](service-principal-names.md) (Nomes da entidade de serviço).
-   Conceder acesso. Verifique se o serviço em tempo de execução tem os direitos de acesso e os privilégios necessários para executar suas tarefas. Isso pode exigir a configuração de ACEs (entradas de controle de acesso) nos descritores de segurança de vários recursos, ou seja, objetos de diretório, compartilhamentos de arquivos e assim por diante, para permitir os direitos de acesso necessários à conta de usuário ou computador. Para obter mais informações, consulte [Concedendo direitos de acesso à conta de logon de serviço](granting-access-rights-to-the-service-logon-account.md).
-   Definir privilégios. Atribua privilégios à conta de logon especificada, como o direito de fazer logon como um serviço no computador host. Para obter mais informações, [consulte Concedendo logon como direito de serviço no computador host.](granting-logon-as-service-right-on-the-host-computer.md)

Depois que um serviço é instalado, há tarefas de manutenção relacionadas à sua conta de logon de serviço. Para obter mais informações, consulte [Tarefas de manutenção da conta de logon](logon-account-maintenance-tasks.md).

-   Manutenção de senha. Para um serviço executado em uma conta de usuário, você deve alterar periodicamente a senha e manter a senha em sincronia com a senha usada por um ou mais gerenciadores de controle de serviço local para iniciar o serviço.
-   Manutenção do SPN. Se uma conta de logon de serviço for mudada, remova os SPNs registrados na conta antiga e registre-os na nova conta. Esteja ciente de que quando um serviço é instalado, um administrador de domínio pode alterar a conta na qual o serviço é executado; use funções Win32 ou a interface do usuário da ferramenta administrativa de Gerenciamento do Computador.
-   Manutenção ace. Se uma conta de logon de serviço for mudada, você precisará atualizar acEs e associações de grupo para garantir que o serviço ainda possa acessar os recursos necessários.

 

 