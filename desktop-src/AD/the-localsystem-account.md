---
title: Usando a conta LocalSystem como uma conta de logon de serviço
description: Uma vantagem de ser executada na conta LocalSystem é que o serviço concluiu o acesso irrestrito aos recursos locais.
ms.assetid: 2bc2e16d-bd25-4ec6-91a2-8d03052df021
ms.tgt_platform: multiple
keywords:
- conta LocalSystem
- LocalSystem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bec3826984e28e29d3156b784da229f8e53e34e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915931"
---
# <a name="using-the-localsystem-account-as-a-service-logon-account"></a>Usando a conta LocalSystem como uma conta de logon de serviço

Uma vantagem de ser executada na conta LocalSystem é que o serviço concluiu o acesso irrestrito aos recursos locais. Isso também é a desvantagem do LocalSystem porque um serviço LocalSystem pode fazer coisas que desativariam todo o sistema. Em particular, um serviço em execução como LocalSystem em um DC (controlador de domínio) tem acesso irrestrito ao Active Directory Domain Services. Isso significa que os bugs no serviço ou ataques de segurança no serviço podem danificar o sistema ou, se o serviço estiver em um controlador de domínio, danificar toda a rede corporativa.

Por esses motivos, os administradores de domínio em instalações confidenciais terão cuidado ao permitir que os serviços sejam executados como LocalSystem. Na verdade, eles podem ter políticas em relação a ele, especialmente em DCs. Se o seu serviço deve ser executado como LocalSystem, a documentação do seu serviço deve justificar aos administradores de domínio os motivos para conceder ao serviço o direito de execução em privilégios elevados. Os serviços nunca devem ser executados como LocalSystem em um controlador de domínio. Para obter mais informações e um exemplo de código que mostra como um serviço ou instalador de serviço pode determinar se está em execução em um controlador de domínio, consulte [testando se em execução em um controlador de domínio](testing-whether-running-on-a-domain-controller.md).

Quando um serviço é executado na conta LocalSystem em um computador que é membro do domínio, o serviço tem qualquer acesso à rede concedido à conta do computador ou a qualquer grupo do qual a conta do computador seja membro. Lembre-se de que, no Windows 2000, uma conta de computador de domínio é uma entidade de serviço, semelhante a uma conta de usuário. Isso significa que uma conta de computador pode estar em um grupo de segurança e uma ACE em um descritor de segurança pode conceder acesso a uma conta de computador. Lembre-se de que a adição de contas de computador a grupos não é recomendada por dois motivos:

-   As contas de computador estão sujeitas à exclusão e à recriação se o computador sair e, em seguida, ingressar novamente no domínio.
-   Se você adicionar uma conta de computador a um grupo, todos os serviços em execução como LocalSystem nesse computador terão permissão para acessar os direitos de acesso do grupo. Isso ocorre porque todos os serviços LocalSystem compartilham a conta de computador de seu servidor host. Por esse motivo, é particularmente importante que as contas de computador não sejam membros de nenhum grupo de administradores de domínio.

As contas de computador normalmente têm poucos privilégios e não pertencem a grupos. A proteção de ACL padrão no Active Directory Domain Services permite o acesso mínimo para contas de computador. Consequentemente, os serviços executados como LocalSystem, em computadores que não sejam DCs, têm apenas acesso mínimo ao Active Directory Domain Services.

Se o serviço for executado em LocalSystem, você deverá testar seu serviço em um servidor membro para garantir que o serviço tenha direitos suficientes para ler/gravar em controladores de Domínio do Active Directory. Um controlador de domínio não deve ser o único computador Windows no qual você testa seu serviço. Lembre-se de que um serviço em execução no LocalSystem em um controlador de domínio do Windows tem acesso completo ao Active Directory Domain Services e que um servidor membro é executado no contexto da conta do computador que tem substancialmente menos direitos.

 

 




