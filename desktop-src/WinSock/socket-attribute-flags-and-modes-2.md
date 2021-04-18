---
description: Há vários atributos de soquete que podem ser indicados por meio do parâmetro flags em WSPSocket.
ms.assetid: 5fd4321b-a5cc-4921-bec5-bdf625261ea2
title: Sinalizadores e modos de atributo de soquete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8da1a5f621a7d9f489f4e91782462c215659772b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788628"
---
# <a name="socket-attribute-flags-and-modes"></a>Sinalizadores e modos de atributo de soquete

Há vários atributos de soquete que podem ser indicados por meio do parâmetro *flags* em [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket). O \_ sinalizador de sinalizador WSA \_ sobreposto indica que um Soquete será usado para operações de e/s sobrepostas. O suporte desse atributo é obrigatório para todos os provedores de serviço. Consulte [e/s sobreposta](overlapped-i-o-2.md) para obter mais informações. Observe que a criação de um soquete com o atributo Overlapped não afeta se um soquete está atualmente no modo de bloqueio ou sem bloqueio. Os soquetes criados com o atributo Overlapped podem ser usados para executar e/s sobreposta e fazer isso não altera o modo de bloqueio de um soquete. Como as operações de e/s sobrepostas não são bloqueadas, o modo de bloqueio de um soquete é irrelevante para essas operações.

Quatro sinalizadores de atributo adicionais são usados ao criar soquetes que devem ser usados para operações do MultiPoint e/ou multicast, e o suporte para esses atributos é opcional. Provedores que dão suporte a atributos do MultiPoint indicam isso por meio do XP1 \_ suporte \_ MultiPoint bit em suas respectivas estruturas de [**\_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) . Consulte [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) e [multicast independente de protocolo e MultiPoint na API](protocol-independent-multicast-and-multipoint-in-the-spi-2.md) para obter a definição e o uso de cada um desses sinalizadores. Somente os soquetes criados com atributos relacionados ao MultiPoint podem ser usados na função [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) para criar sessões do MultiPoint.

Um soquete está em um dos dois modos, bloqueio e não bloqueio, a qualquer momento. Os soquetes são criados no modo de bloqueio por padrão e podem ser alterados para o modo de não bloqueio chamando [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)), [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85))ou [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)). Um soquete pode ser revertido para o modo de bloqueio usando **WSPIoctl** se nenhum **WSPAsyncSelect** ou **WSPEventSelect** estiver ativo. O modo para um soquete afeta apenas as funções que podem bloquear e não afeta as operações de e/s sobrepostas. Consulte [bloqueando operações](blocking-operations-2.md) para obter mais informações.

 

 
