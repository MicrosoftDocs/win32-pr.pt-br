---
description: Projetando para segurança
ms.assetid: 436f9d86-fbfa-4d5a-8580-fa1d4065c0aa
title: Projetando para segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69bc59b06cfcb7432806e548cc9808199b194e6e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785176"
---
# <a name="designing-for-security"></a>Projetando para segurança

A estratégia de ponta a ponta de segurança, obviamente, depende do tipo de aplicativo distribuído que você está desenvolvendo. A seguir, há várias sugestões para tratar da segurança em relação à lógica do aplicativo de camada intermediária:

-   Para obter eficiência e desempenho, autentique o mais próximo possível do usuário. Se seu aplicativo envolver uma arquitetura de lógica para banco de dados do navegador para o negócio, considere mapear os clientes do navegador para identidades de domínio, executar o aplicativo COM+ sob identidades específicas de cada aplicativo e configurar tabelas na camada de dados para que sejam acessíveis somente por uma identidade de aplicativo específica. Esse cenário de servidor confiável é mais escalonável e menos problemático do que usar o DBMS para autenticação.
-   Se estiver criando um componente que será usado em um aplicativo distribuído usando a segurança baseada em função, você poderá usar a funcionalidade de [segurança do com+](com--security.md) . Essa funcionalidade permite chamar métodos como [**IObjectContext:: IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-iscallerinrole) e [**IObjectContext:: IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-issecurityenabled) para ajudar a proteger blocos de código contra o acesso não autorizado. Você também pode usar o contexto de chamada de segurança para obter informações sobre os chamadores de um objeto.
-   Se você estiver criando um componente que será usado em um aplicativo distribuído sem usar a segurança baseada em função, a segurança será automaticamente verificada somente no nível do processo. Permissões de acesso de processo determinam quem recebe acesso ao aplicativo. Se você precisar de um controle mais detalhado sobre as configurações de segurança no processo ou no nível da interface, use a funcionalidade de segurança programática fornecida pelo COM.
-   Se um componente que usa a segurança programática do COM+ for executado sem ser integrado a um aplicativo COM+, exceções serão lançadas. Portanto, se você quiser que esse componente seja integrado com êxito a um aplicativo que não faz parte do ambiente COM+, você deve lidar com todas as exceções adequadamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Projetando para disponibilidade](designing-for-availability.md)
</dt> <dt>

[Projetando para implantação](designing-for-deployment.md)
</dt> <dt>

[Projetando para escalabilidade](designing-for-scalability.md)
</dt> <dt>

[Segurança de componente programática](programmatic-component-security.md)
</dt> </dl>

 

 



