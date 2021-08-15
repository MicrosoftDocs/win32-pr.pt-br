---
title: Classe de objeto e categoria de objeto
description: Cada instância de uma classe de objeto tem uma propriedade objectClass com valores múltiplos que identifica a classe da qual o objeto é uma instância, bem como todas as superclasses estruturais ou abstratas das quais essa classe é derivada.
ms.assetid: b3c5f9ee-98e0-42dd-9b61-3731e14b9cd4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b35e7f461caa27e8668cfc47cd94852bf53b291658b828ea017e3dc00a19d39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185693"
---
# <a name="object-class-and-object-category"></a>Classe de objeto e categoria de objeto

Cada instância de uma classe de objeto tem uma propriedade [**objectClass**](/windows/desktop/ADSchema/a-objectclass) com valores múltiplos que identifica a classe da qual o objeto é uma instância, bem como todas as superclasses estruturais ou abstratas das quais essa classe é derivada. Assim, a propriedade **objectClass** de um objeto de usuário identificaria as classes [**Top**](/windows/desktop/ADSchema/c-top), [**Person**](/windows/desktop/ADSchema/c-person), [**OrganizationalPerson**](/windows/desktop/ADSchema/c-organizationalperson)e [**User**](/windows/desktop/ADSchema/c-user) . A propriedade **objectClass** não inclui classes auxiliares na lista. O sistema define o valor de **objectClass** quando a instância do objeto é criada e não pode ser alterada.

Cada instância de uma classe de objeto também tem uma propriedade [**objectCategory**](/windows/desktop/ADSchema/a-objectcategory) , que é uma propriedade de valor único que contém o nome distinto da classe da qual o objeto é uma instância ou uma de suas superclasses. Quando um objeto é criado, o sistema define sua propriedade **objectCategory** para o valor especificado pela propriedade [**defaultObjectCategory**](/windows/desktop/ADSchema/a-defaultobjectcategory) de sua classe de objeto. A propriedade **objectCategory** de um objeto não pode ser alterada.

Para obter mais informações e um exemplo de código que recupera a propriedade [**objectClass**](/windows/desktop/ADSchema/a-objectclass) de um objeto, consulte [recuperando o atributo objectClass](retrieving-the-objectclass-property.md).

> [!IMPORTANT]
> antes do Windows Server 2008, o atributo [**objectClass**](/windows/desktop/ADSchema/a-objectclass) não é indexado. Isso ocorre porque ele tem vários valores e é altamente não exclusivo; ou seja, cada instância do atributo **objectClass** inclui a classe [**Top**](/windows/desktop/ADSchema/c-top) . Isso significa que um índice seria muito grande e ineficaz. Para localizar objetos de uma determinada classe, use o atributo [**objectCategory**](/windows/desktop/ADSchema/a-objectcategory) , que é de valor único e indexado. Para obter mais informações sobre como usar essas propriedades em filtros de pesquisa, consulte [decidindo o que encontrar](deciding-what-to-find.md).

 

Para a maioria das classes, o [**defaultObjectCategory**](/windows/desktop/ADSchema/a-defaultobjectcategory) é o nome distinto do objeto [**classSchema**](/windows/desktop/ADSchema/c-classschema) da classe. Por exemplo, o **defaultObjectCategory** para a classe [**ORGANIZATIONALUNIT**](/windows/desktop/ADSchema/c-organizationalunit) é "CN = Organization-Unit, CN = Schema, cn = Configuration, <DC = forestroot>". No entanto, algumas classes referem-se a outra classe como sua **defaultObjectCategory**. Isso permite que uma consulta Localize prontamente grupos de objetos relacionados, mesmo que eles sejam de diferentes classes. Por exemplo, as classes [**User**](/windows/desktop/ADSchema/c-user), [**Person**](/windows/desktop/ADSchema/c-person), [**OrganizationalPerson**](/windows/desktop/ADSchema/c-organizationalperson)e [**Contact**](/windows/desktop/ADSchema/c-contact) identificam a classe **Person** em suas propriedades **defaultObjectCategory** . Isso permite que filtros de pesquisa como (objectCategory = Person) localizem instâncias de todas essas classes com uma única consulta. As consultas para pessoas são muito comuns, portanto, essa é uma otimização simples.

Se você criar uma subclasse de uma classe estrutural, a prática recomendada é definir o valor [**defaultObjectCategory**](/windows/desktop/ADSchema/a-defaultobjectcategory) da nova classe como o mesmo nome distinto da superclasse. Isso permite que a interface do usuário padrão "Localize" a subclasse.

 

 