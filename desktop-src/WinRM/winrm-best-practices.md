---
title: Práticas recomendadas do WinRM
description: Este tópico explica algumas das práticas recomendadas para usar os vários recursos da API do WinRM.
ms.assetid: FC2CD030-199F-43C2-804E-9827EA2A46D5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dc780ec299c3249006085d348d983f8dab5b76a462c991a2d3665fed7d18f123
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733796"
---
# <a name="winrm-best-practices"></a>Práticas recomendadas do WinRM

Este tópico explica algumas das práticas recomendadas para usar os vários recursos da API do WinRM.

## <a name="quotas"></a>Cotas

Quando uma cota é atingida, o serviço WinRM retorna um erro para o cliente. Como resultado, a lógica do cliente deve repetir explicitamente a operação com base no erro retornado.

## <a name="event-subscriptions"></a>Assinaturas de evento

Ao usar assinaturas iniciadas pelo coletor, limite o número de [](/windows/desktop/WEC/windows-event-collector) computadores remotos a 500 e isole o serviço coletor de eventos Windows (wecsvc) em um processo de host separado.

Um erro de conexão conterá um thread até que o tempo passe. Um grande número de erros de conexão simultânea pode causar esgotamento do pool de threads e deixar o servidor sem resposta.

 

 