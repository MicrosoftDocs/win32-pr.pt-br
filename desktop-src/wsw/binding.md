---
title: associação de canal
description: Associações especificam o protocolo de conexão e o comportamento local para um canal.
ms.assetid: 82d465c5-b23d-4403-b360-8c710fbc6e1c
keywords:
- Ligando serviços Web para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ae6e1b666f6b83915595f9fb138cc6ba2d81a434bbedd9871f27ba8fd6c6bbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026724"
---
# <a name="channel-binding"></a>associação de canal

Associações especificam o protocolo de conexão e o comportamento local para um canal. As associações são feitas dos seguintes componentes:

-   Uma [**\_ \_ associação do WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding), que identifica o protocolo de transferência a ser usado.
-   Uma [**\_ \_ Descrição de segurança do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description), que especifica como proteger o canal.
-   Um conjunto [**de \_ \_ Propriedades s do WS Channel**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property), que especificam configurações opcionais adicionais (consulte também [**ID de Propriedade do WS \_ Channel \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)).

 

 




