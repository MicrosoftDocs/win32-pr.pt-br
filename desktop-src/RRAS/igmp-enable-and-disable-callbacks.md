---
title: Habilitar e desabilitar retornos de chamada IGMP
description: O Gerenciador do grupo de multicast usa dois retornos de chamada para o IGMP para coordenar alterações na propriedade da interface de IGMP para um protocolo de roteamento e de um protocolo de roteamento para IGMP.
ms.assetid: e4b2be85-6c67-4801-9905-eb1990d4bbb6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6aa58e9b65c67ac5946f5f5e54e611565e59d8c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823917"
---
# <a name="igmp-enable-and-disable-callbacks"></a>Habilitar e desabilitar retornos de chamada IGMP

O Gerenciador do grupo de multicast usa dois retornos de chamada para o IGMP para coordenar alterações na propriedade da interface de IGMP para um protocolo de roteamento e de um protocolo de roteamento para IGMP. Os retornos de chamada permitem que o IGMP coexista em uma interface com outro protocolo de roteamento, como o DVMRP.

Depois que a propriedade de uma interface é alterada, o Gerenciador do grupo de multicast invoca primeiro o retorno de chamada de [**\_ retorno de chamada PMGM Disable \_ IGMP \_**](/windows/win32/api/mgm/nc-mgm-pmgm_disable_igmp_callback) . O IGMP deve parar de adicionar e excluir associações de grupo na interface especificada até que o Gerenciador de grupo de multicast invoque a PMGM habilitar retorno de chamada de [**\_ retorno de \_ \_ chamada IGMP**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback) .

O Gerenciador do grupo de multicast invoca o PMGM habilitar o retorno de chamada de [**\_ retorno de \_ \_ chamada IGMP**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback) depois que a alteração da propriedade da interface é concluída.

 

 