---
description: Outras ferramentas da Microsoft para a criação de aplicativos distribuídos
ms.assetid: 518ca5b5-4285-4d69-abfe-bf6444a1deb5
title: Outras ferramentas da Microsoft para a criação de aplicativos distribuídos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657d65bd7c61a73bedb9463e8558415c7b27fe04
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793345"
---
# <a name="other-microsoft-tools-for-building-distributed-applications"></a><span data-ttu-id="ea679-103">Outras ferramentas da Microsoft para a criação de aplicativos distribuídos</span><span class="sxs-lookup"><span data-stu-id="ea679-103">Other Microsoft Tools for Building Distributed Applications</span></span>

<span data-ttu-id="ea679-104">Além das ferramentas do COM+, a Microsoft fornece as seguintes ferramentas para ajudar o desenvolvedor na criação de aplicativos distribuídos:</span><span class="sxs-lookup"><span data-stu-id="ea679-104">In addition to the tools in COM+, Microsoft provides the following tools to assist the developer in creating distributed applications:</span></span>

-   <span data-ttu-id="ea679-105">MDAC (Microsoft Data Access Components).</span><span class="sxs-lookup"><span data-stu-id="ea679-105">Microsoft Data Access Components (MDAC).</span></span> <span data-ttu-id="ea679-106">A Microsoft fornece vários caminhos para recuperar dados de uma infinidade de fontes.</span><span class="sxs-lookup"><span data-stu-id="ea679-106">Microsoft provides several avenues for retrieving data from a myriad of sources.</span></span> <span data-ttu-id="ea679-107">Por exemplo, OLE DB oferece um conjunto de interfaces COM para a criação de componentes de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ea679-107">For example, OLE DB offers a set of COM interfaces for building database components.</span></span> <span data-ttu-id="ea679-108">As interfaces são definidas para que os provedores de dados possam implementar diferentes níveis de suporte, com base nos recursos do armazenamento de dados subjacente.</span><span class="sxs-lookup"><span data-stu-id="ea679-108">The interfaces are defined so that data providers can implement different levels of support, based on the capabilities of the underlying data store.</span></span> <span data-ttu-id="ea679-109">Como o OLE DB é baseado em COM, ele pode ser facilmente estendido e as extensões são implementadas como novas interfaces.</span><span class="sxs-lookup"><span data-stu-id="ea679-109">Because OLE DB is COM-based, it can easily be extended, and extensions are implemented as new interfaces.</span></span> <span data-ttu-id="ea679-110">O OLE DB também inclui uma interface de programação de nível de aplicativo, chamada ActiveX Data Objects (ADO).</span><span class="sxs-lookup"><span data-stu-id="ea679-110">OLE DB also includes an application-level programming interface, called ActiveX Data Objects (ADO).</span></span> <span data-ttu-id="ea679-111">O ADO expõe interfaces duplas, para que possa ser facilmente usado por meio de linguagens de script, bem como Microsoft Visual C++, Visual Basic e outras ferramentas de desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="ea679-111">ADO exposes dual interfaces, so it can easily be used from scripting languages as well as Microsoft Visual C++, Visual Basic, and other developer tools.</span></span>

    > [!Note]  
    > <span data-ttu-id="ea679-112">Os desenvolvedores também podem optar por usar uma API genérica, neutra para o fornecedor, como a API (interface de programação de aplicativo) do Microsoft Open Database Connectivity (ODBC).</span><span class="sxs-lookup"><span data-stu-id="ea679-112">Developers can also choose to use a generic, vendor-neutral API such as the Microsoft Open Database Connectivity (ODBC) application programming interface (API).</span></span> <span data-ttu-id="ea679-113">A API ODBC é uma interface de linguagem C para acessar dados em um DBMS usando o linguagem SQL (SQL).</span><span class="sxs-lookup"><span data-stu-id="ea679-113">The ODBC API is a C language interface for accessing data in a DBMS by using Structured Query Language (SQL).</span></span> <span data-ttu-id="ea679-114">Um Gerenciador de driver ODBC fornece a interface de programação e os componentes de tempo de execução para localizar drivers específicos de DBMS.</span><span class="sxs-lookup"><span data-stu-id="ea679-114">An ODBC driver manager provides the programming interface and run-time components to locate DBMS-specific drivers.</span></span> <span data-ttu-id="ea679-115">Os drivers ODBC, normalmente fornecidos pelo fornecedor do DBMS, convertem chamadas genéricas do Gerenciador de driver ODBC em chamadas para o método de acesso a dados nativo.</span><span class="sxs-lookup"><span data-stu-id="ea679-115">ODBC drivers, typically supplied by the DBMS vendor, translate generic calls from the ODBC driver manager into calls to the native data access method.</span></span> <span data-ttu-id="ea679-116">A principal vantagem de usar a API ODBC é que você precisa aprender apenas uma API para acessar uma ampla gama de DBMSs.</span><span class="sxs-lookup"><span data-stu-id="ea679-116">The primary advantage of using the ODBC API is that you need to learn only one API to access a wide range of DBMSs.</span></span>

     

-   <span data-ttu-id="ea679-117">Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ea679-117">Microsoft SQL Server.</span></span> <span data-ttu-id="ea679-118">Além de fornecer um sistema de banco de dados relacional robusto e eloqüência, o Microsoft SQL Server pode fornecer um aplicativo distribuído com o pool de conexões e segurança que podem ser integrados ao modelo de segurança do Windows.</span><span class="sxs-lookup"><span data-stu-id="ea679-118">In addition to providing a robust and eloquent relational database system, Microsoft SQL Server can provide a distributed application with connection pooling and security that can integrate with the Windows security model.</span></span>

-   <span data-ttu-id="ea679-119">Integração de transações COM (COMTI).</span><span class="sxs-lookup"><span data-stu-id="ea679-119">COM Transaction Integration (COMTI).</span></span> <span data-ttu-id="ea679-120">O COMTI pode ser usado para integrar sistemas de mainframe em sistemas Windows, incluindo aplicativos COM+.</span><span class="sxs-lookup"><span data-stu-id="ea679-120">COMTI can be used to integrate mainframe systems into Windows systems, including COM+ applications.</span></span> <span data-ttu-id="ea679-121">O COMTI usa protocolos de comunicação padrão (por exemplo, LU 6,2) para a comunicação entre computadores com Windows e mainframe e minicomputers.</span><span class="sxs-lookup"><span data-stu-id="ea679-121">COMTI uses standard communication protocols (for example, LU 6.2) for communicating between Windows computers and mainframe and minicomputers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea679-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ea679-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea679-123">Princípios e pressuposições de design de COM+</span><span class="sxs-lookup"><span data-stu-id="ea679-123">COM+ Design Assumptions and Principles</span></span>](com--design-assumptions-and-principles.md)
</dt> <dt>

[<span data-ttu-id="ea679-124">Criando o aplicativo COM+ usando UML</span><span class="sxs-lookup"><span data-stu-id="ea679-124">Designing the COM+ Application Using UML</span></span>](designing-the-com--application-using-uml.md)
</dt> <dt>

[<span data-ttu-id="ea679-125">Dicas de design gerais para usar o COM+</span><span class="sxs-lookup"><span data-stu-id="ea679-125">General Design Tips for Using COM+</span></span>](general-design-tips-for-using-com-.md)
</dt> <dt>

[<span data-ttu-id="ea679-126">Otimizando interações com a camada de lógica de negócios do COM+</span><span class="sxs-lookup"><span data-stu-id="ea679-126">Optimizing Interactions with the COM+ Business Logic Tier</span></span>](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> </dl>

 

 



