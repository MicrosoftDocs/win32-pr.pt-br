---
title: Referência da interface do protocolo de roteamento
description: Esta documentação descreve as funções e estruturas que são usadas para implementar um protocolo de roteamento como uma DLL de modo de usuário.
ms.assetid: 0429f5ca-6574-48f5-85ab-70b4677ca539
keywords:
- Serviço de roteamento e acesso remoto RRAS, interface do protocolo de roteamento, referência
- Interface do protocolo de roteamento RRAS, referência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9341dd8dbd304da84fd675aee92e378a44271056
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822608"
---
# <a name="routing-protocol-interface-reference"></a>Referência da interface do protocolo de roteamento

Esta documentação descreve as funções e estruturas que são usadas para implementar um protocolo de roteamento como uma DLL de modo de usuário.

MPR50 deve ser definido no arquivo Make para o protocolo de roteamento.

A macro **sizeof \_ IP \_ Binding (x)** calcula o tamanho, em bytes, de uma estrutura [**de \_ \_ \_ informações de associação de adaptador IP**](/windows/desktop/api/Routprot/ns-routprot-ip_adapter_binding_info) que contém o número de endereços IP.

Esses elementos de referência são descritos nos seguintes tópicos:

-   [Funções da interface do protocolo de roteamento](routing-protocol-interface-functions.md)
-   [Estruturas de interface de protocolo de roteamento](routing-protocol-interface-structures.md)
-   [Gerenciamento de tabela de serviço IPX](ipx-service-table-management.md)

 

 




