---
description: Você pode usar o Auxiliar de IP para executar operações ARP (Protocolo de Resolução de Endereços) para o computador local. Use as funções a seguir para recuperar e modificar a tabela ARP.
ms.assetid: 2c5dc1f8-590f-4b41-b6bb-f82ab093252f
title: Usando o protocolo de resolução de endereço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ca1ef7e5d657476ff85a8893d71e197a034c70234e44f32317b7b05f58c9b94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290006"
---
# <a name="using-the-address-resolution-protocol"></a>Usando o protocolo de resolução de endereço

Você pode usar o Auxiliar de IP para executar operações ARP (Protocolo de Resolução de Endereços) para o computador local. Use as funções a seguir para recuperar e modificar a tabela ARP.

O [**GetIpNetTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipnettable) recupera a tabela ARP. A tabela ARP contém o mapeamento de endereços IP para endereços físicos. Os endereços físicos às vezes são chamados de endereços MAC (Controlador de Acesso de Mídia).

Use as [**funções CreateIpNetEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipnetentry) e [**DeleteIpNetEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipnetentry) para adicionar ou remover entradas ARP específicas para ou da tabela. A [**função FlushIpNetTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-flushipnettable) exclui todas as entradas da tabela.

Para criar ou excluir entradas ARP de proxy, use as funções [**CreateProxyArpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createproxyarpentry) [**e DeleteProxyArpEntry.**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteproxyarpentry)

A [**função SendARP**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-sendarp) envia uma solicitação ARP para a rede local.

 

 



