---
description: Um processador de processadores é um mecanismo para IPC (comunicações de um meio de processo). Os aplicativos podem armazenar mensagens em um processador. O proprietário do processador pode recuperar mensagens armazenadas lá.
ms.assetid: e23894ca-edc7-49e6-bcc4-c82f357ecedf
title: Processadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6886e8d6f08206c6104db22c050aa6bb9859f96f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105791394"
---
# <a name="mailslots"></a>Processadores

Um *processador de processadores* é um mecanismo para IPC (comunicações de um meio de processo). Os aplicativos podem armazenar mensagens em um processador. O proprietário do processador pode recuperar mensagens armazenadas lá. Essas mensagens são normalmente enviadas por uma rede para um computador especificado ou para todos os computadores em um domínio especificado. Um *domínio* é um grupo de estações de trabalho e servidores que compartilham um nome de grupo.

-   [Sobre processadores de informações](about-mailslots.md)
-   [Usando processadores](using-mailslots.md)
-   [Referência do processador de processadores](mailslot-reference.md)

Você pode optar por usar [pipes nomeados](named-pipes.md) ou [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2) em vez de processadores de chamadas para comunicações entre processos. Pipes nomeados são uma maneira simples de dois processos para trocar mensagens. Os processadores de mensagens, por outro lado, são uma maneira simples de um processo de difundir mensagem para vários processos. Uma consideração importante é que o unibytes transmite mensagens usando datagramas. Um *datagrama* é um pequeno pacote de informações que a rede envia ao longo da conexão. Como uma transmissão de rádio ou televisão, um datagrama não oferece nenhuma confirmação de recebimento; Não é possível garantir que um datagrama tenha sido recebido. Assim como as montanhas, edifícios grandes ou sinais de interferência podem fazer com que um sinal de rádio ou televisão seja perdido, há coisas que podem impedir que um datagrama atinja um destino específico. Pipes nomeados são como chamadas telefônicas: você se comunica apenas com uma entidade, mas sabe que a mensagem está sendo recebida.

 

 
