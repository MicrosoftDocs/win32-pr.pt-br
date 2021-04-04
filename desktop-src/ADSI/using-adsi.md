---
title: Usando Active Directory interfaces de serviço
description: As interfaces de serviço do Active Directory (ADSI) fornecem os meios para que os aplicativos cliente dos serviços de diretório usem um conjunto de interfaces para se comunicar com qualquer namespace que forneça uma implementação de ADSI.
ms.assetid: 58bde1ea-30d1-4601-a6fb-df0bb837e2ab
ms.tgt_platform: multiple
keywords:
- Usando Active Directory ADSI de interfaces de serviço
- ADSI, ADSI, usando
- ADSI de interfaces de serviço Active Directory, usando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e500044ec755c393f8c8287528fee7f935751fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822177"
---
# <a name="using-active-directory-service-interfaces"></a><span data-ttu-id="a5a04-106">Usando Active Directory interfaces de serviço</span><span class="sxs-lookup"><span data-stu-id="a5a04-106">Using Active Directory Service Interfaces</span></span>

<span data-ttu-id="a5a04-107">As interfaces de serviço do Active Directory (ADSI) fornecem os meios para que os aplicativos cliente dos serviços de diretório usem um conjunto de interfaces para se comunicar com qualquer namespace que forneça uma implementação de ADSI.</span><span class="sxs-lookup"><span data-stu-id="a5a04-107">Active Directory Service Interfaces (ADSI) provides the means for client applications of directory services to use one set of interfaces to communicate with any namespace that provides an ADSI implementation.</span></span> <span data-ttu-id="a5a04-108">Os clientes ADSI usam as interfaces de serviço de Active Directory bem definidas no lugar das chamadas de API específicas da rede para obter acesso mais simples aos serviços para um namespace.</span><span class="sxs-lookup"><span data-stu-id="a5a04-108">ADSI clients use the well-defined Active Directory Service Interfaces in place of the network-specific API calls to gain simpler access to the services for a namespace.</span></span>

<span data-ttu-id="a5a04-109">Active Directory interfaces de serviço estão em conformidade com o Component Object Model (COM) e oferecem suporte a recursos COM padrão.</span><span class="sxs-lookup"><span data-stu-id="a5a04-109">Active Directory Service Interfaces conform to the Component Object Model (COM) and support standard COM features.</span></span>

<span data-ttu-id="a5a04-110">A ADSI fornece interfaces que são compatíveis com a automação para controladores com limite de nome, como Java, Microsoft Visual Basic Development System e Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="a5a04-110">ADSI supplies interfaces that are compliant with Automation for name-bound controllers like Java, Microsoft Visual Basic development system, and Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="a5a04-111">A ADSI também pode fornecer uma interface que pode otimizar o desempenho de interfaces que não são compatíveis com a automação, para uso com ambientes de linguagem como C e C++.</span><span class="sxs-lookup"><span data-stu-id="a5a04-111">ADSI can also provide an interface that can optimize performance for interfaces that are not compliant with Automation, to use with language environments like C and C++.</span></span>

<span data-ttu-id="a5a04-112">A ADSI também fornece interfaces que não são de automação, [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) e [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch), para dar suporte ao gerenciamento de objeto de diretório e consultas.</span><span class="sxs-lookup"><span data-stu-id="a5a04-112">ADSI also provides the non-automation interfaces, [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) and [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch), to support directory object management and queries.</span></span>

<span data-ttu-id="a5a04-113">Além disso, a ADSI fornece seu próprio provedor de OLE DB, para que qualquer cliente que já use OLE DB, incluindo aqueles que usam ActiveX Data Objects, possa consultar serviços de diretório diretamente.</span><span class="sxs-lookup"><span data-stu-id="a5a04-113">In addition, ADSI supplies its own OLE DB provider, so that any client already using OLE DB, including those using ActiveX Data Objects, can query directory services directly.</span></span>

<span data-ttu-id="a5a04-114">Os aplicativos Web que usam Active Server páginas também podem programar o acesso aos serviços de diretório por meio de ADSI.</span><span class="sxs-lookup"><span data-stu-id="a5a04-114">Web applications using Active Server Pages also can program access to directory services through ADSI.</span></span>

