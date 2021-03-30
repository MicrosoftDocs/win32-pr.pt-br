---
title: Implementando provedores de interfaces de serviço Active Directory
description: As interfaces de serviço do Active Directory (ADSI) são interfaces COM que encapsulam objetos de serviço de diretório para expô-los aos clientes dos serviços de diretório. Ao fornecer uma implementação do ADSI, você expande sua base de clientes para o conjunto de aplicativos cliente ADSI.
ms.assetid: f86f36f0-44ff-41b7-8cf6-b97b721a8572
ms.tgt_platform: multiple
keywords:
- Implementando Active Directory ADSI de provedores de interfaces de serviço
- Implementando ADSI de provedores ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30bdd0da406d9e65af898664e76b5e455540ebeb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634873"
---
# <a name="implementing-active-directory-service-interfaces-providers"></a><span data-ttu-id="5ee69-106">Implementando provedores de interfaces de serviço Active Directory</span><span class="sxs-lookup"><span data-stu-id="5ee69-106">Implementing Active Directory Service Interfaces Providers</span></span>

<span data-ttu-id="5ee69-107">As interfaces de serviço do Active Directory (ADSI) são interfaces COM que encapsulam objetos de serviço de diretório para expô-los aos clientes dos serviços de diretório.</span><span class="sxs-lookup"><span data-stu-id="5ee69-107">Active Directory Service Interfaces (ADSI) are COM interfaces that wrap directory service objects to expose them to clients of directory services.</span></span> <span data-ttu-id="5ee69-108">Ao fornecer uma implementação do ADSI, você expande sua base de clientes para o conjunto de aplicativos cliente ADSI.</span><span class="sxs-lookup"><span data-stu-id="5ee69-108">By supplying an implementation of ADSI, you expand your client-base to the set of ADSI client applications.</span></span>

<span data-ttu-id="5ee69-109">Assim como acontece com qualquer implementação de COM, você pode escrever um provedor ADSI em vários idiomas.</span><span class="sxs-lookup"><span data-stu-id="5ee69-109">As with any COM implementation, you can write an ADSI provider in many languages.</span></span> <span data-ttu-id="5ee69-110">As interfaces COM do ADSI são definidas como interfaces duplas que permitem a resolução de nomes em tempo de execução e de compilação e podem ser chamadas por linguagens em conformidade com a automação, como Visual Basic, Visual Basic Scripting Edition, e também as linguagens mais conscientes de desempenho e eficiência, como C e C++.</span><span class="sxs-lookup"><span data-stu-id="5ee69-110">The ADSI COM interfaces are defined as dual interfaces that allow both run-time and compile-time name resolution and can be called by Automation-compliant languages such as Visual Basic, Visual Basic Scripting Edition, and also the more performance and efficiency-conscious languages such as C and C++.</span></span> <span data-ttu-id="5ee69-111">Os clientes ADSI também incluem aplicativos Web que usam Active Server páginas e snap-ins de administração por meio do console de gerenciamento Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5ee69-111">ADSI clients also include web applications using Active Server Pages and administration snap-ins through the Microsoft Management Console.</span></span>

<span data-ttu-id="5ee69-112">Como a ADSI fornece seu próprio provedor de OLE DB, a implementação dos recursos de pesquisa definidos pelo [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) também permite que os clientes ADSI consultem os dados do serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="5ee69-112">Because ADSI supplies its own OLE DB provider, implementing the search features defined by [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) also enables ADSI clients to query your directory service for data.</span></span>

<span data-ttu-id="5ee69-113">Todos os objetos de serviço de diretório podem ser representados por meio de um objeto ADSI genérico com suporte a [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject).</span><span class="sxs-lookup"><span data-stu-id="5ee69-113">All directory service objects can be represented through a generic ADSI object supporting [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject).</span></span> <span data-ttu-id="5ee69-114">A ADSI fornece os blocos de construção necessários para representar os recursos e serviços de qualquer serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="5ee69-114">ADSI supplies the building blocks necessary to represent the features and services of any directory service.</span></span>

<span data-ttu-id="5ee69-115">Além disso, as metainterfaces ADSI representam objetos comuns usados por administradores de diretório.</span><span class="sxs-lookup"><span data-stu-id="5ee69-115">In addition, the ADSI meta-interfaces represent common objects used by directory administrators.</span></span> <span data-ttu-id="5ee69-116">Você mapeia as propriedades das metainterfaces para as propriedades com suporte no serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="5ee69-116">You map the properties of the meta-interfaces to the properties supported by your directory service.</span></span> <span data-ttu-id="5ee69-117">Os clientes ADSI que programam para as interfaces do serviço de Active Directory têm acesso ao serviço de diretório assim que o provedor é instalado e o sistema é reiniciado.</span><span class="sxs-lookup"><span data-stu-id="5ee69-117">ADSI clients programming to the Active Directory Service Interfaces gain access to your directory service as soon as the provider is installed and the system restarted.</span></span>

<span data-ttu-id="5ee69-118">Se o serviço de diretório oferecer suporte a uma representação de esquema, o suporte às interfaces de gerenciamento de esquema tornará seu namespace diretamente acessível aos navegadores do serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="5ee69-118">If your directory service supports a schema representation, supporting the schema management interfaces makes your namespace directly accessible to directory service browsers.</span></span> <span data-ttu-id="5ee69-119">Ao publicar seus recursos por meio do esquema, os clientes podem consultar seu serviço de diretório online e aproveitar os serviços que você oferece.</span><span class="sxs-lookup"><span data-stu-id="5ee69-119">By publishing your features through the schema, clients can query your directory service online and take advantage of the services you offer.</span></span> <span data-ttu-id="5ee69-120">Devido à disponibilidade do esquema online e à vantagem da interface COM, você pode continuar disponibilizando novos recursos para o software cliente ao mesmo tempo em que oferece suporte a versões de nível inferior.</span><span class="sxs-lookup"><span data-stu-id="5ee69-120">Because of the online schema availability and the COM interface advantage, you can continue to make new features available to your client software while supporting down-level versions.</span></span>

 

 




