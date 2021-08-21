---
description: Os controles de reunião TAPI 3 permitem que um programador crie aplicativos que podem criar e descobrir conferências de IP de multicast de multimídia.
ms.assetid: 4da2046c-00fd-46a8-805f-503729cfa531
title: Conferência de telefonia IP de reunião
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c1486f2ca730f1efb0391fdea5a3ad22bec65385a31bce9bf233f0f230b7ee5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773566"
---
# <a name="rendezvous-ip-telephony-conferencing"></a>Conferência de telefonia IP de reunião

\[os controles e as interfaces de conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

Os controles de reunião TAPI 3 permitem que um programador crie aplicativos que podem criar e descobrir conferências de IP de multicast de multimídia.

Os principais componentes da reunião:

Os [controles de diretório](directory-controls.md) são uma abstração de listagens de conferências em um servidor ILS ou NTDS.

Os [controles de blob de conferência](conference-blob-controls.md) representam informações específicas da conferência, como hora de início e de parada. Interfaces especiais são fornecidas para BLOBs de protocolo SDP. Para obter informações detalhadas, consulte RFC 2327 intitulado "SDP: Session description protocol". Uma cópia atual desse RFC pode ser localizada usando um mecanismo de pesquisa da Internet.

As [interfaces com multicast](multicast-com-interfaces.md) são wrappers com para as funções do MADCAP, anteriormente conhecidos como MDHCP. Essas interfaces permitem que um aplicativo obtenha endereços multicast de um servidor de alocação de endereços multicast.

O material a seguir fornece uma visão geral e alguns exemplos de uso dos controles de reunião para a telefonia e a conferência por IP.

 

 



