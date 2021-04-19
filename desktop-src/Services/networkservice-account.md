---
description: A conta NetworkService é uma conta local predefinida usada pelo Gerenciador de controle de serviço.
ms.assetid: f90d9346-10ed-4eba-bae2-9a1f1e6dc6b7
title: Conta NetworkService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c319518dbe925a146882014211d131c30420a282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756144"
---
# <a name="networkservice-account"></a>Conta NetworkService

A conta NetworkService é uma conta local predefinida usada pelo Gerenciador de controle de serviço. Essa conta não é reconhecida pelo subsistema de segurança, portanto, você não pode especificar seu nome em uma chamada para a função [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) . Ele tem privilégios mínimos no computador local e atua como o computador na rede.

Essa conta pode ser especificada em uma chamada para as funções [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) e [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) . Observe que essa conta não tem uma senha, portanto, qualquer informação de senha que você fornecer nessa chamada será ignorada. Enquanto o subsistema de segurança localiza esse nome de conta, o SCM não oferece suporte a nomes localizados. Portanto, você receberá um nome localizado para essa conta da função [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) , mas o nome da conta deverá ser a Autoridade NT do \\ NetworkService quando você chamar **CreateService** ou **ChangeServiceConfig**, independentemente da localidade, ou pode ocorrer resultados inesperados.

Um serviço executado no contexto da conta NetworkService apresenta as credenciais do computador a servidores remotos. Por padrão, o token remoto contém SIDs para os grupos todos e usuários autenticados. O SID do usuário é criado a partir do valor de **RID do serviço de rede de segurança \_ \_ \_** .

A conta NetworkService tem sua própria subchave na chave do registro **HKEY \_ Users** . Portanto, a chave de registro **HKEY \_ Current \_ User** está associada à conta NetworkService.

A conta NetworkService tem os seguintes privilégios:

-   **Se \_ \_Nome do ASSIGNPRIMARYTOKEN** (desabilitado)
-   **Se \_ \_Nome da auditoria** (desabilitado)
-   **Se \_ ALTERAR \_ \_ nome da notificação** (habilitado)
-   **Se \_ CRIAR \_ \_ nome global** (habilitado)
-   **Se \_ REPRESENTAR \_ nome** (habilitado)
-   **Se \_ AUMENTAR \_ o \_ nome da cota** (desabilitado)
-   **Se \_ \_Nome do DESligamento** (desabilitado)
-   **Se \_ Desencaixar \_ nome** (desabilitado)
-   Quaisquer privilégios atribuídos a usuários e usuários autenticados

Para obter mais informações, consulte [segurança de serviço e direitos de acesso](service-security-and-access-rights.md).

 

 
