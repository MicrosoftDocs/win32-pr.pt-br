---
title: Eventos (Windows Gerenciamento Remoto)
description: O serviço Coletor de Eventos usa o protocolo WS-Management para coletar eventos de computadores remotos.
ms.assetid: 5c8e0559-c576-4ac6-b636-c4a6fc399c9f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e081a0f4a5cea3f0ecac782a1dc5b07d3eae2160866f2582377a0e5e750f2133
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993796"
---
# <a name="events-windows-remote-management"></a>Eventos (Windows Gerenciamento Remoto)

O serviço Coletor de Eventos usa o protocolo WS-Management para coletar eventos de computadores remotos. Com o serviço Coletor de Eventos, você pode criar assinaturas para Windows eventos em computadores remotos e eventos de hardware gerados por BMCs (controladores de gerenciamento de placa base). Os BMCs devem dar suporte ao WS-Management protocolo.

Quando você cria uma assinatura, os eventos são encaminhados para o computador no qual a assinatura foi criada. Eles aparecerão na Visualizador de Eventos.

Os eventos de hardware gerados pelo IPMI (Intelligent Platform Management Interface) em computadores baseados em Windows são coletados localmente usando o driver IPMI e armazenados no log de Eventos de Hardware, após os quais eles podem ser encaminhados como outros eventos Windows do sistema operacional.

Você pode criar assinaturas usando a Wecutil.exe de linha de comando. Para obter mais informações sobre como usar essa ferramenta, em um prompt de comando, digite **wecutil /?**. Para obter mais informações sobre o serviço Coletor de Eventos, [consulte Windows Coletor de Eventos](/windows/desktop/WEC/windows-event-collector).

> [!Note]  
> Windows As APIs de Gerenciamento Remoto exigem que todos os endereços IPv6 sejam incluídos entre colchetes.

 

> [!Caution]
>
> Ao usar assinaturas iniciadas pelo coletor, limite o número de [](/windows/desktop/WEC/windows-event-collector) computadores remotos a 500 e isole o serviço coletor de eventos Windows (wecsvc) em um processo de host separado.
>
> Um erro de conexão conterá um thread até que o tempo passe. Um grande número de erros de conexão simultânea pode causar esgotamento do pool de threads e deixar o servidor sem resposta.

 

 

 
