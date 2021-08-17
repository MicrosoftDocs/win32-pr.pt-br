---
description: Diferenças entre soquetes ponto a ponto regulares e soquetes de vários pontos raiz C \_ na SPI Windows Sockets (Winsock).
ms.assetid: 5476933b-70f2-4dcf-a6e9-f9f4a537c29f
title: Diferenças semânticas entre soquetes de vários pontos e soquetes regulares na SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e585c335d7503d884d58e25b6fc0ad6dd0c0c3356064ebb1504898770d4b7b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740604"
---
# <a name="semantic-differences-between-multipoint-sockets-and-regular-sockets-in-the-spi"></a>Diferenças semânticas entre soquetes de vários pontos e soquetes regulares na SPI

No plano de controle, há algumas diferenças semânticas significativas entre um soquete raiz c e um soquete ponto \_ a ponto regular:

-   O \_ soquete raiz c pode ser usado [**no WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) para unir uma nova folha.
-   Colocar um soquete raiz c no modo de escuta \_ (chamando [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85))) não impede que o soquete raiz c seja usado em uma chamada para \_ [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) para adicionar uma nova folha ou para enviar e receber dados de vários pontos.
-   O fechamento de um soquete raiz c fará com que todos os soquetes folha \_ c \_ associados recebam a notificação FD \_ CLOSE.

Não há diferenças semânticas entre um soquete folha c e um soquete regular no plano de controle, exceto que o soquete folha c pode ser usado no \_ \_ [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf)e o uso do soquete folha c em \_ [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) indica que apenas solicitações de conexão multipoint devem ser aceitas.

No plano de dados, as diferenças semânticas entre o soquete raiz d \_ e um soquete ponto a ponto regular são

-   Os dados enviados no soquete raiz d serão entregues a todas \_ as folhas na mesma sessão de vários pontos.
-   Os dados recebidos no \_ soquete raiz d podem ser de qualquer uma das folhas.

O soquete folha d no plano de dados com raiz não tem nenhuma diferença semântica do soquete regular, no entanto, no plano de dados não resoted, os dados enviados no soquete folha d vão para todos os outros nós folha e os dados recebidos podem ser de qualquer um dos outros nós \_ \_ folha. Conforme mencionado anteriormente, as informações sobre se o soquete folha d está em um plano de dados com raiz ou não estão contidas na estrutura \_ [**de INFORMAÇÕES WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondente para o soquete.

 

 
