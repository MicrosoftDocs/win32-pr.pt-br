---
title: Problemas de associação para ambientes mistos
description: Problemas de associação para ambientes mistos
ms.assetid: d9f9a6bc-7733-4269-99c8-61a84b37d487
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, usando, problemas de associação para ambientes mistos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 822795e050d2b69a3f7b60aac6847a150760f35cc62806c36f14d4d6c4694a47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118017990"
---
# <a name="binding-issues-for-mixed-environments"></a>Problemas de associação para ambientes mistos

para ambientes nos quais o domínio que contém Active Directory tem uma relação de confiança com um domínio Windows NT 4,0, pode haver um problema ao usar a associação sem servidor para associar a objetos Active Directory.

em alguns ambientes de rede, as relações de confiança foram configuradas entre controladores de domínio que contêm Active Directory e Windows NT servidores 4,0 com a finalidade de permitir a autenticação entre domínios. nesses ambientes mistos, se um usuário, que é membro do Windows NT 4,0, o domínio tenta usar a associação sem servidor para associar a um objeto de Active Directory em um domínio confiável, a ligação falhará e um erro será retornado. Isso ocorre porque uma ligação sem servidor usa a função [**DsGetDcName**](/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea) para associar ao objeto em Active Directory, que depende do DNS adequado.

nesse cenário, o usuário Windows NT deve fornecer o nome de um domínio específico ao qual associar. A seguir, é mostrado um exemplo.

``` syntax
LDAP://fabrikam.com/OU=Sales
```

 

 