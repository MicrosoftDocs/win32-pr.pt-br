---
title: Diferenças semânticas entre soquetes do MultiPoint e soquetes regulares
description: Diferenças entre \_ soquetes do MultiPoint raiz c e soquetes de ponto a ponto regulares.
ms.assetid: fbadfde8-44dc-41ac-bd93-1a22c76ca321
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04d95b2637a4f805cea5ee6f138cc6992080a238
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782419"
---
# <a name="semantic-differences-between-multipoint-sockets-and-regular-sockets"></a>Diferenças semânticas entre soquetes do MultiPoint e soquetes regulares

No plano de controle, há algumas diferenças semânticas significativas entre um \_ soquete raiz c e um soquete de ponto a ponto regular:

-   O \_ soquete raiz c pode ser usado em [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) para ingressar em uma folha nova.
-   Colocar um \_ soquete raiz c no modo de escuta (chamando [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen)) não impede que o \_ soquete raiz c seja usado em uma chamada para [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) para adicionar uma nova folha ou para enviar e receber dados do MultiPoint.
-   O fechamento de um \_ soquete raiz c faz com que todos os \_ soquetes de folha c associados obtenham uma notificação de \_ fechamento FD.

Não há diferenças semânticas entre um \_ soquete folha c e um soquete regular no plano de controle, exceto que o \_ soquete de folha c pode ser usado em [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf)e o uso do soquete de \_ folha c em [**escuta**](/windows/desktop/api/Winsock2/nf-winsock2-listen) indica que somente as solicitações de conexão do MultiPoint devem ser aceitas.

No plano de dados, as diferenças semânticas entre o \_ soquete raiz d e um soquete de ponto a ponto regular são:

-   Os dados enviados no \_ soquete raiz d são entregues a todas as folhas na mesma sessão do MultiPoint.
-   Os dados recebidos no \_ soquete raiz d podem ser de qualquer uma das folhas.

O \_ soquete de folha d no plano de dados com raiz não tem nenhuma diferença semântica do soquete normal, no entanto, no plano de dados sem raiz, os dados enviados no \_ soquete de folha d vão para todos os outros nós folha e os dados recebidos podem ser de qualquer outro nó folha. Como mencionado anteriormente, as informações sobre se o \_ soquete de folha d está em um plano de dados com raiz ou não raiz está contida na estrutura [**de \_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondente para o soquete.

 

 
