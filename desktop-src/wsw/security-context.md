---
title: Contexto de segurança
description: Os contextos de segurança permitem o estabelecimento de um contexto de segurança de mensagem de acordo com WS-SecureConversation.
ms.assetid: bea92650-21bd-41d4-9dba-043d6779d85f
keywords:
- Contexto de segurança Native-Web-Services
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06dc1754133f47cf06c5c12e7318a94525be3c821f3db52a7e7513349c3100be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083170"
---
# <a name="security-context"></a>Contexto de segurança

Os contextos de segurança permitem o estabelecimento de um contexto de segurança de mensagem de acordo com WS-SecureConversation. Esse contexto pode ser usado para proteger mensagens como uma alternativa à segurança única em que as credenciais são transmitidas para cada solicitação. O contexto de segurança estabelecido é um método mais eficiente de proteger mensagens quando várias mensagens são trocadas.


Os contextos de segurança exigem a presença de credenciais de segurança de inicialização que são usadas para proteger as mensagens enviadas no contexto. As [**estruturas WS \_ KERBEROS \_ APREQ \_ MESSAGE SECURITY \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding), [**WS XML TOKEN MESSAGE SECURITY \_ \_ \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding)e [**WS USERNAME MESSAGE SECURITY \_ \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) podem ser usadas para essa finalidade.

Os contextos de segurança são um recurso de segurança de mensagem e são configurados por meio de vinculações de segurança de mensagem.

## <a name="client"></a>Cliente

No lado do cliente, o contexto de segurança está vinculado a um canal específico. Ele é configurado usando a ASSOCIAÇÃO DE SEGURANÇA DE MENSAGEM DE CONTEXTO DE SEGURANÇA [**\_ \_ \_ \_ \_ do WS.**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) O comportamento e o tempo de vida do contexto são determinados pelo canal. Quando a primeira mensagem é enviada no canal, o contexto de segurança é estabelecido. Depois disso, o contexto é renovado proativamente em um intervalo configurável. Se o servidor retornar uma falha que indica que o contexto requer renovação, o contexto será renovado quando a próxima mensagem for enviada. Se o canal estiver no estado aberto, o contexto será cancelado por uma mensagem de cancelamento quando o canal for fechado.

## <a name="server"></a>Servidor

No servidor, um contexto de segurança é configurado da mesma maneira que no cliente. No entanto, ele não está vinculado a nenhum canal específico. Em vez disso, todos os canais criados para o ouvinte que tem o conjunto ASSOCIAÇÃO DE SEGURANÇA DE MENSAGEM DE CONTEXTO DE SEGURANÇA do WS são capazes de receber mensagens com qualquer um dos contextos de segurança que foram estabelecidos nos canais desse ouvinte. [**\_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding)

Quando uma mensagem chega em um canal que dá suporte a contextos de segurança, o contexto usado por essa mensagem pode ser obtido chamando a [**função WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) com o CONTEXTO DE SEGURANÇA DE PROPRIEDADE DE MENSAGEM do [**WS \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id). O valor recuperado pode ser usado com [**WsRevokeSecurityContext**](/windows/desktop/api/WebServices/nf-webservices-wsrevokesecuritycontext) e [**WsGetSecurityContextProperty.**](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritycontextproperty)

## <a name="metadata"></a>Metadados

A estrutura DE RESTRIÇÃO DE ASSOCIAÇÃO DE SEGURANÇA DE MENSAGEM DE CONTEXTO DE SEGURANÇA [**\_ \_ \_ \_ \_ \_ do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint) é usada para extrair a política de contexto de segurança dos metadados. Para obter mais informações, consulte [Importação de metadados.](metadata-import.md)

Os elementos de API a seguir são usados com contextos de segurança.

| Enumeração                                                                    | Descrição                                         |
|--------------------------------------------------------------------------------|-----------------------------------------------------|
| [**ID DA PROPRIEDADE \_ DE CONTEXTO DE SEGURANÇA \_ \_ \_ DO WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_context_property_id) | Identifica uma propriedade de um objeto de contexto de segurança. |



 



| Função                                                             | Descrição                                        |
|----------------------------------------------------------------------|----------------------------------------------------|
| [**WsGetSecurityContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritycontextproperty) | Obtém uma propriedade do contexto de segurança especificado. |
| [**WsRevokeSecurityContext**](/windows/desktop/api/WebServices/nf-webservices-wsrevokesecuritycontext)           | Revoga um contexto de segurança.                        |



 



| Handle                                           | Descrição                                                 |
|--------------------------------------------------|-------------------------------------------------------------|
| [CONTEXTO DE \_ SEGURANÇA DO WS \_](ws-security-context.md) | Um tipo opaco usado para referenciar um objeto de contexto de segurança. |



 



| Estrutura                                                               | Descrição                                                               |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [**PROPRIEDADE DE \_ CONTEXTO \_ DE SEGURANÇA DO WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_property) | Define uma propriedade de um [CONTEXTO DE \_ SEGURANÇA \_ do WS.](ws-security-context.md) |



 

 

 




