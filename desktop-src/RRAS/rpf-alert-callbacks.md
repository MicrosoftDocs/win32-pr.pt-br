---
title: Retornos de chamada de alerta do RPF
description: Depois que o Gerenciador de grupo de multicast recebe uma notificação de um pacote de uma nova fonte ou de um pacote destinado a um novo grupo, o Gerenciador de grupo de multicast pesquisa a rota para a origem na exibição de multicast da tabela de roteamento.
ms.assetid: dacccca2-e6a5-417a-a217-06ff846d55f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ff1c2dc66b2307b60fb649fd8a0adb6992a63532bf9aa45350d261ab04b6c5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035915"
---
# <a name="rpf-alert-callbacks"></a>Retornos de chamada de alerta do RPF

Depois que o Gerenciador de grupo de multicast recebe uma notificação de um pacote de uma nova fonte ou de um pacote destinado a um novo grupo, o Gerenciador de grupo de multicast pesquisa a rota para a origem na exibição de multicast da tabela de roteamento. Em seguida, o Gerenciador do grupo de multicast invoca o retorno de chamada do [**PMGM \_ RPF \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback) para o protocolo que possui a interface na qual os dados chegaram.

Depois que esse retorno de chamada for invocado, o protocolo de roteamento poderá alterar a interface de entrada se o protocolo de roteamento precisar receber os dados para o grupo em uma interface diferente.

 

 




