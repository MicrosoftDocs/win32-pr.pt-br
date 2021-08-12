---
description: Administração de segurança do Role-Based
ms.assetid: 7247758e-f486-4ce2-afca-f0d10fffe626
title: Administração de segurança do Role-Based
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c72ed2f1fdd5eb0b650b991b776364bf982c774b3ffcaff1358ea2c3ed1ee4d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547068"
---
# <a name="role-based-security-administration"></a>Administração de segurança do Role-Based

A segurança baseada em função é um serviço automático fornecido pelo COM+ que permite que você construa administrativamente e aplique uma política de controle de acesso para seu aplicativo COM+. Com um modelo de configuração de segurança flexível e extensível, a segurança baseada em função oferece uma vantagem considerável sobre a imposição de toda a segurança em seus componentes e oferece os seguintes benefícios:

-   Você pode configurar a segurança administrativamente, usando a ferramenta administrativa serviços de componentes ou as funções administrativas.
-   Você não precisa escrever lógica relacionada à segurança em seus componentes quando a proteção de função no nível do método fornece um controle de acesso suficiente.
-   Você não precisa considerar a segurança na interface ou no design de componentes. Em vez disso, você pode definir a segurança em uma base método por método.
-   Você pode se concentrar na estrutura da política de segurança que deseja impor e por meio de funções, essa política pode ser claramente expressa para os administradores que implantam seu aplicativo.
-   Você pode facilmente modificar uma política de segurança para se adaptar aos requisitos de segurança em evolução de um aplicativo.
-   Você pode criar políticas de segurança mais granulares programaticamente se precisar, usando a segurança baseada em função como plataforma de suporte.
-   Você pode aproveitar a segurança baseada em função para fazer auditoria detalhada, pois você pode obter informações de segurança do chamador para uma cadeia inteira de chamadas upstream.

> [!Note]  
> Os usuários na função Administrador do aplicativo do sistema devem ser membros do grupo Administradores local. além disso, a partir do Windows Server 2003, o recurso de autenticação para o aplicativo de sistema COM+ inclui o valor EOAC \_ DISABLE \_ AAA. Esse valor, que desabilita as ativações de Activate-as-Activator (AAA), é usado na chamada [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ao iniciar o aplicativo do sistema. Definir o recurso de autenticação como EOAC \_ Disable \_ AAA permite que um aplicativo executado em uma conta com privilégios (como LocalSystem) ajude a impedir que sua identidade seja usada para iniciar componentes não confiáveis.

 

Consulte os tópicos a seguir nesta seção para obter informações sobre como funciona a segurança baseada em função e problemas a serem considerados ao usá-lo para construir uma política de segurança para um aplicativo:

-   [Usando funções para autorização de cliente](using-roles-for-client-authorization.md)
-   [Criando funções com eficiência](designing-roles-effectively.md)
-   [Limites de segurança](security-boundaries.md)
-   [Informações de contexto de chamada de segurança](security-call-context-information.md)
-   [Propriedade de contexto de segurança](security-context-property.md)

Para obter descrições detalhadas das etapas envolvidas na configuração da segurança baseada em função para um aplicativo, consulte [configuring Role-Based Security](configuring-role-based-security.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Autenticação de cliente](client-authentication.md)
</dt> <dt>

[Representação e delegação de cliente](client-impersonation-and-delegation.md)
</dt> <dt>

[Segurança de aplicativos de biblioteca](library-application-security.md)
</dt> <dt>

[Segurança de aplicativos de várias camadas](multi-tier-application-security.md)
</dt> <dt>

[Segurança de componente programática](programmatic-component-security.md)
</dt> <dt>

[Usando a política de restrição de software no COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
