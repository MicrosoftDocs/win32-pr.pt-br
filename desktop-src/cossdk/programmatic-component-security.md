---
description: Quando você usa a segurança baseada em função no aplicativo COM+ que contém o componente, você tem acesso à funcionalidade de segurança programática de dentro do seu componente.
ms.assetid: 6117970c-5dbd-485e-978e-3aa96e42b359
title: Segurança de componente programática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31622608e4d4f54aeb53b403b5d8711ff9c6a9af
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763087"
---
# <a name="programmatic-component-security"></a>Segurança de componente programática

Quando você usa a segurança baseada em função no aplicativo COM+ que contém o componente, você tem acesso à funcionalidade de segurança programática de dentro do seu componente. Você pode verificar a associação de função para determinar se seções específicas de código são executadas. você pode acessar informações de segurança usando o objeto de contexto de chamada de segurança e pode determinar se a segurança está habilitada para a chamada atual. Você pode executar todas essas tarefas usando uma referência a um objeto [**SecurityCallContext**](securitycallcontext.md) (para aplicativos do Microsoft Visual Basic) ou um ponteiro para a interface [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) (para aplicativos C e Microsoft Visual C++).

Para obter mais informações sobre a segurança baseada em função programática, consulte os seguintes tópicos nesta seção:

-   [Verificando a associação de função](checking-role-membership.md)
-   [Determinando se a segurança do Role-Based está habilitada](determining-whether-role-based-security-is-enabled.md)
-   [Acessando informações de contexto de chamada de segurança](accessing-security-call-context-information.md)

## <a name="impersonation-and-com-security-features"></a>Representação e recursos de segurança COM

Se o componente for usado em um aplicativo COM+ que não usa segurança baseada em função, a verificação de função programática e as informações de contexto de chamada de segurança não estarão disponíveis. No entanto, você pode usar a funcionalidade de segurança programática fornecida pelo COM. Para obter mais informações, consulte [segurança em com](/windows/desktop/com/security-in-com).

Embora você possa usar a maior parte da funcionalidade de segurança fornecida pelo COM, não é possível chamar [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) de um componente que faz parte de um aplicativo com+, pois **CoInitializeSecurity** é chamado pelo substituto em que o aplicativo com+ é executado. No entanto, você pode chamar outras funções de segurança, como [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket), que recupera informações sobre o cliente.

Em particular, quando você precisa usar a identidade do cliente para acessar algum recurso — por exemplo, acessar um arquivo protegido por um descritor de segurança ou propagar a identidade do cliente por meio de um banco de dados — você pode executar a representação programaticamente. Para obter mais detalhes sobre quando e como fazer isso, consulte [representação e delegação do cliente](client-impersonation-and-delegation.md).

## <a name="testing-security-functionality"></a>Testando a funcionalidade de segurança

Se você usar a segurança programática do COM+ em seu componente, deverá integrar o componente a um aplicativo COM+ quando estiver pronto para testar a funcionalidade de segurança do componente. Se um componente que usa a segurança programática do COM+ for executado sem ser integrado a um aplicativo COM+, exceções serão lançadas. Portanto, se você quiser garantir que esse componente também seja capaz de ser integrado com êxito a um aplicativo que não faz parte do ambiente COM+, deverá garantir que essas exceções sejam tratadas adequadamente.

## <a name="documenting-security-requirements"></a>Documentando os requisitos de segurança

Se você estiver escrevendo um componente autônomo para aplicativos COM+ que usam a segurança baseada em função, você precisará documentar o componente para que a segurança possa ser configurada adequadamente quando o componente for integrado a um aplicativo COM+. Por exemplo, você deve identificar as funções que devem ser adicionadas e explicar a quais métodos e interfaces cada função deve ser atribuída. Além disso, se um método como IsCallerInRole ("caixas") for chamado, você deverá descrever a funcionalidade que apenas os informadores têm acesso ao. Você também deve especificar se uma função é necessária para ajudar a proteger o acesso a todo o componente.

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

[Administração de segurança baseada em funções](role-based-security-administration.md)
</dt> <dt>

[Usando a política de restrição de software no COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
