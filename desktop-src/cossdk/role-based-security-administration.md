---
description: Role-Based administração de segurança do Role-Based
ms.assetid: 7247758e-f486-4ce2-afca-f0d10fffe626
title: Role-Based administração de segurança do Role-Based
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c72ed2f1fdd5eb0b650b991b776364bf982c774b3ffcaff1358ea2c3ed1ee4d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547068"
---
# <a name="role-based-security-administration"></a>Role-Based administração de segurança do Role-Based

A segurança baseada em função é um serviço automático fornecido pelo COM+ que permite construir e impor administrativamente uma política de controle de acesso para seu aplicativo COM+. Com um modelo de configuração de segurança flexível e extensível, a segurança baseada em função oferece uma vantagem considerável em relação à imposição de toda a segurança em seus componentes e oferece os seguintes benefícios:

-   Você pode configurar a segurança administrativamente, usando a ferramenta administrativa serviços de componentes ou as funções administrativas.
-   Você não precisa escrever lógica relacionada à segurança em seus componentes quando a proteção de função no nível do método fornece um controle de acesso suficiente.
-   Você não precisa fatorar a segurança no design da interface ou do componente. Em vez disso, você pode definir a segurança de acordo com o método.
-   Você pode se concentrar na estrutura da política de segurança que deseja impor e, por meio de funções, essa política pode ser expressa claramente para os administradores que implantam seu aplicativo.
-   Você pode modificar facilmente uma política de segurança para se adaptar aos requisitos de segurança em evolução para um aplicativo.
-   Você pode criar políticas de segurança mais granulares programaticamente se precisar, usando a segurança baseada em função como uma plataforma de suporte.
-   Você pode aproveitar a segurança baseada em função para fazer auditoria detalhada, pois você pode obter informações de segurança do chamador para uma cadeia inteira de chamadas upstream.

> [!Note]  
> Os usuários na função Administrador do Aplicativo do Sistema devem ser membros do grupo de administradores locais. Além disso, a partir Windows Server 2003, a funcionalidade de autenticação para o aplicativo do sistema COM+ inclui o valor EOAC \_ DISABLE \_ AAA. Esse valor, que desabilita ativações como ativador (AAA), é usado na chamada [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ao iniciar o aplicativo do sistema. Definir a funcionalidade de autenticação como EOAC DISABLE AAA permite que um aplicativo executado em uma conta privilegiada \_ (como LocalSystem) ajude a impedir que sua identidade seja usada para iniciar componentes não \_ confidenciais.

 

Consulte os tópicos a seguir nesta seção para obter informações sobre como funciona a segurança baseada em função e problemas a considerar ao usá-la para construir uma política de segurança para um aplicativo:

-   [Usando funções para autorização de cliente](using-roles-for-client-authorization.md)
-   [Projetando funções com eficiência](designing-roles-effectively.md)
-   [Limites de segurança](security-boundaries.md)
-   [Informações de contexto de chamada de segurança](security-call-context-information.md)
-   [Propriedade de contexto de segurança](security-context-property.md)

Para ver descrições detalhadas das etapas envolvidas na configuração da segurança baseada em função para um aplicativo, consulte [Configuring Role-Based Security](configuring-role-based-security.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Autenticação de cliente](client-authentication.md)
</dt> <dt>

[Representação e delegação do cliente](client-impersonation-and-delegation.md)
</dt> <dt>

[Segurança do aplicativo de biblioteca](library-application-security.md)
</dt> <dt>

[Segurança de aplicativos de várias camadas](multi-tier-application-security.md)
</dt> <dt>

[Segurança de componente programático](programmatic-component-security.md)
</dt> <dt>

[Usando a política de restrição de software em COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
