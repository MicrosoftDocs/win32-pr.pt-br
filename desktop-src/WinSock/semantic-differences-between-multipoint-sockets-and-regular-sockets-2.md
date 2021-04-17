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
# <a name="semantic-differences-between-multipoint-sockets-and-regular-sockets"></a><span data-ttu-id="c67e7-103">Diferenças semânticas entre soquetes do MultiPoint e soquetes regulares</span><span class="sxs-lookup"><span data-stu-id="c67e7-103">Semantic differences between multipoint sockets and regular sockets</span></span>

<span data-ttu-id="c67e7-104">No plano de controle, há algumas diferenças semânticas significativas entre um \_ soquete raiz c e um soquete de ponto a ponto regular:</span><span class="sxs-lookup"><span data-stu-id="c67e7-104">In the control plane, there are some significant semantic differences between a c\_root socket and a regular point-to-point socket:</span></span>

-   <span data-ttu-id="c67e7-105">O \_ soquete raiz c pode ser usado em [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) para ingressar em uma folha nova.</span><span class="sxs-lookup"><span data-stu-id="c67e7-105">The c\_root socket can be used in [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) to join a new a leaf.</span></span>
-   <span data-ttu-id="c67e7-106">Colocar um \_ soquete raiz c no modo de escuta (chamando [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen)) não impede que o \_ soquete raiz c seja usado em uma chamada para [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) para adicionar uma nova folha ou para enviar e receber dados do MultiPoint.</span><span class="sxs-lookup"><span data-stu-id="c67e7-106">Placing a c\_root socket into listening mode (by calling [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen)) does not preclude the c\_root socket from being used in a call to [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) to add a new leaf, or for sending and receiving multipoint data.</span></span>
-   <span data-ttu-id="c67e7-107">O fechamento de um \_ soquete raiz c faz com que todos os \_ soquetes de folha c associados obtenham uma notificação de \_ fechamento FD.</span><span class="sxs-lookup"><span data-stu-id="c67e7-107">The closing of a c\_root socket causes all of the associated c\_leaf sockets to get FD\_CLOSE notification.</span></span>

<span data-ttu-id="c67e7-108">Não há diferenças semânticas entre um \_ soquete folha c e um soquete regular no plano de controle, exceto que o \_ soquete de folha c pode ser usado em [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf)e o uso do soquete de \_ folha c em [**escuta**](/windows/desktop/api/Winsock2/nf-winsock2-listen) indica que somente as solicitações de conexão do MultiPoint devem ser aceitas.</span><span class="sxs-lookup"><span data-stu-id="c67e7-108">There are no semantic differences between a c\_leaf socket and a regular socket in the control plane, except that the c\_leaf socket can be used in [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf), and the use of c\_leaf socket in [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) indicates that only multipoint connection requests should be accepted.</span></span>

<span data-ttu-id="c67e7-109">No plano de dados, as diferenças semânticas entre o \_ soquete raiz d e um soquete de ponto a ponto regular são:</span><span class="sxs-lookup"><span data-stu-id="c67e7-109">In the data plane, the semantic differences between the d\_root socket and a regular point-to-point socket are:</span></span>

-   <span data-ttu-id="c67e7-110">Os dados enviados no \_ soquete raiz d são entregues a todas as folhas na mesma sessão do MultiPoint.</span><span class="sxs-lookup"><span data-stu-id="c67e7-110">The data sent on the d\_root socket is delivered to all the leaves in the same multipoint session.</span></span>
-   <span data-ttu-id="c67e7-111">Os dados recebidos no \_ soquete raiz d podem ser de qualquer uma das folhas.</span><span class="sxs-lookup"><span data-stu-id="c67e7-111">The data received on the d\_root socket may be from any of the leaves.</span></span>

<span data-ttu-id="c67e7-112">O \_ soquete de folha d no plano de dados com raiz não tem nenhuma diferença semântica do soquete normal, no entanto, no plano de dados sem raiz, os dados enviados no \_ soquete de folha d vão para todos os outros nós folha e os dados recebidos podem ser de qualquer outro nó folha.</span><span class="sxs-lookup"><span data-stu-id="c67e7-112">The d\_leaf socket in the rooted data plane has no semantic difference from the regular socket, however, in the nonrooted data plane, the data sent on the d\_leaf socket goes to all the other leaf nodes, and the data received could be from any other leaf nodes.</span></span> <span data-ttu-id="c67e7-113">Como mencionado anteriormente, as informações sobre se o \_ soquete de folha d está em um plano de dados com raiz ou não raiz está contida na estrutura [**de \_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondente para o soquete.</span><span class="sxs-lookup"><span data-stu-id="c67e7-113">As mentioned earlier, the information about whether the d\_leaf socket is in a rooted or nonrooted data plane is contained in the corresponding [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the socket.</span></span>

 

 
