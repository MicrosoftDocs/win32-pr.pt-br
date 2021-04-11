---
title: Habilitando a associação de Rename-Safe com a propriedade otherWellKnownObjects
description: Objetos da classe de contêiner têm um atributo otherWellKnownObjects que você pode usar para associar um GUID com o DN (nome distinto) de um objeto filho no contêiner.
ms.assetid: 54f7468b-03e5-46b9-8b43-e3571dccdceb
ms.tgt_platform: multiple
keywords:
- Propriedade otherWellKnownObjects
- Propriedade otherWellKnownObjects, usando para associação de renomeação segura
- Active Directory, usando, associação, associação de renomeação segura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7114fa6dfb44625433d8da1c57491a13aefa7cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159328"
---
# <a name="enabling-rename-safe-binding-with-the-otherwellknownobjects-property"></a>Habilitando a associação de Rename-Safe com a propriedade otherWellKnownObjects

Objetos da classe de contêiner têm um atributo **otherWellKnownObjects** que você pode usar para associar um GUID com o DN (nome distinto) de um objeto filho no contêiner. Se o objeto filho for movido ou renomeado, o servidor de Active Directory atualizará o DN no valor **otherWellKnownObjects** para esse objeto filho. Isso permite o uso do recurso de associação WKGUID para associar ao objeto filho usando o GUID e o DN do contêiner em vez do DN do objeto filho.

O atributo **otherWellKnownObjects** é equivalente ao atributo **wellKnownObjects** , exceto que aplicativos e serviços podem gravar um valor **otherWellKnownObjects** , mas apenas o sistema pode gravar **wellKnownObjects**.

Usar o atributo **otherWellKnownObjects** e a associação WKGUID é benéfico nas seguintes situações em que a associação renomear-seguro é necessária em relação a um objeto de contêiner específico.

Se um objeto de contêiner contiver outros objetos importantes ou se objetos importantes puderem ser renomeados ou movidos.

Se os objetos importantes existirem para cada instância do objeto de contêiner. Por exemplo, o sistema usa o atributo **wellKnownObjects** de cada objeto **domainDns** para armazenar um valor para o contêiner Users, que existe em cada instância de um objeto **domainDns** . Isso permite que os aplicativos se associem ao contêiner de usuários em uma forma de renomeação segura, especificando o GUID bem conhecido e o DN do contêiner **domainDns** . Os aplicativos podem usar o atributo **otherWellKnownObjects** de um contêiner da mesma forma.

Se você precisar de uma associação de renomeação segura e/ou recurso de pesquisa nos objetos importantes.

**Para adicionar recursos de pesquisa e Associação de renomeação segura**

1.  Adicione um valor à propriedade **otherWellKnownObjects** do objeto de contêiner quando o objeto importante for criado dentro desse contêiner. O valor contém o GUID que representa o objeto bem conhecido. Lembre-se de que isso não é o **objectGUID** e o **distinguishedName** para esse objeto.
2.  Use o recurso de associação WKGUID para associar ou pesquisar o objeto importante.

O atributo **otherWellKnownObjects** pode ter vários valores e contém as tuplas GUID/DN de objetos bem conhecidos dentro dos contêineres nos quais eles estão definidos. O atributo **otherWellKnownObjects** tem a sintaxe DNWithBinary na qual os valores têm o seguinte formato:


```C++
B:<char count>:<well known GUID>:<object DN>
```



Neste exemplo, " &lt; contagem de caracteres &gt; " é a contagem de dígitos hexadecimais em " &lt; GUID bem conhecido &gt; ", que é 32 (número de dígitos hexadecimais em um GUID) para **otherWellKnownObjects** e **wellKnownObjects**. " &lt; GUID bem conhecido &gt; " é a representação de dígito HEXADECIMAL do GUID conhecido. " &lt; Object DN &gt; " é o nome distinto do objeto representado por esse valor de WKO. O servidor mantém a parte ObjectDN de cada valor de **wellKnownObjects** e **otherWellKnownObjects** para que ele contenha o nome distinto atual do objeto especificado originalmente quando o valor foi criado.

Por exemplo, se {df447b5e-aa5b-11D2-8D53-00c04f79ab81} for o GUID bem conhecido do objeto MyObject no contêiner MyContainer no domínio Fabrikam.com, o valor **otherWellKnownObjects** especificará o GUID bem conhecido e o DN de MyObject:


```C++
B:32:df447b5eaa5b11d28d5300c04f79ab81:cn=MyObject,cn=MyContainer,dc=Fabrikam,dc=com
```



Para associar a esse objeto, use a seguinte cadeia de vinculação WKGUID que especifica o GUID bem conhecido do objeto e o DN do contêiner:


```C++
LDAP://<WKGUID=df447b5eaa5b11d28d5300c04f79ab81,cn=MyContainer,dc=Fabrikam,dc=com>
```



Após a associação a esse objeto, você pode usar as interfaces COM do ADSI para pesquisar, ler, modificar ou excluir o objeto.

Para obter mais informações e um exemplo de código que mostra como adicionar um objeto ao atributo **otherWellKnownObjects** , consulte [exemplo de código para criar um objeto de contêiner](example-code-for-creating-a-container-object.md).

 

 




