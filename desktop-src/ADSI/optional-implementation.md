---
title: Implementação opcional
description: Os recursos a seguir são opcionais, mas recomendado
ms.assetid: 6123bdda-06cf-4b8b-b2a8-89882b6341b4
ms.tgt_platform: multiple
keywords:
- ADSI de implementação opcional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 043b07f3a9bcfaef4bde8e95458d64828d4e46be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498600"
---
# <a name="optional-implementation"></a><span data-ttu-id="ec028-104">Implementação opcional</span><span class="sxs-lookup"><span data-stu-id="ec028-104">Optional Implementation</span></span>

<span data-ttu-id="ec028-105">Os recursos a seguir são opcionais, mas recomendados:</span><span class="sxs-lookup"><span data-stu-id="ec028-105">The following features are optional, but recommended:</span></span>

-   <span data-ttu-id="ec028-106">A interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) para clientes que não são de automação.</span><span class="sxs-lookup"><span data-stu-id="ec028-106">The [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface for non-Automation clients.</span></span> <span data-ttu-id="ec028-107">Como o provedor de OLE DB ADSI usa **IDirectorySearch** para apresentar consultas e coletar resultados do serviço de diretório subjacente, os provedores que implementam essa interface automaticamente fornecem acesso a bancos de dados de estilo OLE DB sem a necessidade de implementar interfaces adicionais.</span><span class="sxs-lookup"><span data-stu-id="ec028-107">Because the ADSI OLE DB provider uses **IDirectorySearch** to present queries and collect results from the underlying directory service, providers that implement this interface automatically provide access to OLE DB style databases without having to implement any additional interfaces.</span></span>
-   <span data-ttu-id="ec028-108">As interfaces [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)e [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) .</span><span class="sxs-lookup"><span data-stu-id="ec028-108">The [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist), and [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) interfaces.</span></span> <span data-ttu-id="ec028-109">Os provedores para serviços de diretório que dão suporte à segurança de objeto baseado em ACL são incentivados a implementar esses recursos adicionais.</span><span class="sxs-lookup"><span data-stu-id="ec028-109">Providers for directory services that support ACL-based object security are encouraged to implement these additional features.</span></span>

 

 




