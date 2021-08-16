---
title: Implementação opcional
description: Os recursos a seguir são opcionais, mas recomendados
ms.assetid: 6123bdda-06cf-4b8b-b2a8-89882b6341b4
ms.tgt_platform: multiple
keywords:
- ADSI de implementação opcional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3074f3ef6b4d36713d483937ad0f6ef10167777a7c36f8d21427d7df2b0485a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838946"
---
# <a name="optional-implementation"></a>Implementação opcional

Os seguintes recursos são opcionais, mas recomendados:

-   A [**interface IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) para clientes que não são de Automação. Como o provedor de OLE DB ADSI usa **IDirectorySearch** para apresentar consultas e coletar resultados do serviço de diretório subjacente, os provedores que implementam essa interface fornecem automaticamente acesso a bancos de dados de estilo OLE DB sem precisar implementar nenhuma interface adicional.
-   As [**interfaces IADsSecurityDescriptor,**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)e [**IADsAccessControlEntry.**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) Os provedores de serviços de diretório que suportam a segurança de objeto baseada em ACL são incentivados a implementar esses recursos adicionais.

 

 




