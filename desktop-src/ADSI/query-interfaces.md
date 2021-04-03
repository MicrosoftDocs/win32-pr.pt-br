---
title: Interfaces de consulta
description: Três tipos de interfaces ADSI podem ser usados para executar pesquisas de diretório. O ambiente de aplicativo e outros requisitos podem indicar qual interface é usada.
ms.assetid: 42843e02-b685-492e-9046-aea460e84584
ms.tgt_platform: multiple
keywords:
- ADSI de interfaces de consulta
- Consultas ADSI, interfaces de consulta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 805303a972b4a8140a9e632857287aeebca9b32f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822190"
---
# <a name="query-interfaces"></a><span data-ttu-id="fb673-106">Interfaces de consulta</span><span class="sxs-lookup"><span data-stu-id="fb673-106">Query Interfaces</span></span>

<span data-ttu-id="fb673-107">Três tipos de interfaces ADSI podem ser usados para executar pesquisas de diretório.</span><span class="sxs-lookup"><span data-stu-id="fb673-107">Three types of ADSI interfaces can be used to perform directory searches.</span></span> <span data-ttu-id="fb673-108">O ambiente de aplicativo e outros requisitos podem indicar qual interface é usada.</span><span class="sxs-lookup"><span data-stu-id="fb673-108">The application environment and other requirements may indicate which interface is used.</span></span>

-   <span data-ttu-id="fb673-109">[**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch).</span><span class="sxs-lookup"><span data-stu-id="fb673-109">[**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch).</span></span> <span data-ttu-id="fb673-110">O **IDirectorySearch** é uma interface com básica disponível apenas para programadores C/C++.</span><span class="sxs-lookup"><span data-stu-id="fb673-110">**IDirectorySearch** is a basic COM interface only available to C/C++ programmers.</span></span> <span data-ttu-id="fb673-111">Para obter mais informações, consulte [pesquisando com a interface IDirectorySearch](searching-with-idirectorysearch.md).</span><span class="sxs-lookup"><span data-stu-id="fb673-111">For more information, see [Searching With the IDirectorySearch Interface](searching-with-idirectorysearch.md).</span></span>
-   <span data-ttu-id="fb673-112">Data.</span><span class="sxs-lookup"><span data-stu-id="fb673-112">ADO.</span></span> <span data-ttu-id="fb673-113">As interfaces ADO (ActiveX Data Object) são interfaces de automação que usam OLE DB.</span><span class="sxs-lookup"><span data-stu-id="fb673-113">The ActiveX Data Object (ADO) interfaces are Automation interfaces that use OLE DB.</span></span> <span data-ttu-id="fb673-114">Use o ADO para consultas em aplicativos que dependem da automação.</span><span class="sxs-lookup"><span data-stu-id="fb673-114">Use ADO for queries within applications that rely on Automation.</span></span> <span data-ttu-id="fb673-115">Isso inclui Visual Basic aplicativos, Active Server páginas e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="fb673-115">These include Visual Basic applications, Active Server Pages, and so on.</span></span> <span data-ttu-id="fb673-116">Para obter mais informações, consulte [pesquisando com ActiveX Data Objects](searching-with-activex-data-objects-ado.md).</span><span class="sxs-lookup"><span data-stu-id="fb673-116">For more information, see [Searching with ActiveX Data Objects](searching-with-activex-data-objects-ado.md).</span></span>
-   <span data-ttu-id="fb673-117">OLE DB.</span><span class="sxs-lookup"><span data-stu-id="fb673-117">OLE DB.</span></span> <span data-ttu-id="fb673-118">OLE DB é um conjunto de interfaces C/C++ usado para consultar bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="fb673-118">OLE DB is a set of C/C++ interfaces used to query databases.</span></span> <span data-ttu-id="fb673-119">Ao dar suporte a essas interfaces, os provedores ADSI podem implementar recursos de OLE DB avançados, como consultas distribuídas com outros provedores de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="fb673-119">By supporting these interfaces, ADSI providers can implement advanced OLE DB features, such as distributed queries with other OLE DB providers.</span></span> <span data-ttu-id="fb673-120">Para obter mais informações, consulte [pesquisando com OLE DB](searching-with-ole-db.md).</span><span class="sxs-lookup"><span data-stu-id="fb673-120">For more information, see [Searching with OLE DB](searching-with-ole-db.md).</span></span>

 

 




