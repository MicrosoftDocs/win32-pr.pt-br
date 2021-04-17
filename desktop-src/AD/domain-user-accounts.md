---
title: Usando uma conta de usuário de domínio como uma conta de logon de serviço
description: Uma conta de usuário de domínio permite que o serviço Aproveite ao máximo os recursos de segurança do serviço do Windows e do Microsoft Active Directory Domain Services.
ms.assetid: 03c486fd-faec-450c-9348-314680eb73cb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.custom: contperf-fy21q3
ms.openlocfilehash: f482359eb8445cacef12c46716ecde662a95d46d
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/19/2021
ms.locfileid: "105752413"
---
# <a name="using-a-domain-user-account-as-a-service-logon-account"></a>Usando uma conta de usuário de domínio como uma conta de logon de serviço

Uma conta de usuário de domínio permite que o serviço Aproveite ao máximo os recursos de segurança do serviço do Windows e do Microsoft Active Directory Domain Services. O serviço tem qualquer acesso local e de rede concedido à conta ou a qualquer grupo do qual a conta seja membro. O serviço pode dar suporte à autenticação mútua Kerberos.

> [!Note]  
> A documentação a seguir é para os desenvolvedores. Se você for um usuário final procurando informações sobre uma mensagem de erro envolvendo contas de usuário de domínio, consulte os [fóruns da Comunidade da Microsoft](https://answers.microsoft.com). Para obter informações sobre como gerenciar contas de usuário de domínio, consulte [TechNet](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754217(v=ws.11)).

A vantagem de usar uma conta de usuário de domínio é que as ações do serviço são limitadas pelos direitos de acesso e privilégios associados à conta. Ao contrário de um `LocalSystem` serviço, os bugs em um serviço de conta de usuário não podem danificar o sistema. Se o serviço for comprometido por um ataque de segurança, o dano será isolado nas operações que o sistema permite que a conta de usuário execute. Ao mesmo tempo, os clientes em execução em diferentes níveis de privilégio podem se conectar ao serviço, o que permite que o serviço represente um cliente para executar operações confidenciais.

A conta de usuário de um serviço não deve ser um membro de grupos de administradores locais, de domínio ou corporativos. Se o serviço precisar de privilégios administrativos locais, execute-o na `LocalSystem` conta. Para operações que exigem privilégios administrativos de domínio, execute-as representando o contexto de segurança de um aplicativo cliente.

Uma instância de serviço que usa uma conta de usuário de domínio requer uma ação administrativa periódica para manter a senha da conta. O SCM (Gerenciador de controle de serviço) no computador host de uma instância de serviço armazena em cache a senha da conta para uso no registro em log no serviço. Ao alterar a senha da conta, você também deve atualizar a senha armazenada em cache no computador host em que o serviço do está instalado. Para obter mais informações e um exemplo de código, consulte [alterando a senha na conta de usuário de um serviço](changing-the-password-on-a-serviceampaposs-user-account.md). Você pode evitar a manutenção regular deixando a senha inalterada, mas isso aumentaria a probabilidade de um ataque de senha na conta de serviço. Lembre-se de que, embora o SCM armazene a senha em uma parte segura do registro, ele está, no entanto, sujeito a ataques.

Uma conta de usuário de domínio tem dois formatos de nome: o nome distinto do objeto de usuário no diretório e o <domain> \\ <username> formato "" usado pelo Gerenciador de controle de serviço local. Para obter mais informações e um exemplo de código que converte de um formato para outro, consulte [convertendo formatos de nome de conta de domínio](converting-domain-account-name-formats.md).

 

 
