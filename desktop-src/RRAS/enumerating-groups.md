---
title: Enumerando grupos (RRAS)
description: A tabela a seguir resume uma série de etapas em uma interação entre um protocolo de roteamento e o Gerenciador do grupo de multicast.
ms.assetid: 30a81946-fa60-4424-9a16-a9b4dfe1961e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d3860c6876ed6ea5caef4941efcdd949eb9890d
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/12/2019
ms.locfileid: "104453795"
---
# <a name="enumerating-groups"></a>Enumerando grupos

A tabela a seguir resume uma série de etapas em uma interação entre um protocolo de roteamento e o Gerenciador do grupo de multicast. A primeira coluna descreve as ações que o protocolo de roteamento executa e as respostas do protocolo de roteamento para o Gerenciador do grupo de multicast. A segunda coluna descreve as respostas do Gerenciador do grupo de multicast para o protocolo de roteamento. A terceira coluna apresenta informações adicionais.

Cada linha da tabela representa uma etapa.



| Ação do protocolo de roteamento                                                                                                                                                    | Ação do Gerenciador de grupo multicast                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Obtenha um identificador para uma enumeração usando a função [**MgmGroupEnumerationStart**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationstart) .                                                         | Retornar um identificador.                                                                                                                                                                                                                                                                                             |
| Obtenha um ou mais grupos usando a função [**MgmGroupEnumerationGetNext**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext) .                                                             | Retornar quantos grupos couberem no buffer fornecido pelo cliente. Se nenhum grupo puder ser retornado no buffer fornecido, \_ \_ o buffer de erro de retorno será insuficiente e o tamanho do buffer necessário para retornar um grupo.<br/> Retorne o erro \_ sem \_ mais \_ itens quando não houver mais grupos.<br/> |
| Se \_ o buffer insuficiente de erro \_ for recebido, chame a função [**MgmGroupEnumerationGetNext**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext) novamente usando um buffer do tamanho indicado. |                                                                                                                                                                                                                                                                                                              |
| Continue chamando a função [**MgmGroupEnumerationGetNext**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext) até que o erro \_ nenhum \_ \_ item seja recebido.                                   |                                                                                                                                                                                                                                                                                                              |
| Finalize o processo de enumeração usando a função [**MgmGroupEnumerationEnd**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationend) .                                                                   | Destrua o identificador.                                                                                                                                                                                                                                                                                          |



 

 

 





