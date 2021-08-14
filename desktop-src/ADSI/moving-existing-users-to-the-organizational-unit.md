---
title: Movendo usuários existentes para a unidade organizacional
description: Quando o administrador corporativo, Joe Worden, atualiza o domínio Windows NT 4.0 para o Active Directory, todos os usuários e grupos são migrados para os contêineres Usuários no domínio fabrikam.
ms.assetid: 230a594f-70c2-4ab6-a7e8-d5a77f2d6dd1
ms.tgt_platform: multiple
keywords:
- Movendo usuários existentes para o AD da Unidade Organizacional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d26104feb5d4c8b6a1f24176ce23fcbb6ef6a965ca29c58887f02724b3ccba8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118178950"
---
# <a name="moving-existing-users-to-the-organizational-unit"></a>Movendo usuários existentes para a unidade organizacional

Quando o administrador corporativo, Joe Worden, atualiza o domínio Windows NT 4.0 para o Active Directory, todos os usuários e grupos são migrados para os contêineres Usuários no domínio fabrikam. Joe agora pode mover esses usuários e grupos para as unidades organizacionais apropriadas. Um objeto também pode ser movido entre domínios Windows 2000 relacionados usando ADSI.

No exemplo de código a seguir, Joe move "jeffsmith" para a organização Sales.


```VB
Set usr = salesOU.MoveHere("LDAP://CN=jeffsmith,CN=Users,DC=fabrikam,DC=com", vbNullString)
```



O [**método IADsContainer.MoveHere**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere) leva o ADsPath do objeto a ser movido e o novo nome do objeto (RDN). Para manter o mesmo nome, você pode especificar **NULL** (**vbNullString**) para o *parâmetro bstrNewName.* Para renomear o objeto quando ele for movido, especifique o novo nome diferenciado relativo para o *parâmetro bstrNewName.* Por exemplo, para mover jeffsmith para a organização de vendas e renomear o objeto "jeffsmith" para "jeff smith" na mesma operação, Joe executaria \_ o seguinte código:


```VB
Set usr = salesOU.MoveHere("LDAP://CN=jeffsmith,CN=Users,DC=Fabrikam,DC=com", "CN=jeff_smith")
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando novos usuários na unidade organizacional](creating-new-users-in-the-organizational-unit.md)
</dt> </dl>

 

 




