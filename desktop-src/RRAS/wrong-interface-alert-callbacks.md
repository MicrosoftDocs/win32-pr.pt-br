---
title: Retornos de chamada de alerta de interface incorreto
description: Depois que o encaminhador de kernel recebe dados de multicast de uma fonte específica na interface errada, ele notifica o Gerenciador do grupo de multicast.
ms.assetid: 7b20625e-286b-4c4f-8452-4d21563fd030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d12906d836ca994e90347ea78cf22e50f8f2f00d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637039"
---
# <a name="wrong-interface-alert-callbacks"></a><span data-ttu-id="fdaa1-103">Retornos de chamada de alerta de interface incorreto</span><span class="sxs-lookup"><span data-stu-id="fdaa1-103">Wrong Interface Alert Callbacks</span></span>

<span data-ttu-id="fdaa1-104">Depois que o encaminhador de kernel recebe dados de multicast de uma fonte específica na interface errada, ele notifica o Gerenciador do grupo de multicast.</span><span class="sxs-lookup"><span data-stu-id="fdaa1-104">After the kernel forwarder receives multicast data from a specific source on the wrong interface, it notifies the multicast group manager.</span></span> <span data-ttu-id="fdaa1-105">O Gerenciador do grupo de multicast invocará o [**PMGM \_ errado \_ se \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback) o retorno de chamada de retorno de chamada ao protocolo de roteamento que possui a interface em que os dados chegaram incorretamente.</span><span class="sxs-lookup"><span data-stu-id="fdaa1-105">The multicast group manager then invokes the [**PMGM\_WRONG\_IF\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback) callback to the routing protocol that owns the interface on which the data incorrectly arrived.</span></span>

> [!Note]  
> <span data-ttu-id="fdaa1-106">Este retorno de chamada não está implementado atualmente nesta versão da API MGM.</span><span class="sxs-lookup"><span data-stu-id="fdaa1-106">This callback is not currently implemented in this version of the MGM API.</span></span>

 

 

 




