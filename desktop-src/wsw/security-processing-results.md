---
title: Resultados do processamento de segurança
description: Em um canal seguro, somente as mensagens que passam com êxito pelas verificações de segurança são entregues ao aplicativo.
ms.assetid: 891e1f91-406e-4997-9da6-59b5fe578d0d
keywords:
- O processamento de segurança resulta em serviços Web para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f53009729b3d7f1c8ff6b9e38a054d8dbadf202b7a0caa4a92c7861232c8390a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962925"
---
# <a name="security-processing-results"></a>Resultados do processamento de segurança

Em um canal seguro, somente as mensagens que passam com êxito pelas verificações de segurança são entregues ao aplicativo. Para essas mensagens, alguns resultados da verificação de segurança são anexados como propriedades de mensagem, e o aplicativo pode extrair e examinar essas propriedades para executar etapas adicionais, como verificações de autorização.


A função [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) pode ser usada para recuperar qualquer uma das propriedades relacionadas à segurança definidas na [**\_ ID da \_ propriedade \_ da mensagem do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id). **WsGetMessageProperty** retorna um erro para consultas que solicitam Propriedades de segurança não aplicáveis ao tipo de segurança usado no canal. A mensagem continua a possuir as propriedades retornadas pela função de consulta.

Os seguintes elementos de API são usados com resultados de processamento de segurança.

| Enumeração                                                                | Descrição                                                                                 |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**\_ID da \_ Propriedade do token de segurança do WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_token_property_id) | Define as chaves para os campos e propriedades que podem ser extraídas de um token de segurança. |



 



| Função                                                         | Descrição                                           |
|------------------------------------------------------------------|-------------------------------------------------------|
| [**WsGetSecurityTokenProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritytokenproperty) | Extrai um campo ou uma propriedade de um token de segurança. |



 



| Handle                                       | Descrição                                     |
|----------------------------------------------|-------------------------------------------------|
| [\_token de segurança do WS \_](ws-security-token.md) | Um identificador opaco que representa um token de segurança. |



 

 

 




