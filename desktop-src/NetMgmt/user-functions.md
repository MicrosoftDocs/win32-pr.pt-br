---
title: Funções de usuário
description: As funções de usuário de gerenciamento de rede controlam a conta de um usuário no banco de dados de segurança, que é o banco de dados SAM (Gerenciador de contas de segurança) ou, no caso de controladores de domínio, o Active Directory. As funções de usuário são listadas a seguir.
ms.assetid: cf0e5102-3924-46c0-8124-0aa04e95f48d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6a3349673d09e42fbfe7a5dc949d1bcff53b828
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105779604"
---
# <a name="user-functions"></a>Funções de usuário

As funções de usuário de gerenciamento de rede controlam a conta de um usuário no banco de dados de segurança, que é o banco de dados SAM (Gerenciador de contas de segurança) ou, no caso de controladores de domínio, o Active Directory. As funções de usuário são listadas a seguir.



| Função                                               | Descrição                                                         |
|--------------------------------------------------------|---------------------------------------------------------------------|
| [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd)                       | Adiciona uma conta de usuário e atribui um nível de senha e de privilégio.     |
| [**NetUserChangePassword**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserchangepassword) | Altera a senha de um usuário para um domínio ou servidor de rede especificado. |
| [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel)                       | Exclui uma conta de usuário do servidor.                             |
| [**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum)                     | Lista todas as contas de usuário em um servidor.                                |
| [**NetUserGetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups)           | Retorna uma lista de nomes de grupos globais aos quais um usuário pertence.       |
| [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo)               | Retorna informações sobre uma conta de usuário específica em um servidor.    |
| [**NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups) | Retorna uma lista de nomes de grupos locais aos quais um usuário pertence.        |
| [**NetUserSetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetgroups)           | Define associações de grupo global para uma conta de usuário especificada.         |
| [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo)               | Define a senha e outros elementos de uma conta de usuário.             |



 

Cada usuário ou aplicativo que acessa recursos de rede deve ter uma conta no banco de dados de segurança. Os serviços de diretório usam essa conta para verificar se o usuário ou aplicativo tem permissão para se conectar a um recurso. Quando um usuário ou um aplicativo solicita acesso a um recurso, o sistema de segurança do Windows verifica uma conta de usuário ou conta de grupo apropriada para permitir o acesso.

Depois de remover uma conta de usuário chamando a função [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel) , o usuário não poderá mais acessar o servidor, exceto usando a conta de convidado.

Como a senha de um usuário é confidencial, ela não é retornada pela função [**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum) ou pela função [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo) . A senha é atribuída inicialmente quando você chama [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd).

As informações de conta de usuário estão disponíveis nos seguintes níveis:

-   [**Informações do usuário \_ \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_0)
-   [**Informações do usuário \_ \_ 1**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1)
-   [**Informações do usuário \_ \_ 2**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_2)
-   [**Informações do usuário \_ \_ 3**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_3)
-   [**Informações do usuário \_ \_ 4**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_4)
-   [**Informações do usuário \_ \_ 10**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_10)
-   [**Informações do usuário \_ \_ 11**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_11)
-   [**Informações do usuário \_ \_ 20**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_20)
-   [**Informações do usuário \_ \_ 21**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_21)
-   [**Informações do usuário \_ \_ 22**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_22)
-   [**Informações do usuário \_ \_ 23**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_23)

Além disso, os seguintes níveis de informações são válidos quando você chama a função [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) :

-   [**Informações do usuário \_ \_ 1003**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1003)
-   [**Informações do usuário \_ \_ 1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1005)
-   [**Informações do usuário \_ \_ 1006**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1006)
-   [**Informações do usuário \_ \_ 1007**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1007)
-   [**Informações do usuário \_ \_ 1008**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1008)
-   [**Informações do usuário \_ \_ 1009**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1009)
-   [**Informações do usuário \_ \_ 1010**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1010)
-   [**Informações do usuário \_ \_ 1011**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1011)
-   [**Informações do usuário \_ \_ 1012**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1012)
-   [**Informações do usuário \_ \_ 1014**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1014)
-   [**Informações do usuário \_ \_ 1017**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1017)
-   [**Informações do usuário \_ \_ 1020**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1020)
-   [**Informações do usuário \_ \_ 1024**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1024)
-   [**Informações do usuário \_ \_ 1051**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1051)
-   [**Informações do usuário \_ \_ 1052**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1052)
-   [**Informações do usuário \_ \_ 1053**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1053)

As funções a seguir permitem que os aplicativos verifiquem a conformidade com a senha.



| Função                                                               | Descrição                                                                                                |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**NetValidatePasswordPolicyFree**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicyfree) | Libera a memória alocada pela função [**NetValidatePasswordPolicy**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicy) . |
| [**NetValidatePasswordPolicy**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicy)         | Verifica se as senhas atendem à complexidade, à duração, ao comprimento mínimo e aos requisitos de reutilização de histórico.            |



 

Se você estiver programando para Active Directory, poderá chamar determinados métodos da interface de serviço Active Directory (ADSI) para obter a mesma funcionalidade que pode obter ao chamar as funções de usuário de gerenciamento de rede. Para obter mais informações, consulte [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) e [**IADsComputer**](/windows/desktop/api/iads/nn-iads-iadscomputer).

 

 