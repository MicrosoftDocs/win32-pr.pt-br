---
description: O objeto address representa uma entidade que pode fazer ou receber chamadas.
ms.assetid: ab6db262-f99e-4027-9525-7597fcf02e72
title: Objeto de endereço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3ae91e70d6d8efb56321ca4619c6eb973799024
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829137"
---
# <a name="address-object"></a><span data-ttu-id="e8aa1-103">Objeto de endereço</span><span class="sxs-lookup"><span data-stu-id="e8aa1-103">Address Object</span></span>

<span data-ttu-id="e8aa1-104">O objeto address representa uma entidade que pode fazer ou receber chamadas.</span><span class="sxs-lookup"><span data-stu-id="e8aa1-104">The Address object represents an entity that can make or receive calls.</span></span> <span data-ttu-id="e8aa1-105">Esse objeto expõe interfaces e métodos que permitem que um aplicativo execute várias operações, como:</span><span class="sxs-lookup"><span data-stu-id="e8aa1-105">This object exposes interfaces and methods that allow an application to perform a number of operations, such as:</span></span>

-   <span data-ttu-id="e8aa1-106">Descubra se um endereço especificado pode dar suporte a um determinado conjunto de necessidades de tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="e8aa1-106">Discover whether a specified address can support a particular set of media type needs.</span></span>
-   <span data-ttu-id="e8aa1-107">Enumere as chamadas associadas ao endereço no momento.</span><span class="sxs-lookup"><span data-stu-id="e8aa1-107">Enumerate calls currently associated with the address.</span></span>
-   <span data-ttu-id="e8aa1-108">Criar ou encaminhar chamadas.</span><span class="sxs-lookup"><span data-stu-id="e8aa1-108">Create or forward calls.</span></span>
-   <span data-ttu-id="e8aa1-109">Obtenha o nome do provedor de serviços associado.</span><span class="sxs-lookup"><span data-stu-id="e8aa1-109">Get the name of the associated service provider.</span></span>
-   <span data-ttu-id="e8aa1-110">Se um provedor de serviços de mídia existir, obtenha os ponteiros de interface que permitem a manipulação de terminal detalhada.</span><span class="sxs-lookup"><span data-stu-id="e8aa1-110">If a media service provider exists, get interface pointers that allow detailed terminal manipulation.</span></span>
-   <span data-ttu-id="e8aa1-111">Obter e definir outras informações, como se uma mensagem está aguardando.</span><span class="sxs-lookup"><span data-stu-id="e8aa1-111">Get and set other information, such as whether a message is waiting.</span></span>

<span data-ttu-id="e8aa1-112">A maioria dos endereços está associada a um terminal, mas isso não é uniformemente o caso.</span><span class="sxs-lookup"><span data-stu-id="e8aa1-112">Most addresses are associated with a terminal, but this is not uniformly the case.</span></span> <span data-ttu-id="e8aa1-113">Por exemplo, um TSP remoto que fornece acesso a equipamentos em um servidor terá um endereço no computador local, mas não um terminal.</span><span class="sxs-lookup"><span data-stu-id="e8aa1-113">For example, a remote TSP that provides access to equipment on a server will have an address on the local machine but not a terminal.</span></span> <span data-ttu-id="e8aa1-114">Um modem sem viva-voz também não tem nenhum terminal associado ao seu endereço.</span><span class="sxs-lookup"><span data-stu-id="e8aa1-114">A speakerless modem also has no terminal associated with its address.</span></span>

<span data-ttu-id="e8aa1-115">Se um endereço não tiver um terminal associado, a interface [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) não será exposta no objeto.</span><span class="sxs-lookup"><span data-stu-id="e8aa1-115">If an address does not have an associated terminal, the [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) interface is not exposed on the object.</span></span>

<span data-ttu-id="e8aa1-116">O exemplo do código [selecionar um endereço](select-an-address.md) mostra o processo básico para a aquisição de um ponteiro de objeto de endereço.</span><span class="sxs-lookup"><span data-stu-id="e8aa1-116">The [Select an Address](select-an-address.md) code example shows the basic process for acquiring an address object pointer.</span></span>

<span data-ttu-id="e8aa1-117">Consulte [interfaces de objeto de endereço](address-object-interfaces.md) para obter uma lista de todas as interfaces associadas ao objeto de endereço.</span><span class="sxs-lookup"><span data-stu-id="e8aa1-117">See [Address Object Interfaces](address-object-interfaces.md) for a list of all interfaces associated with the Address object.</span></span>

 

 
