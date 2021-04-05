---
title: Remover retornos de chamada de alerta
description: Quando o Gerenciador do grupo de multicast é notificado de que os receptores estão saindo de um grupo em uma interface, o Gerenciador do grupo de multicast invoca o retorno de chamada de \_ retorno de chamada de alerta de remoção PMGM \_ \_ .
ms.assetid: 34eb6941-9488-481f-93ca-821789acc140
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a81dab70eaded0fd1fe21bd1b5ec1b5ca495272
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006052"
---
# <a name="prune-alert-callbacks"></a>Remover retornos de chamada de alerta

Quando o Gerenciador do grupo de multicast é notificado de que os receptores estão saindo de um grupo em uma interface, o Gerenciador do grupo de multicast invoca o retorno de chamada de [**retorno de chamada de \_ alerta de remoção \_ \_ PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) . Esse retorno de chamada notifica os protocolos de roteamento que os clientes não pertencem mais ao grupo especificado. Portanto, os protocolos de roteamento devem parar de solicitar dados multicast para os grupos especificados.

O Gerenciador do grupo de multicast tem um conjunto predefinido de regras que são usadas para determinar quando esse retorno de chamada é invocado. Essas regras se baseiam no tipo de solicitação de remoção enviado pelo cliente e na ordem em que as solicitações de remoção foram recebidas.

## <a name="wildcard-prune-requests"></a>Solicitações de remoção de curinga

Quando uma remoção de caractere curinga para um grupo ( \* , g) é recebida e a interface final está sendo removida para o segundo cliente (ou seja, quando as interfaces para apenas um único cliente permanecem), o Gerenciador de grupo de multicast invoca o retorno de chamada de [**retorno de \_ \_ \_ chamada de alerta de remoção PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) para esse cliente restante. Depois que a interface final for removida para o último cliente (ou seja, quando nenhuma outra interface permanecer), esse retorno de chamada será invocado para todos os outros clientes registrados com o Gerenciador do grupo de multicast.

## <a name="source-specific-prune-requests"></a>ReSource-Specific solicitações de remoção

Quando uma remoção específica de origem para um grupo (s, g) é recebida, o Gerenciador de grupo de multicast invoca o retorno de chamada de [**\_ retorno de \_ \_ chamada de alerta PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) apenas para o cliente que possui a interface de entrada em direção às s de origem.

 

 




