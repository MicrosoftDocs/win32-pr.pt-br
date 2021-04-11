---
description: Um aplicativo não pode alterar a lista de controle de acesso de um objeto, a menos que o aplicativo tenha os direitos de fazer isso.
ms.assetid: 5f710fd8-33de-47c0-a8b2-baf3008c4ed7
title: Direitos de acesso para objetos de Access-Token
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb6a62a8c1518dca30f2abbc4481fa5e11cf081
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296679"
---
# <a name="access-rights-for-access-token-objects"></a>Direitos de acesso para objetos de Access-Token

Um aplicativo não pode alterar a lista de controle de acesso de um objeto, a menos que o aplicativo tenha os direitos de fazer isso. Esses direitos são controlados por um descritor de segurança no token de acesso para o objeto. Para obter mais informações sobre segurança, consulte [modelo de controle de acesso](access-control-model.md).

Para obter ou definir o [descritor de segurança](security-descriptors.md) para um [*token de acesso*](/windows/desktop/SecGloss/a-gly), chame as funções [**GetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity) e [**SetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity) .

Quando você chama a função [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) ou [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) para obter um identificador para um token de acesso, o sistema verifica os [direitos de acesso](access-rights-and-access-masks.md) solicitados em relação à DACL no descritor de segurança do token.

Estes são os direitos de acesso válidos para objetos Access-token:

-   Os direitos de acesso padrão de exclusão, controle de leitura \_ , gravação de \_ DAC e gravar \_ proprietário. [](standard-access-rights.md) Tokens de acesso não dão suporte ao direito de sincronização de acesso padrão.
-   O [ \_ direito de \_ segurança do sistema de acesso](sacl-access-right.md) para obter ou definir a SACL no descritor de segurança do objeto.
-   Os direitos de acesso específicos para tokens de acesso, que são listados na tabela a seguir.

    | Valor                     | Significado                                                                                                                                                                                                                                                                           |
    |---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | \_padrão de ajuste de token \_    | Necessário para alterar o proprietário padrão, o grupo primário ou a DACL de um token de acesso.                                                                                                                                                                                                  |
    | \_grupos de ajuste de token \_     | Necessário para ajustar os atributos dos grupos em um token de acesso.                                                                                                                                                                                                               |
    | \_privilégios de ajuste de token \_ | Necessário para habilitar ou desabilitar os privilégios em um token de acesso.                                                                                                                                                                                                                  |
    | ID do TOKEN de \_ ajuste \_  | Necessário para ajustar a ID de sessão de um token de acesso. O \_ privilégio de nome TCB de se \_ é necessário.                                                                                                                                                                                    |
    | \_atribuição \_ primária de token    | Necessário para anexar um [*token primário*](/windows/desktop/SecGloss/p-gly) a um [*processo*](/windows/desktop/SecGloss/p-gly). O \_ privilégio de \_ nome ASSIGNPRIMARYTOKEN se também é necessário para realizar essa tarefa. |
    | TOKEN \_ duplicado          | Necessário para duplicar um token de acesso.                                                                                                                                                                                                                                            |
    | execução do TOKEN \_            | Combina a \_ \_ execução de direitos padrão e a representação de token \_ .                                                                                                                                                                                                                        |
    | representação de TOKEN \_        | Necessário para anexar um token de acesso de representação a um processo.                                                                                                                                                                                                                    |
    | consulta de TOKEN \_              | Necessário para consultar um token de acesso.                                                                                                                                                                                                                                                |
    | \_origem da consulta de token \_      | Necessário para consultar a origem de um token de acesso.                                                                                                                                                                                                                                  |
    | leitura de TOKEN \_               | Combina a \_ \_ consulta de token e leitura de direitos padrão \_ .                                                                                                                                                                                                                                 |
    | gravação de TOKEN \_              | Combina \_ \_ gravação de direitos padrão, privilégios de ajuste de token \_ \_ , grupos de ajuste de token \_ \_ e padrão de ajuste de token \_ \_ .                                                                                                                                                                   |
    | \_todo o \_ acesso ao token        | Combina todos os direitos de acesso possíveis para um token.                                                                                                                                                                                                                                  |

    

     

 

 
