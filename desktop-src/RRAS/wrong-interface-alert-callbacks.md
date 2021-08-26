---
title: Retornos de chamada de alerta de interface incorreto
description: Depois que o encaminhador de kernel recebe dados de multicast de uma fonte específica na interface errada, ele notifica o Gerenciador do grupo de multicast.
ms.assetid: 7b20625e-286b-4c4f-8452-4d21563fd030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ac3354b1355cbcb1654b41a61ab046e74ec41b8dc716de6d50f7d9d52b18d94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024646"
---
# <a name="wrong-interface-alert-callbacks"></a>Retornos de chamada de alerta de interface incorreto

Depois que o encaminhador de kernel recebe dados de multicast de uma fonte específica na interface errada, ele notifica o Gerenciador do grupo de multicast. O Gerenciador do grupo de multicast invocará o [**PMGM \_ errado \_ se \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback) o retorno de chamada de retorno de chamada ao protocolo de roteamento que possui a interface em que os dados chegaram incorretamente.

> [!Note]  
> Este retorno de chamada não está implementado atualmente nesta versão da API MGM.

 

 

 




