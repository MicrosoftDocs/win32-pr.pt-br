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
# <a name="semantic-differences-between-multipoint-sockets-and-regular-sockets-in-the-spi"></a><span data-ttu-id="8c327-103">Diferenças semânticas entre soquetes do MultiPoint e soquetes regulares no SPI</span><span class="sxs-lookup"><span data-stu-id="8c327-103">Semantic Differences Between Multipoint Sockets and Regular Sockets in the SPI</span></span>

<span data-ttu-id="8c327-104">No plano de controle, há algumas diferenças semânticas significativas entre um \_ soquete raiz c e um soquete de ponto a ponto regular:</span><span class="sxs-lookup"><span data-stu-id="8c327-104">In the control plane, there are some significant semantic differences between a c\_root socket and a regular point-to-point socket:</span></span>

-   <span data-ttu-id="8c327-105">O \_ soquete raiz c pode ser usado em [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) para ingressar em uma nova folha.</span><span class="sxs-lookup"><span data-stu-id="8c327-105">The c\_root socket can be used in [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) to join a new leaf.</span></span>
-   <span data-ttu-id="8c327-106">Colocar um \_ soquete raiz c no modo de escuta (chamando [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85))) não impede que o \_ soquete raiz c seja usado em uma chamada para [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) para adicionar uma nova folha ou para enviar e receber dados do MultiPoint.</span><span class="sxs-lookup"><span data-stu-id="8c327-106">Placing a c\_root socket into the listening mode (by calling [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85))) does not preclude the c\_root socket from being used in a call to [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) to add a new leaf, or for sending and receiving multipoint data.</span></span>
-   <span data-ttu-id="8c327-107">O fechamento de um \_ soquete raiz c fará com que todos os \_ soquetes de folha c associados obtenham uma notificação de \_ fechamento FD.</span><span class="sxs-lookup"><span data-stu-id="8c327-107">The closing of a c\_root socket will cause all the associated c\_leaf sockets to get FD\_CLOSE notification.</span></span>

<span data-ttu-id="8c327-108">Não há diferenças semânticas entre um \_ soquete folha c e um soquete regular no plano de controle, exceto que o \_ soquete de folha c pode ser usado em [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf)e o uso do soquete de \_ folha c em [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) indica que somente as solicitações de conexão do MultiPoint devem ser aceitas.</span><span class="sxs-lookup"><span data-stu-id="8c327-108">There are no semantic differences between a c\_leaf socket and a regular socket in the control plane, except that the c\_leaf socket can be used in [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf), and the use of c\_leaf socket in [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) indicates that only multipoint connection requests should be accepted.</span></span>

<span data-ttu-id="8c327-109">No plano de dados, as diferenças semânticas entre o \_ soquete raiz d e um soquete de ponto a ponto regular são</span><span class="sxs-lookup"><span data-stu-id="8c327-109">In the data plane, the semantic differences between the d\_root socket and a regular point-to-point socket are</span></span>

-   <span data-ttu-id="8c327-110">Os dados enviados no \_ soquete raiz d serão entregues a todas as folhas na mesma sessão do MultiPoint.</span><span class="sxs-lookup"><span data-stu-id="8c327-110">The data sent on the d\_root socket will be delivered to all the leaves in the same multipoint session.</span></span>
-   <span data-ttu-id="8c327-111">Os dados recebidos no \_ soquete raiz d podem ser de qualquer uma das folhas.</span><span class="sxs-lookup"><span data-stu-id="8c327-111">The data received on the d\_root socket may be from any of the leaves.</span></span>

<span data-ttu-id="8c327-112">O \_ soquete de folha d no plano de dados com raiz não tem nenhuma diferença semântica do soquete normal, no entanto, no plano de dados sem raiz, os dados enviados no \_ soquete de folha d vão para todos os outros nós folha e os dados recebidos podem ser de qualquer um dos nós folha.</span><span class="sxs-lookup"><span data-stu-id="8c327-112">The d\_leaf socket in the rooted data plane has no semantic difference from the regular socket, however, in the nonrooted data plane, the data sent on the d\_leaf socket will go to all of the other leaf nodes, and the data received could be from any of the other leaf nodes.</span></span> <span data-ttu-id="8c327-113">Como mencionado anteriormente, as informações sobre se o \_ soquete de folha d está em um plano de dados com raiz ou não raiz está contida na estrutura [**de \_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondente para o soquete.</span><span class="sxs-lookup"><span data-stu-id="8c327-113">As mentioned earlier, the information about whether the d\_leaf socket is in a rooted or nonrooted data plane is contained in the corresponding [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the socket.</span></span>

 

 
