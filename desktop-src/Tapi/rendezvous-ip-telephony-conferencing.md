---
description: Os controles de reunião TAPI 3 permitem que um programador crie aplicativos que podem criar e descobrir conferências de IP de multicast de multimídia.
ms.assetid: 4da2046c-00fd-46a8-805f-503729cfa531
title: Conferência de telefonia IP de reunião
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1cbfc3a1e07fdc245af0ae6b93277c90083a75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169477"
---
# <a name="rendezvous-ip-telephony-conferencing"></a>Conferência de telefonia IP de reunião

\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

Os controles de reunião TAPI 3 permitem que um programador crie aplicativos que podem criar e descobrir conferências de IP de multicast de multimídia.

Os principais componentes da reunião:

Os [controles de diretório](directory-controls.md) são uma abstração de listagens de conferências em um servidor ILS ou NTDS.

Os [controles de blob de conferência](conference-blob-controls.md) representam informações específicas da conferência, como hora de início e de parada. Interfaces especiais são fornecidas para BLOBs de protocolo SDP. Para obter informações detalhadas, consulte RFC 2327 intitulado "SDP: Session description protocol". Uma cópia atual desse RFC pode ser localizada usando um mecanismo de pesquisa da Internet.

As [interfaces com multicast](multicast-com-interfaces.md) são wrappers com para as funções do MADCAP, anteriormente conhecidos como MDHCP. Essas interfaces permitem que um aplicativo obtenha endereços multicast de um servidor de alocação de endereços multicast.

O material a seguir fornece uma visão geral e alguns exemplos de uso dos controles de reunião para a telefonia e a conferência por IP.

 

 



