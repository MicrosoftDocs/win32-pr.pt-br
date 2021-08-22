---
title: O que os desenvolvedores de aplicativos e serviços precisam saber sobre grupos
description: Ao desenvolver um aplicativo ou serviço, você pode usar grupos para delegar administração ou controlar o acesso ao aplicativo ou serviço como um todo ou parte.
ms.assetid: 19e189a5-2880-4b45-84c8-e7b542c4fbb6
ms.tgt_platform: multiple
keywords:
- O que os desenvolvedores de aplicativos e serviços precisam saber sobre grupos
- grupos do AD , informações para desenvolvedores de aplicativos e serviços
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b59a8a1ce369d9b5fa1093297f219bf6a206178a950b9d0762fde3069846551
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024384"
---
# <a name="what-application-and-service-developers-need-to-know-about-groups"></a>O que os desenvolvedores de aplicativos e serviços precisam saber sobre grupos

Ao desenvolver um aplicativo ou serviço, você pode usar grupos para delegar administração ou controlar o acesso ao aplicativo ou serviço como um todo ou parte. Por exemplo, um aplicativo pode controlar quem pode executar várias operações administrativas. Para fazer isso, crie ACEs que concedem direitos de acesso especificados aos grupos apropriados. É uma boa prática de programação ter uma ACE que conceda acesso a um grupo do que ter várias ACEs que concedem acesso a usuários ou computadores individuais.

É recomendável que os aplicativos usem as seguintes diretrizes ao usar grupos:

-   Não crie dependências em grupos codificados, o que poderá criar complicações se o grupo for excluído ou movido.
-   Evite usar grupos integrados, a menos que a função do grupo fornece as necessidades específicas para o aplicativo. Por exemplo, não exigir que um usuário seja membro do grupo Administradores apenas para fornecer ao usuário permissão para criar uma conta de computador. Isso fornece ao usuário permissões e privilégios que talvez não precisem, o que pode causar vulnerabilidade de segurança. Em vez disso, você deve criar um novo grupo de segurança que tenha as permissões específicas necessárias e adicionar o usuário a esse novo grupo.
-   Ao criar novos grupos, tenha em mente as seguintes recomendações:
    -   Proteja o grupo definindo ACEs que controlam quem pode adicionar ou remover membros.
    -   Use grupos globais se eles são usados para controle de acesso em objetos Active Directory Domain Services.
    -   Use grupos universais somente se necessário (os dados de membro são necessários globalmente usando o catálogo global; o grupo pode conter qualquer usuário/grupo). Se você usar grupos universais, coloque grupos globais no grupo universal e adicione/remova usuários do grupo global. Evite alterações em excesso em grupos universais para eficiência de replicação.
-   Não use a associação de grupo para controle de acesso. Em vez disso, use uma ACE e controle o acesso fazendo com que o sistema execute uma verificação de acesso.

Para controlar o acesso a operações que não se ajustam aos direitos de acesso predefinidos para objetos nos serviços Domínio do Active Directory, use o recurso de direitos de acesso de controle do controle de acesso no Windows 2000. Para obter mais informações, consulte [**ADS \_ RIGHTS \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_rights_enum).

**Para usar um direito de acesso de controle para controlar o direito de executar uma operação**

1.  Crie um direito de acesso de controle que define o tipo de acesso ao aplicativo ou serviço. Para obter mais informações, consulte [Controlar direitos de acesso.](control-access-rights.md)
2.  Crie um objeto no Active Directory Domain Services que representa o aplicativo, o serviço ou o recurso.
3.  Adicione ACEs de objeto à DACL no descritor de segurança do objeto para conceder ou negar aos usuários ou grupos o direito de acesso de controle nesse objeto. Para obter mais informações, consulte [Configurando direitos de acesso em um objeto](setting-access-rights-on-an-object.md).
4.  Quando um usuário tenta executar a operação protegida, seu aplicativo ou serviço usa a função [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) para determinar se o direito de acesso de controle é concedido ao usuário. Para obter mais informações, consulte [Verificando um direito de acesso de controle na ACL de um objeto](checking-a-control-access-right-in-an-objectampaposs-acl.md).
5.  Com base no resultado da verificação de acesso no objeto, seu aplicativo ou serviço pode conceder ou negar ao usuário acesso ao aplicativo ou serviço.

Um aplicativo de serviço também pode criar um grupo cujos membros seriam as várias instâncias de serviço. Por exemplo, um serviço com instâncias instaladas em vários computadores em toda a empresa pode ter um arquivo de log comum que todas as instâncias de serviço escrevem. O programa de instalação do serviço cria o arquivo de log e usa uma DACL para conceder acesso somente a membros de um grupo. Os membros do grupo seriam as contas de usuário sob as quais as várias instâncias de serviço estão em execução ou, se os serviços são executados na conta LocalSystem, os membros seriam as contas de computador dos servidores host.

 

 