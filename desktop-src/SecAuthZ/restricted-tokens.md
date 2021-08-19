---
description: Um token restrito é um token de acesso primário ou de representação que foi modificado pela função CreateRestrictedToken.
ms.assetid: 06580ab9-ff58-4aa9-bf88-9536a2e1981d
title: Tokens restritos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53f63402997d9e1304ca75ca117554ce52c3aa727f44b3b8316c28e1ecfcea45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118912004"
---
# <a name="restricted-tokens"></a>Tokens restritos

Um token restrito é um [*token*](/windows/desktop/SecGloss/a-gly) [*de*](/windows/desktop/SecGloss/p-gly) acesso primário ou de representação que foi modificado pela [**função CreateRestrictedToken.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) Um [*processo*](/windows/desktop/SecGloss/p-gly) ou thread de [](/windows/desktop/SecGloss/s-gly) representação em execução no contexto de segurança de um token restrito é restrito em sua capacidade de acessar objetos que podem sercuráveis ou executar operações privilegiadas. A **função CreateRestrictedToken** pode restringir um token das seguintes maneiras:

-   Remova [os privilégios](privileges.md) do token.
-   Aplique o atributo somente negação a SIDs no token para que eles não sejam usados para acessar objetos protegidos. Para obter mais informações sobre o atributo somente negação, consulte [Atributos SID em um Token de Acesso](sid-attributes-in-an-access-token.md).
-   Especifique uma lista de restrições de SIDs, que podem limitar o acesso a objetos de segurança.

O sistema usa a lista de restrições de SIDs quando verifica o acesso do token a um objeto que pode ser proteger. Quando um processo ou thread restrito tenta acessar um objeto que pode ser proteger, o sistema executa duas verificações de acesso: uma usando os SIDs habilitados do token e outra usando a lista de restrição de SIDs. O acesso será concedido somente se ambas as verificações de acesso permitirem os direitos de acesso solicitados. Para obter mais informações sobre verificações de acesso, consulte [How DACLs Control Access to an Object](how-dacls-control-access-to-an-object.md).

Você pode usar um [*token primário restrito*](/windows/desktop/SecGloss/p-gly) em uma chamada para a função [**CreateProcessAsUser.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) Normalmente, o processo que chama **CreateProcessAsUser** deve ter o privilégio ES \_ ASSIGNPRIMARYTOKEN NAME, que geralmente é mantido apenas pelo código do sistema ou por serviços em execução na conta \_ LocalSystem. No entanto, se a **chamada CreateProcessAsUser** especificar uma versão restrita do token primário do chamador, esse privilégio não será necessário. Isso permite que aplicativos comuns criem processos restritos.

Você também pode usar um token primário ou de representação [*restrito*](/windows/desktop/SecGloss/i-gly) na [**função ImpersonateLoggedOnUser.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser)

Para determinar se um token tem uma lista de RESTRIÇÕES, chame a [**função IsTokenRestricted.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-istokenrestricted)

> [!Note]  
> Aplicativos que usam tokens restritos devem executar o aplicativo restrito em áreas de trabalho diferentes da área de trabalho padrão. Isso é necessário para evitar um ataque por um aplicativo restrito, usando **SendMessage** ou **PostMessage**, para aplicativos irrestritos na área de trabalho padrão. Se necessário, alternar entre áreas de trabalho para fins de aplicativo.

 

 

 
