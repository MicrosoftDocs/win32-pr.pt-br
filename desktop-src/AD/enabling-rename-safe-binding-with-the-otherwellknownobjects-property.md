---
title: Habilitando Rename-Safe associação com a outra propriedadeWellKnownObjects
description: Os objetos da classe Container têm um outro atributoWellKnownObjects que você pode usar para associar um GUID ao DN (nome diferenciado) de um objeto filho no contêiner.
ms.assetid: 54f7468b-03e5-46b9-8b43-e3571dccdceb
ms.tgt_platform: multiple
keywords:
- propriedade otherWellKnownObjects
- propriedade otherWellKnownObjects, usando para associação rename-safe
- Active Directory, usando, associação, renomear associação segura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 446f669adc9a59f9f8aba93e852546fe3991952857469d6f37978d9cf91a7666
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118695315"
---
# <a name="enabling-rename-safe-binding-with-the-otherwellknownobjects-property"></a>Habilitando Rename-Safe associação com a outra propriedadeWellKnownObjects

Os objetos da classe Container têm um **outro atributoWellKnownObjects** que você pode usar para associar um GUID ao DN (nome diferenciado) de um objeto filho no contêiner. Se o objeto filho for movido ou renomeado, o servidor do Active Directory atualizará o DN no outro **valorWellKnownObjects** para esse objeto filho. Isso permite o uso do recurso de associação WKGUID para se vincular ao objeto filho usando o GUID e o DN do contêiner em vez do DN do objeto filho.

O outro **atributoWellKnownObjects** é equivalente ao atributo **wellKnownObjects,** exceto que os aplicativos e serviços podem gravar um outro **valorWellKnownObjects,** mas somente o sistema pode escrever **wellKnownObjects**.

Usar **outro atributoWellKnownObjects** e a associação WKGUID é benéfico nas situações a seguir em que a associação de renomear-safe é necessária em relação a um objeto de contêiner específico.

Se um objeto de contêiner contiver outros objetos importantes ou se objetos importantes puderem ser renomeados ou movidos.

Se os objetos importantes existirem para cada instância do objeto de contêiner. Por exemplo, o sistema usa o atributo **wellKnownObjects** de cada objeto **domainDNS** para armazenar um valor para o contêiner Usuários, que existe em cada instância de um objeto **domainDNS.** Isso permite que os aplicativos se a vinifiquem ao contêiner Usuários de maneira segura de renomeação especificando o GUID conhecido e o DN do contêiner **domainDNS.** Os aplicativos podem usar o **atributo otherWellKnownObjects de** um contêiner da mesma forma.

Se você precisar renomear a associação segura e/ou a funcionalidade de pesquisa nos objetos importantes.

**Para adicionar recursos de associação e pesquisa com segurança de renomear**

1.  Adicione um valor à **outra propriedadeWellKnownObjects** do objeto de contêiner quando o objeto importante for criado dentro desse contêiner. O valor contém o GUID que representa o objeto conhecido. Esteja ciente de que esse não é **o objectGUID** e **o distinguishedName** para esse objeto.
2.  Use o recurso de associação WKGUID para se vincular ou pesquisar o objeto importante.

O **outro atributoWellKnownObjects** pode ter vários valores e contém as tuplas GUID/DN de objetos conhecidos dentro dos contêineres nos quais estão definidos. O **outro atributoWellKnownObjects** tem a sintaxe DNWithBinary na qual os valores têm o seguinte formato:


```C++
B:<char count>:<well known GUID>:<object DN>
```



Neste exemplo, " contagem de caracteres " é a contagem de dígitos hexadecimais em " GUID bem conhecido ", que é 32 (número de dígitos hexadecimais em um GUID) para ambos &lt; &gt; os &lt; &gt; **outrosWellKnownObjects** e **wellKnownObjects**. " GUID conhecido " é a representação de dígito &lt; &gt; hexadecimal do GUID conhecido. " &lt; object DN &gt; " é o nome diferenciado do objeto representado por esse valor WKO. O servidor mantém a parte ObjectDN de cada **wellKnownObjects** e outro **valorWellKnownObjects** para que ele contenha o nome diferenciado atual do objeto originalmente especificado quando o valor foi criado.

Por exemplo, se {df447b5e-aa5b-11d2-8d53-00c04f79ab81} for o GUID conhecido do objeto MyObject no contêiner MyContainer no domínio Fabrikam.com, o outro **valorWellKnownObjects** especificará o GUID conhecido e o DN de MyObject:


```C++
B:32:df447b5eaa5b11d28d5300c04f79ab81:cn=MyObject,cn=MyContainer,dc=Fabrikam,dc=com
```



Para se vincular a esse objeto, use a seguinte cadeia de caracteres de associação WKGUID que especifica o GUID conhecido do objeto e o DN do contêiner:


```C++
LDAP://<WKGUID=df447b5eaa5b11d28d5300c04f79ab81,cn=MyContainer,dc=Fabrikam,dc=com>
```



Após a associação a esse objeto, você pode usar as interfaces COM ADSI para pesquisar, ler, modificar ou excluir o objeto.

Para obter mais informações e um exemplo de código que mostra como adicionar um objeto ao outro **atributoWellKnownObjects,** consulte Código de exemplo para criar um [objeto de contêiner](example-code-for-creating-a-container-object.md).

 

 




