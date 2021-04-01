---
description: Um token restrito é um token de acesso primário ou de representação que foi modificado pela função CreateRestrictedToken.
ms.assetid: 06580ab9-ff58-4aa9-bf88-9536a2e1981d
title: Tokens restritos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fee8e6c89915e3edd0a9206f84a0d3d5697a3cb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090752"
---
# <a name="restricted-tokens"></a>Tokens restritos

Um token restrito é um [*token de acesso*](/windows/desktop/SecGloss/a-gly) [*primário*](/windows/desktop/SecGloss/p-gly) ou de representação que foi modificado pela função [**CreateRestrictedToken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) . Um [*processo*](/windows/desktop/SecGloss/p-gly) ou representação de threads em execução no [*contexto de segurança*](/windows/desktop/SecGloss/s-gly) de um token restrito é restrito em sua capacidade de acessar objetos protegíveis ou executar operações privilegiadas. A função **CreateRestrictedToken** pode restringir um token das seguintes maneiras:

-   Remova os [privilégios](privileges.md) do token.
-   Aplique o atributo somente negação a SIDs no token para que eles não possam ser usados para acessar objetos protegidos. Para obter mais informações sobre o atributo somente negado, consulte [atributos de Sid em um token de acesso](sid-attributes-in-an-access-token.md).
-   Especifique uma lista de SIDs de restrição, que podem limitar o acesso a objetos protegíveis.

O sistema usa a lista de SIDs de restrição quando verifica o acesso do token a um objeto protegível. Quando um processo ou thread restrito tenta acessar um objeto protegível, o sistema executa duas verificações de acesso: uma usando os SIDs habilitados do token e outra usando a lista de SIDs de restrição. O acesso será concedido somente se ambas as verificações de acesso permitirem os direitos de acesso solicitados. Para obter mais informações sobre verificações de acesso, consulte [como as DACLs controlam o acesso a um objeto](how-dacls-control-access-to-an-object.md).

Você pode usar um [*token primário*](/windows/desktop/SecGloss/p-gly) restrito em uma chamada para a função [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) . Normalmente, o processo que chama **CreateProcessAsUser** deve ter o \_ privilégio de \_ nome ASSIGNPRIMARYTOKEN se, que geralmente é mantido apenas pelo código do sistema ou por serviços em execução na conta LocalSystem. No entanto, se a chamada **CreateProcessAsUser** especificar uma versão restrita do token primário do chamador, esse privilégio não será necessário. Isso permite que aplicativos comuns criem processos restritos.

Você também pode usar um [*token de representação*](/windows/desktop/SecGloss/i-gly) ou primário restrito na função [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) .

Para determinar se um token tem uma lista de SIDs de restrição, chame a função [**IsTokenRestricted**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-istokenrestricted) .

> [!Note]  
> Os aplicativos que usam tokens restritos devem executar o aplicativo restrito em desktops diferentes da área de trabalho padrão. Isso é necessário para evitar um ataque por um aplicativo restrito, usando **SendMessage** ou uma **mensagem** de erro, para aplicativos irrestritos na área de trabalho padrão. Se necessário, alterne entre áreas de trabalho para fins de aplicativo.

 

 

 
