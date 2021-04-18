---
description: Os problemas de tamanho do pacote de mídia abordados no tópico sobre o tamanho do pacote de mídia afetam os vários protocolos IPX de PF de \_ forma diferente.
ms.assetid: 7f0643b8-6bb2-4dbb-b306-d9b2e0d0e03c
title: Como o tamanho do pacote afeta os protocolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c778ee6c75cd558d19cdf1cbb76052065e03c427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296350"
---
# <a name="how-packet-size-affects-protocols"></a>Como o tamanho do pacote afeta os protocolos

Os problemas de tamanho do pacote de mídia abordados no tópico [sobre o tamanho do pacote de mídia](about-media-packet-size-2.md)afetam os vários protocolos IPX de PF de \_ forma diferente. Uma estratégia comum para lidar com várias restrições de tamanho de roteador e mídia é usar o tamanho de mídia completo quando o número de rede da estação remota corresponde à estação local e retorna para o tamanho mínimo do pacote, caso contrário.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>NSPROTO \_ IPX
</dt> <dd>

Fornece um serviço de datagrama; cada datagrama deve residir no tamanho máximo do pacote. O Winsock define o tamanho máximo do pacote de datagrama para o tamanho do pacote de mídia local menos o cabeçalho IPX. No entanto, tenha em mente que, se o pacote for roteado, ele poderá atingir as restrições do roteador em direção à rota. Verifique se seu aplicativo pode retornar a datagramas de 546 bytes.

</dd> <dt>

<span id="NSPROTO_SPX"></span><span id="nsproto_spx"></span>NSPROTO \_ SPX
</dt> <dd>

Fornece serviços de fluxo e pacotes sequenciados. O Winsock IPX/SPX permite que fluxos de dados e mensagens abranjam vários pacotes, portanto, o tamanho do pacote não limita a quantidade de dados manipulados por [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send) e [**recv**](/windows/desktop/api/winsock/nf-winsock-recv). No entanto, o tamanho da mídia subjacente deve ser definido corretamente ou o primeiro pacote grande não será entregue e a conexão será redefinida. Se a estação de destino estiver na rede local, o Winsock definirá seu tamanho de pacote para o tamanho do pacote de mídia. Caso contrário, o padrão é 512 bytes. Esse tamanho pode ser alterado imediatamente após a [**conexão**](/windows/desktop/api/Winsock2/nf-winsock2-connect) ou a [**aceitação**](/windows/desktop/api/Winsock2/nf-winsock2-accept) por meio do [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt).

</dd> <dt>

<span id="NSPROTO_SPXII"></span><span id="nsproto_spxii"></span>NSPROTO \_ SPXII
</dt> <dd>

O SPXII apresenta uma grande negociação de pacotes da Internet para manter um melhor ajuste para pacotes e não requer intervenção do programador. No entanto, se a estação remota não oferecer suporte a SPXII e negociar para o SPX Standard, as regras do NSPROTO \_ SPX estarão em vigor.



| Protocolo     | Mídia      | Tipo        | Tamanho do pacote de dados |
|--------------|------------|-------------|------------------|
| NSPROTO \_ IPX | Ethernet   | Ethernet II |                  |
|              |            | 802.3       |                  |
|              |            | 802.2       | 1466             |
|              |            | ALINHA        |                  |
|              | Anel de token | 4 megabits   |                  |
|              |            | 16 megabits  |                  |
| NSPROTO \_ SPX | Ethernet   | Ethernet II |                  |
|              |            | 802.3       |                  |
|              |            | 802.2       | 1454             |
|              |            | ALINHA        |                  |
|              | Anel de token | 4 megabits   |                  |
|              |            | 16 megabits  |                  |



 

</dd> </dl>

 

 



