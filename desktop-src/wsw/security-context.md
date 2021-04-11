---
title: Contexto de segurança
description: Os contextos de segurança habilitam o estabelecimento de um contexto de segurança de mensagem de acordo com o WS-SecureConversation.
ms.assetid: bea92650-21bd-41d4-9dba-043d6779d85f
keywords:
- Contexto de segurança nativo-Web-Services
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cff86ea12ae7a4b8bd554e25cde534cba3b4dcb4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104294611"
---
# <a name="security-context"></a>Contexto de segurança

Os contextos de segurança habilitam o estabelecimento de um contexto de segurança de mensagem de acordo com o WS-SecureConversation. Esse contexto pode, então, ser usado para proteger mensagens como uma alternativa para a segurança de uma imagem em que as credenciais são transmitidas para cada solicitação. O contexto de segurança estabelecido é um método mais eficiente de proteger mensagens quando várias mensagens são trocadas.


Contextos de segurança exigem a presença de credenciais de segurança de bootstrap que são usadas para proteger as mensagens enviadas no contexto. A associação de [**\_ \_ segurança de \_ mensagem \_ \_ APREQ do WS Kerberos**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding), [**Associação de \_ segurança de \_ \_ mensagem \_ \_ de token do WS XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding)e estruturas de associação de [**segurança de \_ \_ mensagem \_ \_ WS username**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) podem ser usadas para essa finalidade.

Os contextos de segurança são um recurso de segurança de mensagem e são configurados por meio de associações de segurança de mensagem.

## <a name="client"></a>Cliente

No lado do cliente, o contexto de segurança é vinculado a um canal específico. Ele é configurado usando a [**\_ Associação de \_ \_ segurança de \_ \_ mensagem de contexto de segurança do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding). O comportamento e o tempo de vida do contexto são determinados pelo canal. Quando a primeira mensagem é enviada no canal, o contexto de segurança é estabelecido. Depois disso, o contexto é renovado proativamente em um intervalo configurável. Se o servidor retornar uma falha indicando que o contexto requer renovação, o contexto será renovado quando a próxima mensagem for enviada. Se o canal estiver no estado aberto, o contexto será cancelado por uma mensagem de cancelamento quando o canal for fechado.

## <a name="server"></a>Servidor

No servidor, um contexto de segurança é configurado da mesma maneira que no cliente. No entanto, ele não está vinculado a nenhum canal específico. Em vez disso, todos os canais criados para o ouvinte que tem o conjunto de [**Associação de segurança de mensagem de \_ contexto de segurança \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) são capazes de receber mensagens com qualquer um dos contextos de segurança que foram estabelecidos em canais desse ouvinte.

Quando uma mensagem chega em um canal que dá suporte a contextos de segurança, o contexto usado por essa mensagem pode ser obtido chamando-se a função [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) com o contexto de segurança de [**propriedade de \_ mensagem \_ \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id). O valor recuperado pode ser usado com [**WsRevokeSecurityContext**](/windows/desktop/api/WebServices/nf-webservices-wsrevokesecuritycontext) e [**WsGetSecurityContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritycontextproperty).

## <a name="metadata"></a>Metadados

A estrutura de restrição de associação de segurança de mensagem de contexto de segurança do WS é usada para extrair a política de contexto de segurança dos metadados. [**\_ \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint) Para obter mais informações, consulte [importação de metadados](metadata-import.md).

Os seguintes elementos de API são usados com contextos de segurança.

| Enumeração                                                                    | Descrição                                         |
|--------------------------------------------------------------------------------|-----------------------------------------------------|
| [**\_ID da \_ Propriedade do contexto de segurança WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_context_property_id) | Identifica uma propriedade de um objeto de contexto de segurança. |



 



| Função                                                             | Descrição                                        |
|----------------------------------------------------------------------|----------------------------------------------------|
| [**WsGetSecurityContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritycontextproperty) | Obtém uma propriedade do contexto de segurança especificado. |
| [**WsRevokeSecurityContext**](/windows/desktop/api/WebServices/nf-webservices-wsrevokesecuritycontext)           | Revoga um contexto de segurança.                        |



 



| Handle                                           | Descrição                                                 |
|--------------------------------------------------|-------------------------------------------------------------|
| [\_contexto de segurança do WS \_](ws-security-context.md) | Um tipo opaco usado para fazer referência a um objeto de contexto de segurança. |



 



| Estrutura                                                               | Descrição                                                               |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [**\_propriedade de \_ contexto de segurança WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_property) | Define uma propriedade de um [ \_ \_ contexto de segurança do WS](ws-security-context.md). |



 

 

 




