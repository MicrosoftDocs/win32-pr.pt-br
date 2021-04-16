---
description: A conta LocalService é uma conta local predefinida usada pelo Gerenciador de controle de serviço.
ms.assetid: 5409e2fe-a349-4739-a481-f8a35fd3c9b4
title: Conta do LocalService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d67051b95d6e5d18179bb2dc69928e68edb0f3e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506132"
---
# <a name="localservice-account"></a>Conta do LocalService

A conta LocalService é uma conta local predefinida usada pelo Gerenciador de controle de serviço. Ele tem privilégios mínimos no computador local e apresenta credenciais anônimas na rede.

Essa conta pode ser especificada em uma chamada para as funções [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) e [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) . Observe que essa conta não tem uma senha, portanto, qualquer informação de senha que você fornecer nessa chamada será ignorada. Enquanto o subsistema de segurança localiza esse nome de conta, o SCM não oferece suporte a nomes localizados. Portanto, você receberá um nome localizado para essa conta da função [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) , mas o nome da conta deverá ser a Autoridade NT \\ LocalService quando você chamar **CreateService** ou **ChangeServiceConfig**, independentemente da localidade, ou podem ocorrer resultados inesperados.

O SID de usuário é criado com base no valor de **\_ \_ \_ RID do serviço local de segurança** .

A conta LocalService tem sua própria subchave na chave do registro **HKEY \_ Users** . Portanto, a chave de registro **HKEY \_ Current \_ User** está associada à conta LocalService.

A conta LocalService tem os seguintes privilégios:

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

 

 
