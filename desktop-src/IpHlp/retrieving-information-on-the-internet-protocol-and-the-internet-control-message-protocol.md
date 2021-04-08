---
description: O IP Helper fornece recursos de recuperação de informações que são úteis para a administração de rede do computador local.
ms.assetid: b50b3927-6c74-4282-b79b-c86d72d93ae3
title: Recuperando informações sobre o protocolo de Internet e o protocolo de mensagem de controle da Internet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09b2768ff591b53db79bbbfb38fc2c6c2596ca9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920662"
---
# <a name="retrieving-information-on-the-internet-protocol-and-the-internet-control-message-protocol"></a>Recuperando informações sobre o protocolo de Internet e o protocolo de mensagem de controle da Internet

O IP Helper fornece recursos de recuperação de informações que são úteis para a administração de rede do computador local. As funções a seguir recuperam estatísticas para o protocolo IP e o protocolo ICMP (Internet Control Message Protocol). Você também pode usar essas funções para definir determinados parâmetros de configuração para o IP.

A função [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) recupera as estatísticas de IP atuais para o computador local. Para obter exemplos de código envolvendo **GetIpStatistics** , consulte [recuperando informações usando GetIpStatistics](retrieving-information-using-getipstatistics.md).

A função [**GetIcmpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-geticmpstatistics) recupera as estatísticas ICMP atuais.

Use a função [**SetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipstatistics) para habilitar ou desabilitar o encaminhamento de IP. Essa função também possibilita que você defina o TTL (vida útil) padrão para datagramas IP. Como alternativa, você pode definir o TTL usando a função [**SetIpTTL**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipttl) .

 

 