<span data-ttu-id="a5a04-115">Os clientes ADSI podem descobrir programaticamente todos os provedores ADSI em um site e usar as mesmas interfaces para se comunicar com cada namespace.</span><span class="sxs-lookup"><span data-stu-id="a5a04-115">ADSI clients can programmatically discover all the ADSI providers at a site and use the same interfaces to communicate with each namespace.</span></span> <span data-ttu-id="a5a04-116">À medida que provedores adicionais são instalados, os clientes ADSI podem se comunicar, sem recompilar, com os novos namespaces também.</span><span class="sxs-lookup"><span data-stu-id="a5a04-116">As additional providers are installed, the ADSI clients can communicate, without recompiling, with the new namespaces as well.</span></span>

<span data-ttu-id="a5a04-117">Este guia de programação descreve como o ADSI funciona e fornece informações para executar tarefas específicas no ADSI.</span><span class="sxs-lookup"><span data-stu-id="a5a04-117">This programming guide describes how ADSI works and provides information for performing specific tasks in ADSI.</span></span> <span data-ttu-id="a5a04-118">Os seguintes tópicos são abordados:</span><span class="sxs-lookup"><span data-stu-id="a5a04-118">The following topics are discussed:</span></span>

-   [<span data-ttu-id="a5a04-119">Associação a um objeto ADSI</span><span class="sxs-lookup"><span data-stu-id="a5a04-119">Binding to an ADSI Object</span></span>](binding-to-an-adsi-object.md)
-   [<span data-ttu-id="a5a04-120">Criando e excluindo objetos</span><span class="sxs-lookup"><span data-stu-id="a5a04-120">Creating and Deleting Objects</span></span>](creating-and-deleting-objects.md)
-   [<span data-ttu-id="a5a04-121">Acessando e manipulando dados com ADSI</span><span class="sxs-lookup"><span data-stu-id="a5a04-121">Accessing and Manipulating Data with ADSI</span></span>](accessing-and-manipulating-data-with-adsi.md)
-   [<span data-ttu-id="a5a04-122">Usando o esquema ADSI</span><span class="sxs-lookup"><span data-stu-id="a5a04-122">Using the ADSI Schema</span></span>](using-the-adsi-schema.md)
-   [<span data-ttu-id="a5a04-123">Coleções e grupos</span><span class="sxs-lookup"><span data-stu-id="a5a04-123">Collections and Groups</span></span>](collections-and-groups.md)
-   [<span data-ttu-id="a5a04-124">Enumerando objetos ADSI</span><span class="sxs-lookup"><span data-stu-id="a5a04-124">Enumerating ADSI Objects</span></span>](enumerating-adsi-objects.md)
-   [<span data-ttu-id="a5a04-125">Pesquisando Active Directory</span><span class="sxs-lookup"><span data-stu-id="a5a04-125">Searching Active Directory</span></span>](searching-active-directory.md)
-   [<span data-ttu-id="a5a04-126">Modelo de segurança ADSI</span><span class="sxs-lookup"><span data-stu-id="a5a04-126">ADSI Security Model</span></span>](adsi-security-model.md)
-   [<span data-ttu-id="a5a04-127">Extensões ADSI</span><span class="sxs-lookup"><span data-stu-id="a5a04-127">ADSI Extensions</span></span>](adsi-extensions.md)
-   [<span data-ttu-id="a5a04-128">Usando o ADSI com o Exchange</span><span class="sxs-lookup"><span data-stu-id="a5a04-128">Using ADSI with Exchange</span></span>](using-adsi-with-exchange.md)
-   [<span data-ttu-id="a5a04-129">Interfaces do utilitário ADSI</span><span class="sxs-lookup"><span data-stu-id="a5a04-129">ADSI Utility Interfaces</span></span>](adsi-utility-interfaces.md)
-   [<span data-ttu-id="a5a04-130">Programando ADSI com Java/COM</span><span class="sxs-lookup"><span data-stu-id="a5a04-130">Programming ADSI with Java/COM</span></span>](programming-adsi-with-javacom.md)

 

 




