---
title: Movendo usuários existentes para a unidade organizacional
description: Quando o administrador corporativo, Joe Worden, atualiza o domínio do Windows NT 4,0 para Active Directory, todos os usuários e grupos são migrados para os contêineres de usuários no domínio da Fabrikam.
ms.assetid: 230a594f-70c2-4ab6-a7e8-d5a77f2d6dd1
ms.tgt_platform: multiple
keywords:
- Movendo usuários existentes para o AD da unidade organizacional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 535ff7110eaf956f108854e8442faa7386667346
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159294"
---
# <a name="moving-existing-users-to-the-organizational-unit"></a>Movendo usuários existentes para a unidade organizacional

Quando o administrador corporativo, Joe Worden, atualiza o domínio do Windows NT 4,0 para Active Directory, todos os usuários e grupos são migrados para os contêineres de usuários no domínio da Fabrikam. Joe agora pode mover esses usuários e grupos para as unidades organizacionais apropriadas. Um objeto também pode ser movido entre domínios do Windows 2000 relacionados usando ADSI.

No exemplo de código a seguir, Joe move "jeffsmith" para a organização Sales.


```VB
Set usr = salesOU.MoveHere("LDAP://CN=jeffsmith,CN=Users,DC=fabrikam,DC=com", vbNullString)
```



O método [**IADsContainer. MoveHere**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere) usa o ADsPath do objeto a ser movido e o nome do novo objeto (RDN). Para manter o mesmo nome, você pode especificar **NULL** (**vbNullString**) para o parâmetro *bstrNewName* . Para renomear o objeto quando ele for movido, especifique o novo nome distinto relativo para o parâmetro *bstrNewName* . Por exemplo, para mover jeffsmith para a organização de vendas e renomear o objeto "jeffsmith" como "Jeff \_ Smith" na mesma operação, Joe executará o seguinte código:


```VB
Set usr = salesOU.MoveHere("LDAP://CN=jeffsmith,CN=Users,DC=Fabrikam,DC=com", "CN=jeff_smith")
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando novos usuários na unidade organizacional](creating-new-users-in-the-organizational-unit.md)
</dt> </dl>

 

 




