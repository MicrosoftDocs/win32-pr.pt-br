---
description: Você pode usar o IP Helper para executar operações de ARP (protocolo de resolução de endereço) para o computador local. Use as funções a seguir para recuperar e modificar a tabela ARP.
ms.assetid: 2c5dc1f8-590f-4b41-b6bb-f82ab093252f
title: Usando o protocolo de resolução de endereço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deec57c3b028f8f90135567bb07dbc00bda89036
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757007"
---
# <a name="using-the-address-resolution-protocol"></a>Usando o protocolo de resolução de endereço

Você pode usar o IP Helper para executar operações de ARP (protocolo de resolução de endereço) para o computador local. Use as funções a seguir para recuperar e modificar a tabela ARP.

O [**GetIpNetTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipnettable) recupera a tabela ARP. A tabela ARP contém o mapeamento de endereços IP para endereços físicos. Os endereços físicos às vezes são chamados de endereços MAC (controlador de acesso à mídia).

Use as funções [**CreateIpNetEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipnetentry) e [**DeleteIpNetEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipnetentry) para adicionar ou remover entradas ARP específicas de ou para a tabela. A função [**FlushIpNetTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-flushipnettable) exclui todas as entradas da tabela.

Para criar ou excluir entradas ARP de proxy, use as funções [**CreateProxyArpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createproxyarpentry) e [**DeleteProxyArpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteproxyarpentry) .

A função [**SendARP**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-sendarp) envia uma solicitação ARP para a rede local.

 

 



