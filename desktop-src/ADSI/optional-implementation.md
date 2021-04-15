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
# <a name="optional-implementation"></a>Implementação opcional

Os recursos a seguir são opcionais, mas recomendados:

-   A interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) para clientes que não são de automação. Como o provedor de OLE DB ADSI usa **IDirectorySearch** para apresentar consultas e coletar resultados do serviço de diretório subjacente, os provedores que implementam essa interface automaticamente fornecem acesso a bancos de dados de estilo OLE DB sem a necessidade de implementar interfaces adicionais.
-   As interfaces [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)e [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) . Os provedores para serviços de diretório que dão suporte à segurança de objeto baseado em ACL são incentivados a implementar esses recursos adicionais.

 

 




