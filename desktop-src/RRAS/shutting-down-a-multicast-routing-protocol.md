---
title: Desligando um protocolo de roteamento multicast
description: A tabela a seguir resume uma série de etapas em uma interação de desligamento entre o Gerenciador do grupo de multicast e o protocolo de roteamento quando o protocolo de roteamento está sendo desligado.
ms.assetid: d868218d-7939-45d1-9e2f-3415c40f1a62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08d35285bdf613cb8ec5966fa438742004a97c0a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641606"
---
# <a name="shutting-down-a-multicast-routing-protocol"></a>Desligando um protocolo de roteamento multicast

A tabela a seguir resume uma série de etapas em uma interação de desligamento entre o Gerenciador do grupo de multicast e o protocolo de roteamento quando o protocolo de roteamento está sendo desligado. A primeira coluna descreve as ações que o protocolo de roteamento executa e as respostas do protocolo de roteamento para o Gerenciador do grupo de multicast. A segunda coluna descreve as respostas do Gerenciador do grupo de multicast para o protocolo de roteamento e quaisquer ações que o Gerenciador de grupo de multicast executa, como retornos de chamada. A terceira coluna apresenta informações adicionais.

Cada linha da tabela representa uma etapa.



| Ação do protocolo de roteamento                                                                                                                                     | Ação do Gerenciador de grupo multicast                                                                                                                                                                                                                                                                                                                                                                                                                                            | Observações                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| Liberar a propriedade de cada interface que o protocolo de roteamento possui usando a função [**MgmReleaseInterfaceOwnership**](/windows/desktop/api/Mgm/nf-mgm-mgmreleaseinterfaceownership) . | Se o IGMP também estiver em execução na interface que acabou de ser lançada por um protocolo de roteamento, contate o IGMP usando o retorno de chamada de [**\_ retorno de chamada PMGM Disable \_ IGMP \_**](/windows/win32/api/mgm/nc-mgm-pmgm_disable_igmp_callback) . Depois que todas as alterações nos dados de multicast sobre a propriedade da interface tiverem sido feitas, entre em contato com o IGMP novamente usando PMGM habilitar retorno de chamada do [**\_ \_ IGMP \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback) .<br/> Exclua todas as entradas de encaminhamento associadas a esta interface.<br/> |                                                                           |
| Cancele o registro com o Gerenciador do grupo de multicast usando a função [**MgmDeRegisterMProtocol**](/windows/desktop/api/Mgm/nf-mgm-mgmderegistermprotocol) .                                    | Destrua o identificador que foi retornado ao protocolo de roteamento por uma chamada anterior para a função [**MgmDeRegisterMProtocol**](/windows/desktop/api/Mgm/nf-mgm-mgmderegistermprotocol) .                                                                                                                                                                                                                                                                                                                 | O protocolo de roteamento não pode mais usar esse identificador para chamar as funções MGM. |



 

 

