---
description: O IP Helper torna possível acessar informações sobre protocolos de rede que são usados no computador local.
ms.assetid: 3ae07fbd-0b69-42d6-81ab-cc239c354bbb
title: Recuperando informações sobre o protocolo de controle de transmissão e o protocolo de datagrama do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99a73893bf379dda6a58f86854028967da806863
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663603"
---
# <a name="retrieving-information-about-the-transmission-control-protocol-and-the-user-datagram-protocol"></a>Recuperando informações sobre o protocolo de controle de transmissão e o protocolo de datagrama do usuário

O IP Helper torna possível acessar informações sobre protocolos de rede que são usados no computador local. Use as funções descritas nos parágrafos a seguir para recuperar informações sobre o protocolo TCP e UDP (User Datagram Protocol) no computador local.

A função [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) recupera as estatísticas atuais para TCP. Para obter exemplos de código envolvendo **GetTcpStatistics** , consulte [recuperando informações usando GetTcpStatistics](retrieving-information-using-gettcpstatistics.md).

A função [**GetUdpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudpstatistics) recupera as estatísticas atuais para UDP.

A função [**GetTcpTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcptable) recupera a tabela de conexão TCP. O [**GetUdpTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudptable) recupera a tabela de ouvinte UDP.

A função [**SetTcpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-settcpentry) permite que um desenvolvedor defina o estado de uma conexão TCP especificada para a \_ exclusão de estado de TCP do MIB \_ \_ \_ .

 

 



