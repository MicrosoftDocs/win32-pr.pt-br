---
description: Diferenças entre soquetes de ponto a ponto regulares e \_ soquetes do MultiPoint raiz c no SPI do Windows Sockets (Winsock).
ms.assetid: 5476933b-70f2-4dcf-a6e9-f9f4a537c29f
title: Diferenças semânticas entre soquetes do MultiPoint e soquetes regulares no SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd9e4e94583ee653a8ec0bf19c743dddd3e16253
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762323"
---
# <a name="semantic-differences-between-multipoint-sockets-and-regular-sockets-in-the-spi"></a>Diferenças semânticas entre soquetes do MultiPoint e soquetes regulares no SPI

No plano de controle, há algumas diferenças semânticas significativas entre um \_ soquete raiz c e um soquete de ponto a ponto regular:

-   O \_ soquete raiz c pode ser usado em [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) para ingressar em uma nova folha.
-   Colocar um \_ soquete raiz c no modo de escuta (chamando [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85))) não impede que o \_ soquete raiz c seja usado em uma chamada para [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) para adicionar uma nova folha ou para enviar e receber dados do MultiPoint.
-   O fechamento de um \_ soquete raiz c fará com que todos os \_ soquetes de folha c associados obtenham uma notificação de \_ fechamento FD.

Não há diferenças semânticas entre um \_ soquete folha c e um soquete regular no plano de controle, exceto que o \_ soquete de folha c pode ser usado em [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf)e o uso do soquete de \_ folha c em [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) indica que somente as solicitações de conexão do MultiPoint devem ser aceitas.

No plano de dados, as diferenças semânticas entre o \_ soquete raiz d e um soquete de ponto a ponto regular são

-   Os dados enviados no \_ soquete raiz d serão entregues a todas as folhas na mesma sessão do MultiPoint.
-   Os dados recebidos no \_ soquete raiz d podem ser de qualquer uma das folhas.

O \_ soquete de folha d no plano de dados com raiz não tem nenhuma diferença semântica do soquete normal, no entanto, no plano de dados sem raiz, os dados enviados no \_ soquete de folha d vão para todos os outros nós folha e os dados recebidos podem ser de qualquer um dos nós folha. Como mencionado anteriormente, as informações sobre se o \_ soquete de folha d está em um plano de dados com raiz ou não raiz está contida na estrutura [**de \_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondente para o soquete.

 

 
