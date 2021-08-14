---
title: Funções de usuário
description: As funções de usuário de gerenciamento de rede controlam a conta de um usuário no banco de dados de segurança, que é o banco de dados SAM (gerenciador de contas de segurança) ou, no caso de controladores de domínio, o Active Directory. As funções de usuário são listadas a seguir.
ms.assetid: cf0e5102-3924-46c0-8124-0aa04e95f48d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34c8d7b59ff121c0225f166888b42ef1a731336ed80799cd0593ba38b4fb04ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796812"
---
# <a name="user-functions"></a>Funções de usuário

As funções de usuário de gerenciamento de rede controlam a conta de um usuário no banco de dados de segurança, que é o banco de dados SAM (gerenciador de contas de segurança) ou, no caso de controladores de domínio, o Active Directory. As funções de usuário são listadas a seguir.



| Função                                               | Descrição                                                         |
|--------------------------------------------------------|---------------------------------------------------------------------|
| [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd)                       | Adiciona uma conta de usuário e atribui um nível de senha e privilégio.     |
| [**NetUserChangePassword**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserchangepassword) | Altera a senha de um usuário para um servidor de rede ou domínio especificado. |
| [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel)                       | Exclui uma conta de usuário do servidor.                             |
| [**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum)                     | Lista todas as contas de usuário em um servidor.                                |
| [**NetUserGetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups)           | Retorna uma lista de nomes de grupo globais aos quais um usuário pertence.       |
| [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo)               | Retorna informações sobre uma conta de usuário específica em um servidor.    |
| [**NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups) | Retorna uma lista de nomes de grupo local aos quais um usuário pertence.        |
| [**NetUserSetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetgroups)           | Define associações de grupo global para uma conta de usuário especificada.         |
| [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo)               | Define a senha e outros elementos de uma conta de usuário.             |



 

Cada usuário ou aplicativo que acessa os recursos de rede deve ter uma conta no banco de dados de segurança. Os serviços de diretório usam essa conta para verificar se o usuário ou o aplicativo tem permissão para se conectar a um recurso. Quando um usuário ou um aplicativo solicita acesso a um recurso, o Windows de segurança verifica se há uma conta de usuário ou conta de grupo apropriada para permitir o acesso.

Depois de remover uma conta de usuário chamando a [**função NetUserDel,**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel) o usuário não poderá mais acessar o servidor, exceto usando a conta de convidado.

Como a senha de um usuário é confidencial, ela não é retornada pela função [**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum) ou pela [**função NetUserGetInfo.**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo) A senha é inicialmente atribuída quando você chama [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd).

As informações da conta de usuário estão disponíveis nos seguintes níveis:

-   [**INFORMAÇÕES \_ DO \_ USUÁRIO 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_0)
-   [**INFORMAÇÕES \_ DO USUÁRIO \_ 1**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1)
-   [**INFORMAÇÕES \_ DO USUÁRIO \_ 2**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_2)
-   [**INFORMAÇÕES \_ DO USUÁRIO \_ 3**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_3)
-   [**INFORMAÇÕES \_ DO USUÁRIO \_ 4**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_4)
-   [**INFORMAÇÕES \_ DO \_ USUÁRIO 10**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_10)
-   [**INFORMAÇÕES \_ DO \_ USUÁRIO 11**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_11)
-   [**INFORMAÇÕES \_ DO \_ USUÁRIO 20**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_20)
-   [**INFORMAÇÕES \_ DO USUÁRIO \_ 21**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_21)
-   [**INFORMAÇÕES \_ DO \_ USUÁRIO 22**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_22)
-   [**INFORMAÇÕES \_ DO USUÁRIO \_ 23**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_23)

Além disso, os seguintes níveis de informações são válidos quando você chama a [**função NetUserSetInfo:**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo)

-   [**INFORMAÇÕES \_ DO \_ USUÁRIO 1003**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1003)
-   [**INFORMAÇÕES \_ DO \_ USUÁRIO 1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1005)
-   [**INFORMAÇÕES \_ DO \_ USUÁRIO 1006**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1006)
-   [**INFORMAÇÕES \_ DO \_ USUÁRIO 1007**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1007)
-   [**INFORMAÇÕES \_ DO \_ USUÁRIO 1008**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1008)
-   [**INFORMAÇÕES \_ DO \_ USUÁRIO 1009**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1009)
-   [**INFORMAÇÕES \_ DO \_ USUÁRIO 1010**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1010)
-   [**INFORMAÇÕES \_ DO \_ USUÁRIO 1011**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1011)
-   [**INFORMAÇÕES \_ DO \_ USUÁRIO 1012**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1012)
-   [**INFORMAÇÕES \_ DO \_ USUÁRIO 1014**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1014)
-   [**INFORMAÇÕES \_ DO \_ USUÁRIO 1017**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1017)
-   [**INFORMAÇÕES \_ DO \_ USUÁRIO 1020**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1020)
-   [**INFORMAÇÕES \_ DO \_ USUÁRIO 1024**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1024)
-   [**INFORMAÇÕES \_ DO \_ USUÁRIO 1051**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1051)
-   [**INFORMAÇÕES \_ DO \_ USUÁRIO 1052**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1052)
-   [**INFORMAÇÕES \_ DO \_ USUÁRIO 1053**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1053)

As funções a seguir permitem que os aplicativos verifiquem a conformidade de senha.



| Função                                                               | Descrição                                                                                                |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**NetValidatePasswordPolicyFree**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicyfree) | Libera a memória alocada pela [**função NetValidatePasswordPolicy.**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicy) |
| [**NetValidatePasswordPolicy**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicy)         | Verifica se as senhas atendem aos requisitos de complexidade, de idade, de comprimento mínimo e de reutilização de histórico.            |



 

Se você estiver programando para o Active Directory, poderá chamar determinados métodos ADSI (Interface de Serviço do Active Directory) para obter a mesma funcionalidade que você pode obter chamando as funções de usuário de gerenciamento de rede. Para obter mais informações, [**consulte IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) [**e IADsComputer**](/windows/desktop/api/iads/nn-iads-iadscomputer).

 

 