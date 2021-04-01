---
description: Com base na taxonomia definida para esquemas de MultiPoint/multicast independentes de protocolo do Windows Sockets 2, o ATM se enquadra na categoria de dados com raiz e em planos de controle com raiz.
ms.assetid: 309afa65-2cc4-4b7b-9968-4c4efb2d10a3
title: Detalhes da função ATM do Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e82ca0531272490c2d3189467186535a63d6ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090999"
---
# <a name="winsock-atm-function-details"></a><span data-ttu-id="81f0a-103">Detalhes da função ATM do Winsock</span><span class="sxs-lookup"><span data-stu-id="81f0a-103">Winsock ATM Function Details</span></span>

<span data-ttu-id="81f0a-104">Com base na taxonomia definida para esquemas de MultiPoint/multicast independentes de protocolo do Windows Sockets 2, o ATM se enquadra na categoria de dados com raiz e em planos de controle com raiz.</span><span class="sxs-lookup"><span data-stu-id="81f0a-104">Based on the taxonomy defined for Windows Sockets 2 protocol-independent multipoint/multicast schemes, ATM falls into the category of rooted data and rooted control planes.</span></span> <span data-ttu-id="81f0a-105">(Consulte a especificação da API do Windows Sockets 2, Apêndice D para obter mais informações.) Um aplicativo agindo como a raiz criará \_ soquetes raiz c, e as contrapartes em execução em nós folha utilizarão \_ soquetes de folha c.</span><span class="sxs-lookup"><span data-stu-id="81f0a-105">(See the Windows Sockets 2 API Specification, Appendix D for more information.) An application acting as the root would create c\_root sockets, and counterparts running on leaf nodes would utilize c\_leaf sockets.</span></span> <span data-ttu-id="81f0a-106">O aplicativo raiz usará [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) para adicionar novos nós folha.</span><span class="sxs-lookup"><span data-stu-id="81f0a-106">The root application will use [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) to add new leaf nodes.</span></span> <span data-ttu-id="81f0a-107">Os aplicativos correspondentes nos nós folha terão definido seus \_ soquetes folha c no modo de escuta.</span><span class="sxs-lookup"><span data-stu-id="81f0a-107">The corresponding applications on the leaf nodes will have set their c\_leaf sockets into the listening mode.</span></span> <span data-ttu-id="81f0a-108">**WSAJoinLeaf** com um \_ soquete raiz c especificado será mapeado para a mensagem de instalação do Q. 2931 (para a primeira folha) ou para adicionar a mensagem da parte (para qualquer uma das folhas subsequentes).</span><span class="sxs-lookup"><span data-stu-id="81f0a-108">**WSAJoinLeaf** with a c\_root socket specified will be mapped to the Q.2931 SETUP message (for the first leaf) or ADD PARTY message (for any subsequent leaves).</span></span>

> [!Note]  
> <span data-ttu-id="81f0a-109">Os parâmetros de QoS especificados em **WSAJoinLeaf** para quaisquer folhas subsequentes devem ser ignorados segundo a especificação uni do fórum ATM.</span><span class="sxs-lookup"><span data-stu-id="81f0a-109">The QoS parameters specified in **WSAJoinLeaf** for any subsequent leaves should be ignored per the ATM Forum UNI specification.</span></span>

 

<span data-ttu-id="81f0a-110">A junção iniciada por folha não faz parte do ATM UNI 3,1, mas tem suporte no ATM UNI 4,0.</span><span class="sxs-lookup"><span data-stu-id="81f0a-110">The leaf-initiated join is not part of the ATM UNI 3.1, but is supported in the ATM UNI 4.0.</span></span> <span data-ttu-id="81f0a-111">Portanto, o [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) com um \_ soquete folha c especificado pode ser mapeado para a mensagem ATM UNI 4,0 apropriada.</span><span class="sxs-lookup"><span data-stu-id="81f0a-111">Thus [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) with a c\_leaf socket specified can be mapped to the appropriate ATM UNI 4.0 message.</span></span>

<span data-ttu-id="81f0a-112">O parâmetro AAL e a negociação B-LLI têm suporte por meio da modificação das s correspondentes no parâmetro *lpSQOS* na invocação da função Condition especificada em [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept).</span><span class="sxs-lookup"><span data-stu-id="81f0a-112">The AAL Parameter and B-LLI negotiation is supported through the modification of the corresponding IEs in the *lpSQOS* parameter upon the invocation of the condition function specified in [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept).</span></span>

> [!Note]  
> <span data-ttu-id="81f0a-113">Somente determinados campos nessas duas s podem ser modificados.</span><span class="sxs-lookup"><span data-stu-id="81f0a-113">Only certain fields in those two IEs can be modified.</span></span> <span data-ttu-id="81f0a-114">Consulte o Apêndice C e o Apêndice F da especificação UNI do ATM Forum para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="81f0a-114">See the ATM Forum UNI specification Appendix C and Appendix F for details.</span></span>

 

 

 



