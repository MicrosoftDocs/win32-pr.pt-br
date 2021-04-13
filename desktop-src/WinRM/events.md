---
title: Eventos (Gerenciamento Remoto do Windows)
description: O serviço coletor de eventos usa o protocolo WS-Management para coletar eventos de computadores remotos.
ms.assetid: 5c8e0559-c576-4ac6-b636-c4a6fc399c9f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 06f96877904a5e76ea61a6b2f636e962e4dbd9b9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104369068"
---
# <a name="events-windows-remote-management"></a>Eventos (Gerenciamento Remoto do Windows)

O serviço coletor de eventos usa o protocolo WS-Management para coletar eventos de computadores remotos. Com o serviço coletor de eventos, você pode criar assinaturas para eventos do Windows em computadores remotos e eventos de hardware gerados por BMCs (controladores de gerenciamento da baseboard). BMCs deve dar suporte ao protocolo WS-Management.

Quando você cria uma assinatura, os eventos são encaminhados para o computador no qual a assinatura foi criada. Eles aparecerão na Visualizador de Eventos.

Os eventos de hardware gerados pela IPMI (interface de gerenciamento de plataforma inteligente) em computadores baseados no Windows são coletados localmente usando o driver IPMI e armazenados no log de eventos de hardware, após o qual eles podem ser encaminhados como outros eventos do sistema operacional Windows.

Você pode criar assinaturas usando a ferramenta de linha de comando Wecutil.exe. Para obter mais informações sobre como usar essa ferramenta, em um prompt de comando, digite **wecutil/?**. Para obter mais informações sobre o serviço coletor de eventos, consulte [coletor de eventos do Windows](/windows/desktop/WEC/windows-event-collector).

> [!Note]  
> As APIs de Gerenciamento Remoto do Windows exigem que todos os endereços IPv6 sejam colocados entre colchetes.

 

> [!Caution]
>
> Ao usar assinaturas iniciadas pelo coletor, limite o número de computadores remotos a 500 e isole o serviço [coletor de eventos do Windows](/windows/desktop/WEC/windows-event-collector) (Wecsvc) em um processo de host separado.
>
> Um erro de conexão manterá um thread até atingir o tempo limite. Um grande número de erros de conexão simultâneas pode causar esgotamento do pool de threads e renderizar o servidor sem resposta.

 

 

 
