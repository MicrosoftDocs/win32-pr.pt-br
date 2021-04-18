---
title: Problemas de associação para ambientes mistos
description: Problemas de associação para ambientes mistos
ms.assetid: d9f9a6bc-7733-4269-99c8-61a84b37d487
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, usando, problemas de associação para ambientes mistos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a65135e0562f387ee9b70e2395d807b639a48e37
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105756461"
---
# <a name="binding-issues-for-mixed-environments"></a>Problemas de associação para ambientes mistos

Para ambientes nos quais o domínio que contém Active Directory tem uma relação de confiança com um domínio do Windows NT 4,0, pode haver um problema ao usar a associação sem servidor para associar a objetos Active Directory.

Em alguns ambientes de rede, as relações de confiança foram configuradas entre controladores de domínio que contêm Active Directory e servidores Windows NT 4,0 com a finalidade de permitir a autenticação entre domínios. Nesses ambientes mistos, se um usuário, que é membro do Windows NT 4,0, o domínio tenta usar a associação sem servidor para se associar a um objeto de Active Directory em um domínio confiável, a ligação falhará e um erro será retornado. Isso ocorre porque uma ligação sem servidor usa a função [**DsGetDcName**](/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea) para associar ao objeto em Active Directory, que depende do DNS adequado.

Nesse cenário, o usuário do Windows NT deve fornecer o nome de um domínio específico ao qual associar. A seguir, é mostrado um exemplo.

``` syntax
LDAP://fabrikam.com/OU=Sales
```

 

 