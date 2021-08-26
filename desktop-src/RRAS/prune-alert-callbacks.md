---
title: Remoção de retornos de chamada de alerta
description: Quando o gerenciador de grupos multicast é notificado de que os receptores estão deixando um grupo em uma interface, o gerenciador de grupos multicast invoca o retorno de chamada DE ALERTA \_ PMGM \_ PRUNE. \_
ms.assetid: 34eb6941-9488-481f-93ca-821789acc140
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b5aa4d95742a2976ea46367b0f1af9442528c2821dc9d27b09b9e1c29eee6d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036395"
---
# <a name="prune-alert-callbacks"></a>Remoção de retornos de chamada de alerta

Quando o gerenciador de grupos multicast é notificado de que os receptores estão deixando um grupo em uma interface, o gerenciador de grupos multicast invoca o retorno de chamada DE ALERTA [**\_ PMGM PRUNE. \_ \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) Esse retorno de chamada notifica os protocolos de roteamento que os clientes não pertencem mais ao grupo especificado. Portanto, os protocolos de roteamento devem parar de solicitar dados multicast para os grupos especificados.

O gerenciador de grupos multicast tem um conjunto predefinido de regras que são usadas para determinar quando esse retorno de chamada é invocado. Essas regras se baseiam no tipo de solicitação de remoção enviada pelo cliente e na ordem em que as solicitações de remoção foram recebidas.

## <a name="wildcard-prune-requests"></a>Solicitações de remoção de caractere curinga

Quando uma remoção de curinga para um grupo ( , g) é recebida e a interface final está sendo removida para o segundo para o último cliente (ou seja, quando as interfaces para apenas um único cliente permanecem), o gerenciador de grupos multicast invoca o retorno de chamada DE RETORNO DE CHAMADA DE ALERTA DE REMOVEÇÃO DE \* [**PMGM \_ \_ \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) para esse cliente restante. Depois que a interface final for removida para o último cliente (ou seja, quando nenhuma outra interface permanecer), esse retorno de chamada será invocado para todos os outros clientes registrados com o gerenciador de grupos multicast.

## <a name="source-specific-prune-requests"></a>Source-Specific solicitações de remoção

Quando uma remoção específica da origem para um grupo (s, g) é recebida, o gerenciador de grupos multicast invoca o retorno de chamada DE RETORNO DE CHAMADA DE ALERTA [**\_ DE PODA \_ \_ PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) somente para o cliente que possui a interface de entrada para os s de origem.

 

 




