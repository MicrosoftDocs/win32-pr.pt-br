---
title: Diferenças semânticas entre soquetes multipontos e soquetes regulares
description: Diferenças entre soquetes de vários pontos raiz c e soquetes \_ regulares ponto a ponto.
ms.assetid: fbadfde8-44dc-41ac-bd93-1a22c76ca321
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06b30ff05c72fc43bf3f4e731242d9f22a2236e9f6fd275c382b57fb05d094cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740806"
---
# <a name="semantic-differences-between-multipoint-sockets-and-regular-sockets"></a>Diferenças semânticas entre soquetes multipontos e soquetes regulares

No plano de controle, há algumas diferenças semânticas significativas entre um soquete raiz c e um soquete ponto \_ a ponto regular:

-   O \_ soquete raiz c pode ser usado [**em WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) para unir uma nova folha.
-   Colocar um soquete raiz c no modo de escuta (chamando listen ) não impede que o soquete raiz c seja usado em uma chamada para \_ [](/windows/desktop/api/Winsock2/nf-winsock2-listen) \_ [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) para adicionar uma nova folha ou para enviar e receber dados de vários pontos.
-   O fechamento de um soquete raiz c faz com que todos os soquetes folha \_ c \_ associados recebam a notificação FD \_ CLOSE.

Não há diferenças semânticas entre um soquete folha c e um soquete regular no plano de controle, exceto que o soquete folha c pode ser usado em \_ \_ [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf)e o uso do soquete folha c em listen indica que apenas solicitações de conexão de vários pontos devem ser \_ aceitas. [](/windows/desktop/api/Winsock2/nf-winsock2-listen)

No plano de dados, as diferenças semânticas entre o soquete raiz d e \_ um soquete ponto a ponto regular são:

-   Os dados enviados no soquete raiz d são entregues a todas \_ as folhas na mesma sessão de vários pontos.
-   Os dados recebidos no \_ soquete raiz d podem ser de qualquer uma das folhas.

O soquete folha d no plano de dados com raiz não tem nenhuma diferença semântica do soquete regular, no entanto, no plano de dados não rooted, os dados enviados no soquete folha d vão para todos os outros nós folha e os dados recebidos podem ser de qualquer outro nós \_ \_ folha. Conforme mencionado anteriormente, as informações sobre se o soquete folha d está em um plano de dados com raiz ou não estão contidas na estrutura \_ [**de INFORMAÇÕES WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondente para o soquete.

 

 
