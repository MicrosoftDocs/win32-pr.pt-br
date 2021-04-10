---
description: O auxiliar de IP estende sua capacidade de gerenciar interfaces de rede. Há uma correspondência um-para-um entre as interfaces e os adaptadores em um determinado computador. Uma interface é uma abstração de nível de IP, enquanto que um adaptador é uma abstração no nível de vínculo de datalink.
ms.assetid: 598bbe67-30df-4c02-8f30-2ccf15b5c494
title: Gerenciando interfaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 024d79d46ec1ba7606cbc7e79b4312432984239a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169407"
---
# <a name="managing-interfaces"></a><span data-ttu-id="dfc74-105">Gerenciando interfaces</span><span class="sxs-lookup"><span data-stu-id="dfc74-105">Managing Interfaces</span></span>

<span data-ttu-id="dfc74-106">O auxiliar de IP estende sua capacidade de gerenciar interfaces de rede.</span><span class="sxs-lookup"><span data-stu-id="dfc74-106">IP Helper extends your abilities to manage network interfaces.</span></span> <span data-ttu-id="dfc74-107">Há uma correspondência um-para-um entre as interfaces e os adaptadores em um determinado computador.</span><span class="sxs-lookup"><span data-stu-id="dfc74-107">There is a one-to-one correspondence between the interfaces and adapters on a given computer.</span></span> <span data-ttu-id="dfc74-108">Uma interface é uma abstração de nível de IP, enquanto que um adaptador é uma abstração no nível de vínculo de datalink.</span><span class="sxs-lookup"><span data-stu-id="dfc74-108">An interface is an IP-level abstraction, whereas an adapter is a datalink-level abstraction.</span></span>

<span data-ttu-id="dfc74-109">Use as funções descritas nos parágrafos a seguir para gerenciar interfaces no computador local.</span><span class="sxs-lookup"><span data-stu-id="dfc74-109">Use the functions described in the following paragraphs to manage interfaces on the local computer.</span></span>

<span data-ttu-id="dfc74-110">A função [**GetNumberOfInterfaces**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnumberofinterfaces) retorna o número de interfaces no computador local.</span><span class="sxs-lookup"><span data-stu-id="dfc74-110">The [**GetNumberOfInterfaces**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnumberofinterfaces) function returns the number of interfaces on the local computer.</span></span>

<span data-ttu-id="dfc74-111">A função [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) retorna uma tabela que contém os nomes e os índices correspondentes para as interfaces no computador local.</span><span class="sxs-lookup"><span data-stu-id="dfc74-111">The [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) function returns a table that contains the names and corresponding indexes for the interfaces on the local computer.</span></span> <span data-ttu-id="dfc74-112">Para obter exemplos de código envolvendo **GetInterfaceInfo** , consulte [Gerenciando interfaces usando o GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md).</span><span class="sxs-lookup"><span data-stu-id="dfc74-112">For code samples involving **GetInterfaceInfo** see [Managing Interfaces Using GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md).</span></span>

<span data-ttu-id="dfc74-113">A função [**GetFriendlyIfIndex**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getfriendlyifindex) usa um índice de interface e retorna um índice de interface compatível com versões anteriores, ou seja, um que usa apenas os 24 bits inferiores.</span><span class="sxs-lookup"><span data-stu-id="dfc74-113">The [**GetFriendlyIfIndex**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getfriendlyifindex) function takes an interface index and returns a backward-compatible interface index, that is, one that uses only the lower 24 bits.</span></span> <span data-ttu-id="dfc74-114">Esse tipo de índice, às vezes, é chamado de índice de interface "amigável".</span><span class="sxs-lookup"><span data-stu-id="dfc74-114">This type of index is sometimes referred to as a "friendly" interface index.</span></span>

<span data-ttu-id="dfc74-115">A função [**GetIfEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getifentry) retorna uma [**estrutura \_ IFROW MIB**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow) que contém informações sobre uma interface específica no computador local.</span><span class="sxs-lookup"><span data-stu-id="dfc74-115">The [**GetIfEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getifentry) function returns a [**MIB\_IFROW**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow) structure that contains information about a particular interface on the local computer.</span></span> <span data-ttu-id="dfc74-116">Essa função requer que o chamador forneça o índice da interface.</span><span class="sxs-lookup"><span data-stu-id="dfc74-116">This function requires the caller to supply the index of the interface.</span></span>

<span data-ttu-id="dfc74-117">A função [**GetIfTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getiftable) retorna uma tabela de [**entradas \_ IFROW de MIB**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow) , uma para cada interface no computador.</span><span class="sxs-lookup"><span data-stu-id="dfc74-117">The [**GetIfTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getiftable) function returns a table of [**MIB\_IFROW**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow) entries, one for each interface on the computer.</span></span>

<span data-ttu-id="dfc74-118">Use a função [**SetIfEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setifentry) para modificar a configuração de uma interface específica.</span><span class="sxs-lookup"><span data-stu-id="dfc74-118">Use the [**SetIfEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setifentry) function to modify the configuration of a particular interface.</span></span>

 

 
