---
description: O Auxiliar de IP possibilita acessar informações sobre protocolos de rede usados no computador local.
ms.assetid: 3ae07fbd-0b69-42d6-81ab-cc239c354bbb
title: Recuperando informações sobre o protocolo de controle de transmissão e o protocolo de datagrama do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f10691c39e1f1a2c9c92af8736549427f01cc2400773e214f3a4d5f536fa46e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102046"
---
# <a name="retrieving-information-about-the-transmission-control-protocol-and-the-user-datagram-protocol"></a>Recuperando informações sobre o protocolo de controle de transmissão e o protocolo de datagrama do usuário

O Auxiliar de IP possibilita acessar informações sobre protocolos de rede usados no computador local. Use as funções descritas nos parágrafos a seguir para recuperar informações sobre o protocolo TCP e o UDP (Protocolo de Datagrama de Usuário) no computador local.

A [**função GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) recupera as estatísticas atuais do TCP. Para obter exemplos de **código que envolvem GetTcpStatistics,** consulte Recuperando informações [usando GetTcpStatistics](retrieving-information-using-gettcpstatistics.md).

A [**função GetUdpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudpstatistics) recupera as estatísticas atuais do UDP.

A [**função GetTcpTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcptable) recupera a tabela de conexão TCP. O [**GetUdpTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudptable) recupera a tabela do ouvinte UDP.

A [**função SetTcpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-settcpentry) permite que um desenvolvedor de definir o estado de uma conexão TCP especificada como \_ TCB TCP STATE DELETE do \_ MIB. \_ \_

 

 



