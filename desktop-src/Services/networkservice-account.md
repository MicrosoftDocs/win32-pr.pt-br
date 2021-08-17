---
description: A conta NetworkService é uma conta local predefinida usada pelo Gerenciador de controle de serviço.
ms.assetid: f90d9346-10ed-4eba-bae2-9a1f1e6dc6b7
title: Conta NetworkService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24f8256a15b43d9a9c0403067a61f9a7cbf6b9d2df0d78936c4d9c06f6dfd87c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889390"
---
# <a name="networkservice-account"></a>Conta NetworkService

A conta NetworkService é uma conta local predefinida usada pelo Gerenciador de controle de serviço. Essa conta não é reconhecida pelo subsistema de segurança, portanto, você não pode especificar seu nome em uma chamada para a função [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) . Ele tem privilégios mínimos no computador local e atua como o computador na rede.

Essa conta pode ser especificada em uma chamada para as funções [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) e [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) . Observe que essa conta não tem uma senha, portanto, qualquer informação de senha que você fornecer nessa chamada será ignorada. Enquanto o subsistema de segurança localiza esse nome de conta, o SCM não oferece suporte a nomes localizados. Portanto, você receberá um nome localizado para essa conta da função [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) , mas o nome da conta deverá ser a Autoridade NT do \\ NetworkService quando você chamar **CreateService** ou **ChangeServiceConfig**, independentemente da localidade, ou pode ocorrer resultados inesperados.

Um serviço executado no contexto da conta NetworkService apresenta as credenciais do computador a servidores remotos. Por padrão, o token remoto contém SIDs para os grupos todos e usuários autenticados. O SID do usuário é criado a partir do valor de **RID do serviço de rede de segurança \_ \_ \_** .

A conta NetworkService tem sua própria subchave na chave do registro **HKEY \_ Users** . Portanto, a chave de registro **HKEY \_ Current \_ User** está associada à conta NetworkService.

A conta NetworkService tem os seguintes privilégios:

-   **ES \_ \_Nome do ASSIGNPRIMARYTOKEN** (desabilitado)
-   **ES \_ \_Nome da auditoria** (desabilitado)
-   **ES \_ ALTERAR \_ \_ nome da notificação** (habilitado)
-   **ES \_ CRIAR \_ \_ nome global** (habilitado)
-   **ES \_ REPRESENTAR \_ nome** (habilitado)
-   **ES \_ AUMENTAR \_ o \_ nome da cota** (desabilitado)
-   **ES \_ \_Nome do DESligamento** (desabilitado)
-   **ES \_ Desencaixar \_ nome** (desabilitado)
-   Quaisquer privilégios atribuídos a usuários e usuários autenticados

Para obter mais informações, consulte [segurança de serviço e direitos de acesso](service-security-and-access-rights.md).

 

 
