---
title: Usando uma conta de usuário de domínio como uma conta de logon de serviço
description: Uma conta de usuário de domínio permite que o serviço Aproveite ao máximo os recursos de segurança do serviço do Windows e do Microsoft Active Directory Domain Services.
ms.assetid: 03c486fd-faec-450c-9348-314680eb73cb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.custom: contperf-fy21q3
ms.openlocfilehash: c8defc6cc3b35ca88038ca3818b56024dfb18699
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881456"
---
# <a name="using-a-domain-user-account-as-a-service-logon-account"></a>Usando uma conta de usuário de domínio como uma conta de logon de serviço

Uma conta de usuário de domínio permite que o serviço Aproveite ao máximo os recursos de segurança do serviço do Windows e do Microsoft Active Directory Domain Services. O serviço tem qualquer acesso local e de rede concedido à conta ou a todos os grupos dos quais a conta é membro. O serviço pode dar suporte à autenticação mútua Kerberos.

> [!Note]  
> A documentação a seguir é para desenvolvedores. Se você for um usuário final que procura informações sobre uma mensagem de erro envolvendo contas de usuário de domínio, confira os Fóruns [da comunidade da Microsoft.](https://answers.microsoft.com) Para obter informações sobre como gerenciar contas de usuário de domínio, consulte [TechNet](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754217(v=ws.11)).

A vantagem de usar uma conta de usuário de domínio é que as ações do serviço são limitadas pelos direitos de acesso e privilégios associados à conta. Ao contrário `LocalSystem` de um serviço, bugs em um serviço de conta de usuário não podem danificar o sistema. Se o serviço for comprometido por um ataque de segurança, o dano será isolado das operações que o sistema permite que a conta de usuário execute. Ao mesmo tempo, os clientes em execução em diferentes níveis de privilégio podem se conectar ao serviço, o que permite que o serviço represente um cliente para executar operações confidenciais.

A conta de usuário de um serviço não deve ser membro de nenhum grupo de administradores local, domínio ou empresa. Se o serviço precisar de privilégios administrativos locais, execute-o na `LocalSystem` conta. Para operações que exigem privilégios administrativos de domínio, execute-os representando o contexto de segurança de um aplicativo cliente.

Uma instância de serviço que usa uma conta de usuário de domínio requer uma ação administrativa periódica para manter a senha da conta. O SCM (gerenciador de controle de serviço) no computador host de uma instância de serviço armazena em cache a senha da conta para uso no registro em log no serviço. Ao alterar a senha da conta, você também deve atualizar a senha armazenada em cache no computador host em que o serviço está instalado. Para obter mais informações e um exemplo de código, consulte [Alterando a senha na conta de usuário de um serviço](changing-the-password-on-a-serviceampaposs-user-account.md). Você pode evitar a manutenção regular deixando a senha inalterada, mas isso aumentaria a probabilidade de um ataque de senha na conta de serviço. Esteja ciente de que, embora o SCM armazene a senha em uma parte segura do Registro, ela está, no entanto, sujeita a ataques.

Uma conta de usuário de domínio tem dois formatos de nome: o nome diferenciado do objeto de usuário no diretório e o formato " nome de usuário de domínio " usado pelo gerenciador de controle &lt; &gt; \\ &lt; de serviço &gt; local. Para obter mais informações e um exemplo de código que converte de um formato para outro, consulte [Convertendo formatos](converting-domain-account-name-formats.md)de nome de conta de domínio .

 

 
