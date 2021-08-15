---
title: Retornos de chamada de saída locais
description: Depois que o gerenciador de grupos multicast for notificado pelo IGMP de que não há mais receptores presentes para um grupo em uma interface, o gerenciador de grupos multicast invocará o retorno de chamada DE RETORNO DE CHAMADA DE SAÍDA LOCAL do PMGM para o protocolo de roteamento nessa interface, se \_ \_ \_ houver. Esse retorno de chamada notifica o protocolo de roteamento da alteração.
ms.assetid: 47696533-603c-459f-9aa7-3ce42fff3332
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce4cd346ac3d84a5c763c7f8f866e21a1bffa2af533e5710c86ec8826ad7db45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790636"
---
# <a name="local-leave-callbacks"></a>Retornos de chamada de saída locais

Depois que o gerenciador de grupos multicast for notificado pelo IGMP de que não há mais receptores presentes para um grupo em uma interface, o gerenciador de grupos multicast invocará o retorno de chamada DE RETORNO DE CHAMADA DE SAÍDA LOCAL do [**PMGM \_ \_ \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback) para o protocolo de roteamento nessa interface, se houver. Esse retorno de chamada notifica o protocolo de roteamento da alteração.

Esse retorno de chamada e o retorno de chamada DO [**\_ PMGM LOCAL JOIN \_ \_ CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback) são usados para sincronizar o encaminhamento entre protocolos de roteamento e IGMP.

 

 




