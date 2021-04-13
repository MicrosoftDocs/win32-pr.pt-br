---
title: Adicionando usuários a um grupo
description: Joe Worden, administrador corporativo, agora adicionará Julie Bankert ao grupo de gerenciamento. Para adicionar um objeto a um grupo, use o método IADs. Add.
ms.assetid: 57a9f5b2-2e48-401d-8d3b-eceb711a1df9
ms.tgt_platform: multiple
keywords:
- Adicionar usuários a um grupo ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ea0ac78c0175248cb12e0f47a94ae60e7f1d16c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291804"
---
# <a name="adding-users-to-a-group"></a>Adicionando usuários a um grupo

Joe Worden, administrador corporativo, agora adicionará Julie Bankert ao grupo de gerenciamento. Para adicionar um objeto a um grupo, use o método [**IADs. Add**](/windows/desktop/api/Iads/nf-iads-iadsgroup-add) .


```VB
Dim grp as IADsGroup

Set grp = GetObject("LDAP://CN=Management,OU=Sales,DC=Fabrikam,DC=COM") 
grp.Add ("LDAP://CN=Julie Bankert,OU=Sales,DC=Fabrikam,DC=COM")
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando um novo grupo](creating-a-new-group.md)
</dt> </dl>

 

 




