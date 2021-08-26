---
title: Retornos de chamada de junção local
description: Depois que o gerenciador de grupos multicast for notificado pelo IGMP de que novos receptores estão presentes para um grupo em uma interface, o gerenciador de grupos multicast invocará o retorno de chamada DE CHAMADA DE JUNÇÃO LOCAL DO PMGM para o protocolo de roteamento que possui a interface, se \_ \_ \_ houver.
ms.assetid: 136f86e0-380d-4158-a9dd-c6de1c7f6689
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17b3464aa645a6ab110acef09f238ffca97f781a38cc6c2602a39e7c66316490
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074066"
---
# <a name="local-join-callbacks"></a>Retornos de chamada de junção local

Depois que o gerenciador de grupos multicast for notificado pelo IGMP de que novos receptores estão presentes para um grupo em uma interface, o gerenciador de grupos multicast invocará o retorno de chamada DE CHAMADA DE JUNÇÃO LOCAL DO [**PMGM \_ \_ \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback) para o protocolo de roteamento que possui a interface, se houver. Esse retorno de chamada notifica o protocolo de roteamento da alteração.

Esse retorno de chamada e o retorno de chamada DE RETORNO DE CHAMADA [**DO PMGM \_ LOCAL \_ LEAVE \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback) são usados para sincronizar o encaminhamento entre protocolos de roteamento e IGMP.

 

 




