---
title: Enumerando grupos (RRAS)
description: A tabela a seguir resume uma série de etapas em uma interação entre um protocolo de roteamento e o gerenciador de grupos multicast.
ms.assetid: 30a81946-fa60-4424-9a16-a9b4dfe1961e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4df3731e8370a213636ea12ad2a9b072903908888eba6983909c01201c655ef2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101836"
---
# <a name="enumerating-groups"></a>Enumerando grupos

A tabela a seguir resume uma série de etapas em uma interação entre um protocolo de roteamento e o gerenciador de grupos multicast. A primeira coluna descreve as ações que o protocolo de roteamento executa e as respostas do protocolo de roteamento para o gerenciador de grupos multicast. A segunda coluna descreve as respostas do gerenciador de grupos multicast ao protocolo de roteamento. A terceira coluna apresenta informações adicionais.

Cada linha da tabela representa uma etapa.



| Ação de protocolo de roteamento                                                                                                                                                    | Ação do gerenciador de grupos multicast                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Obtenha um handle para uma enumeração usando a [**função MgmGroupEnumerationStart.**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationstart)                                                         | Retornar um alça.                                                                                                                                                                                                                                                                                             |
| Obtenha um ou mais grupos usando [**a função MgmGroupEnumerationGetNext.**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext)                                                             | Retornar quantos grupos se ajustarem ao buffer fornecido pelo cliente. Se nenhum grupo puder ser retornado no buffer fornecido, retorne ERROR INSUFFICIENT BUFFER e o tamanho do buffer necessário \_ \_ para retornar um grupo.<br/> RETORNAR ERRO \_ NÃO MAIS ITENS quando não houver mais \_ \_ grupos.<br/> |
| Se ERROR INSUFFICIENT BUFFER for recebido, chame \_ a função \_ [**MgmGroupEnumerationGetNext**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext) novamente usando um buffer do tamanho indicado. |                                                                                                                                                                                                                                                                                                              |
| Continue chamando [**a função MgmGroupEnumerationGetNext**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext) até que ERROR \_ NO MORE ITEMS seja \_ \_ recebido.                                   |                                                                                                                                                                                                                                                                                                              |
| Encerrar o processo de enumeração usando [**a função MgmGroupEnumerationEnd.**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationend)                                                                   | Destruir o alça.                                                                                                                                                                                                                                                                                          |



 

 

 





