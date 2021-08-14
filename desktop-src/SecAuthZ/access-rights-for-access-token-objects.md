---
description: Um aplicativo não pode alterar a lista de controle de acesso de um objeto, a menos que o aplicativo tenha direitos para fazer isso.
ms.assetid: 5f710fd8-33de-47c0-a8b2-baf3008c4ed7
title: Direitos de acesso para Access-Token objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac3145aef5fcf3a20f2569ac02df0de0638c2be1f42f5e1a74785d8ae1aedb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785462"
---
# <a name="access-rights-for-access-token-objects"></a>Direitos de acesso para Access-Token objetos

Um aplicativo não pode alterar a lista de controle de acesso de um objeto, a menos que o aplicativo tenha direitos para fazer isso. Esses direitos são controlados por um descritor de segurança no token de acesso do objeto. Para obter mais informações sobre segurança, consulte [Modelo de Controle de Acesso](access-control-model.md).

Para obter ou definir o [descritor de](security-descriptors.md) segurança para um [*token*](/windows/desktop/SecGloss/a-gly)de acesso, chame as funções [**GetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity) e [**SetKernelObjectSecurity.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity)

Quando você chama a função [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) ou [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) para obter um handle [](access-rights-and-access-masks.md) para um token de acesso, o sistema verifica os direitos de acesso solicitados em relação à DACL no descritor de segurança do token.

A seguir estão os direitos de acesso válidos para objetos de token de acesso:

-   Os direitos de acesso padrão DELETE, READ \_ CONTROL, WRITE DAC e \_ WRITE OWNER \_ . [](standard-access-rights.md) Os tokens de acesso não são suportados pelo direito de acesso padrão SYNCHRONIZE.
-   O [direito ACCESS SYSTEM \_ \_ SECURITY](sacl-access-right.md) para obter ou definir a SACL no descritor de segurança do objeto.
-   Os direitos de acesso específicos para tokens de acesso, que são listados na tabela a seguir.

    | Valor                     | Significado                                                                                                                                                                                                                                                                           |
    |---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | PADRÃO \_ DE AJUSTE DE \_ TOKEN    | Necessário para alterar o proprietário padrão, grupo primário ou DACL de um token de acesso.                                                                                                                                                                                                  |
    | GRUPOS \_ DE AJUSTE DE \_ TOKEN     | Necessário para ajustar os atributos dos grupos em um token de acesso.                                                                                                                                                                                                               |
    | PRIVILÉGIOS \_ DE AJUSTE DE \_ TOKEN | Necessário para habilitar ou desabilitar os privilégios em um token de acesso.                                                                                                                                                                                                                  |
    | AJUSTAR \_ \_ SESSIONID DO TOKEN  | Necessário para ajustar a ID de sessão de um token de acesso. O ES \_ TCB \_ NAME é necessário.                                                                                                                                                                                    |
    | TOKEN \_ ASSIGN \_ PRIMARY    | Necessário para anexar um [*token primário*](/windows/desktop/SecGloss/p-gly) a um [*processo*](/windows/desktop/SecGloss/p-gly). O ES \_ privilégio ASSIGNPRIMARYTOKEN \_ NAME também é necessário para realizar essa tarefa. |
    | TOKEN \_ DUPLICADO          | Necessário para duplicar um token de acesso.                                                                                                                                                                                                                                            |
    | TOKEN \_ EXECUTE            | O mesmo que \_ RIGHTS \_ EXECUTE PADRÃO.                                                                                                                                                                                                                                                |
    | REPRESENTAÇÃO \_ DE TOKEN        | Necessário para anexar um token de acesso de representação a um processo.                                                                                                                                                                                                                    |
    | CONSULTA \_ DE TOKEN              | Necessário para consultar um token de acesso.                                                                                                                                                                                                                                                |
    | ORIGEM \_ DA CONSULTA DE \_ TOKEN      | Necessário para consultar a origem de um token de acesso.                                                                                                                                                                                                                                  |
    | LEITURA \_ DE TOKEN               | Combina A CONSULTA DE TOKEN e \_ \_ LEITURA DE DIREITOS \_ PADRÃO.                                                                                                                                                                                                                                 |
    | GRAVAÇÃO \_ DE TOKEN              | Combina A GRAVAÇÃO \_ DE DIREITOS \_ PADRÃO, PRIVILÉGIOS DE AJUSTE DE \_ \_ TOKEN, GRUPOS DE AJUSTE DE TOKEN \_ E PADRÃO DE AJUSTE DE \_ \_ \_ TOKEN.                                                                                                                                                                   |
    | TOKEN \_ TODO \_ O ACESSO        | Combina todos os direitos de acesso possíveis para um token.                                                                                                                                                                                                                                  |

    

     

 

 
