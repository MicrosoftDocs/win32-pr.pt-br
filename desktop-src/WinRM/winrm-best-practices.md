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
ms.openlocfilehash: 3452f2b8e61fb72b1fd5f99a073b48afb26dafb0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917356"
---
# <a name="winrm-best-practices"></a>Práticas recomendadas do WinRM

Este tópico explica algumas das práticas recomendadas para usar os vários recursos da API do WinRM.

## <a name="quotas"></a>Cotas

Quando uma cota é atingida, o serviço WinRM retorna um erro para o cliente. Como resultado, a lógica do cliente deve repetir explicitamente a operação com base no erro retornado.

## <a name="event-subscriptions"></a>Assinaturas de evento

Ao usar assinaturas iniciadas pelo coletor, limite o número de computadores remotos a 500 e isole o serviço [coletor de eventos do Windows](/windows/desktop/WEC/windows-event-collector) (Wecsvc) em um processo de host separado.

Um erro de conexão manterá um thread até atingir o tempo limite. Um grande número de erros de conexão simultâneas pode causar esgotamento do pool de threads e renderizar o servidor sem resposta.

 

 