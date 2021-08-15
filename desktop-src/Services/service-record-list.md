---
description: À medida que cada entrada de serviço é lida do banco de dados dos serviços instalados, o SCM cria um registro de serviço para o serviço.
ms.assetid: c0ee43e2-af9b-4578-9017-46a5ed50b938
title: Lista de registros de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ef0bdebed5e302b1dc59bea6494fd812ec506e7e6d2531634b2a6686b86bc98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888850"
---
# <a name="service-record-list"></a>Lista de registros de serviço

À medida que cada entrada de serviço é lida do banco de dados dos serviços instalados, o SCM cria um registro de serviço para o serviço. Um registro de serviço inclui:

-   Nome do serviço
-   Tipo de início (início automático ou início de demanda)
-   Status do serviço (consulte a estrutura de [**\_ status do serviço**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) ) <dl> Tipo  
    Estado atual  
    Códigos de controle aceitáveis  
    Código de saída  
    Dica de espera  
    </dl>
-   Pointer to dependency list

O nome de usuário e a senha de uma conta são especificados no momento em que o serviço é instalado. O SCM armazena o nome de usuário no registro e a senha em uma parte segura da autoridade de segurança local (LSA). O administrador do sistema pode criar contas com senhas que nunca expiram. Como alternativa, o administrador do sistema pode criar contas com senhas que expiram e gerenciam as contas alterando as senhas periodicamente.

O SCM mantém duas cópias da senha de uma conta de usuário, uma senha atual e uma senha de backup. A senha especificada na primeira vez em que o serviço está instalado é armazenada como a senha atual e a senha de backup não é inicializada. Quando o SCM tenta executar o serviço no contexto de segurança da conta de usuário, ele usa a senha atual. Se a senha atual for usada com êxito, ela também será salva como a senha de backup. Se a senha for modificada com a função [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) ou o utilitário do painel de controle de serviços, a nova senha será armazenada como a senha atual e a senha anterior será armazenada como a senha de backup. Se o SCM tentar iniciar o serviço e a senha atual falhar, ele usará a senha de backup. Se a senha de backup for usada com êxito, ela será salva como a senha atual.

O SCM atualiza o status do serviço quando um serviço envia notificações de status usando a função [**falha em SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) . O SCM mantém o status de um serviço de driver consultando o sistema de e/s, em vez de receber notificações de status, como faz de um serviço.

Um serviço pode registrar informações de tipo adicionais chamando a função [**SetServiceBits**](/windows/desktop/api/Lmserver/nf-lmserver-setservicebits) . As funções [**NetServerGetInfo**](/windows/desktop/api/lmserver/nf-lmserver-netservergetinfo) e [**NetServerEnum**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum) obtêm os tipos de serviço com suporte.

 

 
