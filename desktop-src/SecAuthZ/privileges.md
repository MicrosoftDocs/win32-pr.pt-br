---
description: Um privilégio é o direito de uma conta, como uma conta de usuário ou grupo, para executar várias operações relacionadas ao sistema no computador local, como desligar o sistema, carregar drivers de dispositivo ou alterar a hora do sistema.
ms.assetid: fe6aae0f-93eb-4aba-a6ac-45e71c251c51
title: Privilégios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cccedffdf5786da07dd2cfd77c3de428ee15ba94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921048"
---
# <a name="privileges"></a>Privilégios

Um [*privilégio*](/windows/desktop/SecGloss/p-gly) é o direito de uma conta, como uma conta de usuário ou grupo, para executar várias operações relacionadas ao sistema no computador local, como desligar o sistema, carregar drivers de dispositivo ou alterar a hora do sistema. Os privilégios diferem dos direitos de acesso de duas maneiras:

-   Os privilégios controlam o acesso a recursos do sistema e tarefas relacionadas ao sistema, enquanto os direitos de acesso controlam o acesso a [objetos protegíveis](securable-objects.md).
-   Um administrador de sistema atribui privilégios a contas de usuário e de grupo, enquanto o sistema concede ou nega acesso a um objeto protegível com base nos direitos de acesso concedidos nas ACEs na DACL do objeto.

Cada sistema tem um banco de dados de conta que armazena os privilégios mantidos por contas de usuário e de grupo. Quando um usuário faz logon, o sistema produz um [token de acesso](access-tokens.md) que contém uma lista de privilégios do usuário, incluindo aqueles concedidos ao usuário ou a grupos aos quais o usuário pertence. Observe que os privilégios se aplicam somente ao computador local; uma conta de domínio pode ter privilégios diferentes em computadores diferentes.

Quando o usuário tenta executar uma operação privilegiada, o sistema verifica o token de acesso do usuário para determinar se o usuário tem os privilégios necessários e, nesse caso, verifica se os privilégios estão habilitados. Se o usuário falhar nesses testes, o sistema não executará a operação.

Para determinar os privilégios mantidos em um token de acesso, chame a função [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) , que também indica quais privilégios estão habilitados. A maioria dos privilégios está desabilitada por padrão.

A API do Windows define um conjunto de constantes de cadeia de caracteres, como \_ ASSIGNPRIMARYTOKEN \_ Name, para identificar os vários privilégios. Essas constantes são as mesmas em todos os sistemas e são definidas em Winnt. h. Para obter uma tabela dos privilégios definidos pelo Windows, consulte [constantes de privilégio](authorization-constants.md). No entanto, as funções que obtêm e ajustam os privilégios em um token de acesso usam o tipo de [**LUID**](/windows/desktop/api/Winnt/ns-winnt-luid) para identificar privilégios. Os valores de **LUID** de um privilégio podem ser diferentes de um computador para outro e de uma inicialização para outra no mesmo computador. Para obter o **LUID** atual que corresponde a uma das constantes de cadeia de caracteres, use a função [**LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) . Use a função [**LookupPrivilegeName**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegenamea) para converter um **LUID** em sua constante de cadeia de caracteres correspondente.

O sistema fornece um conjunto de nomes de exibição que descrevem cada um dos privilégios. Eles são úteis quando você precisa exibir uma descrição de um privilégio para o usuário. Use a função [**LookupPrivilegeDisplayName**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegedisplaynamea) para recuperar uma cadeia de caracteres de descrição que corresponda à constante de cadeia de caracteres para um privilégio. Por exemplo, em sistemas que usam inglês americano, o nome de exibição para o \_ privilégio de nome SYSTEMTIME se \_ é "alterar a hora do sistema".

Você pode usar a função [**PrivilegeCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-privilegecheck) para determinar se um token de acesso contém um conjunto especificado de privilégios. Isso é útil principalmente para aplicativos de servidor que estão representando um cliente.

Um administrador de sistema pode usar ferramentas administrativas, como o Gerenciador de usuários, para adicionar ou remover privilégios para contas de usuário e de grupo. Os administradores podem usar programaticamente as funções de [*autoridade de segurança local*](/windows/desktop/SecGloss/l-gly) (LSA) para trabalhar com privilégios. As funções [**LsaAddAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaaddaccountrights) e [**LsaRemoveAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaremoveaccountrights) adicionam ou removem privilégios de uma conta. A função [**LsaEnumerateAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumerateaccountrights) enumera os privilégios mantidos por uma conta especificada. A função [**LsaEnumerateAccountsWithUserRight**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright) enumera as contas que mantêm um privilégio especificado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes de autorização](authorization-constants.md)
</dt> <dt>

[Habilitando e desabilitando privilégios em C++](enabling-and-disabling-privileges-in-c--.md)
</dt> </dl>

 

 
