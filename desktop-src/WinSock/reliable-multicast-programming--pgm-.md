---
description: Esta seção descreve a implementação do protocolo de multicast de Pragmatic General multicast (PGM) no Windows, geralmente conhecida como multicast confiável. O multicast confiável é implementado por meio do Windows Sockets no Windows Server 2003 e posterior.
ms.assetid: 81c203ed-739f-4a06-99a1-9a99c6164edc
title: Programação de multicast confiável (PGM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce57fcce7bf2faf471604bed97d345971801ca1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105796225"
---
# <a name="reliable-multicast-programming-pgm"></a>Programação de multicast confiável (PGM)

Esta seção descreve a implementação do protocolo de multicast de Pragmatic General multicast (PGM) no Windows, geralmente conhecida como multicast confiável. O multicast confiável é implementado por meio do Windows Sockets no Windows Server 2003 e posterior.

**Windows XP:** O PGM só tem suporte quando o MSMQ (enfileiramento de mensagens da Microsoft) 3,0 está instalado.

O PGM é um protocolo multicast confiável e escalonável que permite que os receptores detectem perda, solicitem a retransmissão de dados perdidos ou notifiquem uma aplicação de perda irrecuperável. O PGM é um protocolo confiável para receptor, o que significa que o receptor é responsável por garantir que todos os dados sejam recebidos, absolvingndo o remetente da responsabilidade de recepção.

O PGM é apropriado para aplicativos que exigem entrega de dados multicast livre de duplicação de várias fontes para vários destinatários. O PGM não dá suporte à entrega confirmada, nem garante a ordenação de pacotes de vários remetentes.

Para obter mais informações sobre o PGM, consulte RFC 3208 disponível em [www.ietf.org](https://www.ietf.org/).

Esta seção descreve como usar multicast confiável no Windows. Os tópicos a seguir explicam os diversos aspectos da criação de um aplicativo de multicast confiável usando soquetes do Windows:

-   [Remetentes e receptores de PGM](pgm-senders-and-receivers.md)
-   [Opções do remetente PGM](pgm-sender-options.md)
-   [Enviando e recebendo dados do PGM](sending-and-receiving-pgm-data.md)
-   [Hospedagem múltipla e PGM](multihoming-and-pgm.md)
-   [Opções de soquete PGM](pgm-socket-options.md)

 

 



