---
description: Como um aplicativo de biblioteca COM+ é hospedado por outro processo, que pode ter suas próprias configurações de segurança, a segurança para aplicativos de biblioteca requer consideração especial.
ms.assetid: a966020c-a0bd-467c-b6d3-e09267cf5574
title: Segurança do aplicativo de biblioteca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f9fa2d03f21707af42fa108cb9c4ecbce6d2a352ea03714961a0eef4f028119
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118813515"
---
# <a name="library-application-security"></a>Segurança do aplicativo de biblioteca

Como um aplicativo de biblioteca COM+ é hospedado por outro processo, que pode ter suas próprias configurações de segurança, a segurança para aplicativos de biblioteca requer consideração especial.

As seguintes restrições se aplicam à segurança do aplicativo de biblioteca:

-   Os aplicativos de biblioteca são executados no token de segurança do processo do cliente, em vez de em sua própria identidade de usuário. Eles têm apenas o mesmo privilégio que o cliente.
-   Os aplicativos de biblioteca não controlam a segurança no nível do processo. Nenhum usuário em funções será adicionado ao descritor de segurança para o processo. A única maneira de um aplicativo de biblioteca executar suas próprias verificações de acesso é usar a segurança no nível do componente. (Consulte [Limites de segurança](security-boundaries.md).)
-   Os aplicativos de biblioteca podem ser configurados para participar ou não da autenticação do processo de host, habilitando ou desabilitando a autenticação. (Consulte [Habilitando a autenticação para um aplicativo de biblioteca](enabling-authentication-for-a-library-application.md).)
-   Os aplicativos de biblioteca não podem definir um nível de representação; eles usam o do processo de host.

## <a name="using-library-applications-to-limit-application-privilege"></a>Usando aplicativos de biblioteca para limitar o privilégio do aplicativo

Em alguns casos, talvez você queira configurar um aplicativo especificamente como um aplicativo de biblioteca para que ele seja executado sob a identidade do processo de hospedagem. Isso limita fundamentalmente o aplicativo para que ele possa acessar somente os recursos que seu cliente, o processo de host, pode acessar. Os threads em que os componentes do aplicativo de biblioteca são executados usarão o token de processo por padrão e, portanto, quando fizerem chamadas fora do aplicativo ou acessarem recursos, como arquivos protegidos com um descritor de segurança, eles parecerão ser o cliente. Para aplicativos que executam um trabalho sensível, essa pode ser uma maneira fácil de controlar o escopo de suas ações.

## <a name="effectively-securing-library-applications"></a>Proteger efetivamente aplicativos de biblioteca

Há considerações especiais sobre como configurar a segurança baseada em função e a autenticação para aplicativos de biblioteca para que eles sejam bem-desempenhos conforme o esperado. Para obter detalhes, consulte [Configurando a segurança para aplicativos de biblioteca.](configuring-security-for-library-applications.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Autenticação de cliente](client-authentication.md)
</dt> <dt>

[Representação e delegação do cliente](client-impersonation-and-delegation.md)
</dt> <dt>

[Segurança de aplicativos de várias camadas](multi-tier-application-security.md)
</dt> <dt>

[Segurança de componente programático](programmatic-component-security.md)
</dt> <dt>

[Administração de segurança baseada em função](role-based-security-administration.md)
</dt> <dt>

[Usando a política de restrição de software em COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 



