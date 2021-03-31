---
title: Arquitetura de interfaces de serviço Active Directory
description: Muitos serviços de diretório são hierárquicos e, portanto, prestam-se a um modelo de objeto hierárquico. Esta seção usa representações de objeto COM para ilustrar vários recursos ADSI.
ms.assetid: ef545aea-a7a5-4f65-9133-e68b94a86311
ms.tgt_platform: multiple
keywords:
- ADSI da arquitetura de interfaces do serviço Active Directory
- ADSI ADSI, sobre, arquitetura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce59d8d6281aa99bd96efa38166ef658972a5f54
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634900"
---
# <a name="active-directory-service-interfaces-architecture"></a><span data-ttu-id="538ad-106">Arquitetura de interfaces de serviço Active Directory</span><span class="sxs-lookup"><span data-stu-id="538ad-106">Active Directory Service Interfaces Architecture</span></span>

<span data-ttu-id="538ad-107">Muitos serviços de diretório são hierárquicos e, portanto, prestam-se a um modelo de objeto hierárquico.</span><span class="sxs-lookup"><span data-stu-id="538ad-107">Many directory services are hierarchical and thus lend themselves to a hierarchical object model.</span></span> <span data-ttu-id="538ad-108">Esta seção usa representações de objeto COM para ilustrar vários recursos ADSI.</span><span class="sxs-lookup"><span data-stu-id="538ad-108">This section uses COM object representations to illustrate various ADSI features.</span></span>

<span data-ttu-id="538ad-109">Na figura de modelo de objeto a seguir, um objeto de sistema de nível superior contém um objeto de namespace para cada provedor ADSI instalado.</span><span class="sxs-lookup"><span data-stu-id="538ad-109">In the following object model figure, a top-level system object contains one Namespace object for every installed ADSI provider.</span></span>

![objeto contêiner de namespaces](images/ds2top.png)

<span data-ttu-id="538ad-111">Cada um dos objetos de namespace é, em si, um contêiner que contém os nós raiz de nível superior de cada servidor, domínio ou quaisquer outros tipos de objetos do sistema de diretório definidos como raízes em cada serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="538ad-111">Each of the Namespace objects is itself a container that contains the top-level root nodes of every server, domain, or whatever other kinds of directory-system objects are defined as roots in each directory service.</span></span>

<span data-ttu-id="538ad-112">A ADSI fornece um conjunto de interfaces e objetos predefinidos para que os aplicativos cliente possam interagir com os serviços de diretório usando um conjunto uniforme de métodos.</span><span class="sxs-lookup"><span data-stu-id="538ad-112">ADSI supplies a set of predefined objects and interfaces so that client applications can interact with directory services using a uniform set of methods.</span></span> <span data-ttu-id="538ad-113">No entanto, a ADSI pode não fornecer acesso a todos os recursos de um serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="538ad-113">However, ADSI may not provide access to all features of a directory service.</span></span> <span data-ttu-id="538ad-114">Para usar melhor o conjunto de recursos completo de cada serviço de diretório, a ADSI fornece um modelo de esquema que os provedores de serviço de diretório e fornecedores de software de terceiros podem usar para estender recursos além das interfaces fornecidas na ADSI.</span><span class="sxs-lookup"><span data-stu-id="538ad-114">To better use the full feature set of each directory service, ADSI supplies a schema model that directory service providers and third-party software vendors can use to extend features beyond the interfaces provided in ADSI.</span></span>

<span data-ttu-id="538ad-115">Os objetos de contêiner de nó raiz, encontrados dentro de cada objeto de namespace de provedor, incluem um objeto de contêiner de esquema ADSI.</span><span class="sxs-lookup"><span data-stu-id="538ad-115">The root-node container objects, found within each provider Namespace object, include an ADSI schema container object.</span></span> <span data-ttu-id="538ad-116">Este objeto contém a definição de todos os recursos para esse provedor.</span><span class="sxs-lookup"><span data-stu-id="538ad-116">This object contains the definition of all features for that provider.</span></span> <span data-ttu-id="538ad-117">Para obter mais informações, consulte [modelo de esquema ADSI](adsi-schema-model.md).</span><span class="sxs-lookup"><span data-stu-id="538ad-117">For more information, see [ADSI Schema Model](adsi-schema-model.md).</span></span>

<span data-ttu-id="538ad-118">Esta seção inclui os tópicos a seguir:</span><span class="sxs-lookup"><span data-stu-id="538ad-118">This section includes the following topics:</span></span>

-   [<span data-ttu-id="538ad-119">Active Directory objetos de interfaces de serviço</span><span class="sxs-lookup"><span data-stu-id="538ad-119">Active Directory Service Interfaces Objects</span></span>](active-directory-service-interfaces-objects.md)
-   [<span data-ttu-id="538ad-120">Namespaces</span><span class="sxs-lookup"><span data-stu-id="538ad-120">Namespaces</span></span>](namespaces.md)
-   [<span data-ttu-id="538ad-121">Provedor de interfaces de serviço Active Directory</span><span class="sxs-lookup"><span data-stu-id="538ad-121">Active Directory Service Interfaces Provider</span></span>](active-directory-service-interfaces-provider.md)
-   [<span data-ttu-id="538ad-122">Modelo de esquema ADSI</span><span class="sxs-lookup"><span data-stu-id="538ad-122">ADSI Schema Model</span></span>](adsi-schema-model.md)

 

 




