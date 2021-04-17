---
description: O ATM se enquadra na categoria de dados com raiz e em planos de controle com raiz.
ms.assetid: 8e355efe-2903-49c1-a9b3-792b07bd2995
title: Ponto ATM para MultiPoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba17616feadfe1c8bf87ee8468dd967af73452c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811990"
---
# <a name="atm-point-to-multipoint"></a><span data-ttu-id="de83c-103">Ponto ATM para MultiPoint</span><span class="sxs-lookup"><span data-stu-id="de83c-103">ATM Point to Multipoint</span></span>

<span data-ttu-id="de83c-104">O ATM se enquadra na categoria de dados com raiz e em planos de controle com raiz.</span><span class="sxs-lookup"><span data-stu-id="de83c-104">ATM falls into the category of rooted data and rooted control planes.</span></span> <span data-ttu-id="de83c-105">Um aplicativo agindo como a raiz criará \_ soquetes raiz c e as contrapartes em execução em nós folha utilizarão \_ soquetes de folha c.</span><span class="sxs-lookup"><span data-stu-id="de83c-105">An application acting as the root would create c\_root sockets and counterparts running on leaf nodes would utilize c\_leaf sockets.</span></span> <span data-ttu-id="de83c-106">O aplicativo raiz usa [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) para adicionar novos nós folha.</span><span class="sxs-lookup"><span data-stu-id="de83c-106">The root application uses [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) to add new leaf nodes.</span></span> <span data-ttu-id="de83c-107">Os aplicativos correspondentes nos nós folha terão definido seus \_ soquetes folha c no modo de escuta.</span><span class="sxs-lookup"><span data-stu-id="de83c-107">The corresponding applications on the leaf nodes will have set their c\_leaf sockets into listen mode.</span></span> <span data-ttu-id="de83c-108">**WSAJoinLeaf** com um \_ soquete raiz c especificado é mapeado para a mensagem de addparting do Q. 2931.</span><span class="sxs-lookup"><span data-stu-id="de83c-108">**WSAJoinLeaf** with a c\_root socket specified is mapped to the Q.2931 ADDPARTY message.</span></span> <span data-ttu-id="de83c-109">A junção iniciada por folha não tem suporte no ATM UNI 3,1, mas tem suporte no ATM UNI 4,0.</span><span class="sxs-lookup"><span data-stu-id="de83c-109">The leaf-initiated join is not supported in ATM UNI 3.1, but is supported in ATM UNI 4.0.</span></span> <span data-ttu-id="de83c-110">Portanto, **WSAJoinLeaf** com um \_ soquete folha c especificado é mapeado para a mensagem ATM UNI 4,0 apropriada.</span><span class="sxs-lookup"><span data-stu-id="de83c-110">Thus **WSAJoinLeaf** with a c\_leaf socket specified is mapped to the appropriate ATM UNI 4.0 message.</span></span>

<span data-ttu-id="de83c-111">Há considerações adicionais a serem lembradas para o ponto a multiponto do ATM:</span><span class="sxs-lookup"><span data-stu-id="de83c-111">There are additional considerations to bear in mind for ATM point-to-multipoint:</span></span>

-   <span data-ttu-id="de83c-112">A adição de novas folhas à sessão de ponto a multiponto ATM é apenas baseada em convite.</span><span class="sxs-lookup"><span data-stu-id="de83c-112">The addition of new leaves to the ATM point-to-multipoint session is invitation-based only.</span></span> <span data-ttu-id="de83c-113">As convites raiz saem, que já têm sua chamada de função [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) – chamando a função [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) .</span><span class="sxs-lookup"><span data-stu-id="de83c-113">The root invites leaves — which have already their [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) function call — by calling the [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) function.</span></span>
-   <span data-ttu-id="de83c-114">O fluxo de dados em uma sessão de ponto a multiponto ATM é somente de raiz para sair; as folhas não podem usar a mesma sessão para enviar informações para a raiz.</span><span class="sxs-lookup"><span data-stu-id="de83c-114">The flow of data in an ATM point-to-multipoint session is from root-to-leaves only; leaves cannot use the same session to send information to the root.</span></span>
-   <span data-ttu-id="de83c-115">Apenas uma folha por adaptador ATM é permitida.</span><span class="sxs-lookup"><span data-stu-id="de83c-115">Only one leaf per ATM adapter is allowed.</span></span>

 

 



