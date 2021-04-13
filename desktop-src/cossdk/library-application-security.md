---
description: Como um aplicativo de biblioteca COM+ é hospedado por outro processo, que pode ter suas próprias configurações de segurança, a segurança para aplicativos de biblioteca requer uma consideração especial.
ms.assetid: a966020c-a0bd-467c-b6d3-e09267cf5574
title: Segurança de aplicativos de biblioteca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d2885173f3798d33ed26a5b447fde4429b9bf96
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500892"
---
# <a name="library-application-security"></a>Segurança de aplicativos de biblioteca

Como um aplicativo de biblioteca COM+ é hospedado por outro processo, que pode ter suas próprias configurações de segurança, a segurança para aplicativos de biblioteca requer uma consideração especial.

As seguintes restrições se aplicam à segurança do aplicativo de biblioteca:

-   Os aplicativos de biblioteca são executados no token de segurança do processo do cliente em vez de em sua própria identidade de usuário. Eles têm apenas tantos privilégios quanto o cliente.
-   Os aplicativos de biblioteca não controlam a segurança em nível de processo. Nenhum usuário em funções será adicionado ao descritor de segurança para o processo. A única maneira de um aplicativo de biblioteca executar suas próprias verificações de acesso é usar a segurança em nível de componente. (Consulte [limites de segurança](security-boundaries.md).)
-   Os aplicativos de biblioteca podem ser configurados para participar ou não participar da autenticação de processo de host, habilitando ou desabilitando a autenticação. (Consulte [habilitando a autenticação para um aplicativo de biblioteca](enabling-authentication-for-a-library-application.md).)
-   Aplicativos de biblioteca não podem definir um nível de representação; Eles usam o do processo de host.

## <a name="using-library-applications-to-limit-application-privilege"></a>Usando aplicativos de biblioteca para limitar o privilégio do aplicativo

Em alguns casos, talvez você queira configurar um aplicativo especificamente como um aplicativo de biblioteca para que ele seja executado sob a identidade do processo de hospedagem. Isso limita o aplicativo de forma fundamental para que ele possa acessar somente os recursos que o cliente, o processo de host, pode acessar. Os threads nos quais os componentes do aplicativo de biblioteca são executados usarão o token de processo por padrão e, portanto, quando eles fazem chamadas fora do aplicativo ou acessam recursos como arquivos protegidos com um descritor de segurança, parecerão ser o cliente. Para aplicativos que executam trabalho confidencial, essa pode ser uma maneira fácil de controlar o escopo de suas ações.

## <a name="effectively-securing-library-applications"></a>Protegendo aplicativos de biblioteca com eficiência

Há considerações especiais na configuração da segurança baseada em função e da autenticação para aplicativos de biblioteca para que eles sejam executados conforme o esperado. Para obter detalhes, consulte [Configurando a segurança para aplicativos de biblioteca](configuring-security-for-library-applications.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Autenticação de cliente](client-authentication.md)
</dt> <dt>

[Representação e delegação de cliente](client-impersonation-and-delegation.md)
</dt> <dt>

[Segurança de aplicativos de várias camadas](multi-tier-application-security.md)
</dt> <dt>

[Segurança de componente programática](programmatic-component-security.md)
</dt> <dt>

[Administração de segurança baseada em funções](role-based-security-administration.md)
</dt> <dt>

[Usando a política de restrição de software no COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 



