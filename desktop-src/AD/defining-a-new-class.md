---
title: Definindo uma nova classe
description: Quando você define uma nova classe, especifique as classes pai legais da nova classe, ou seja, as classes que podem conter instâncias da nova classe.
ms.assetid: 24e346b3-2de2-41f9-a0a2-7b7d8ab5668b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 069d6c0ede945c39a00111cd43ece8257031b3aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915958"
---
# <a name="defining-a-new-class"></a>Definindo uma nova classe

Quando você define uma nova classe, especifique as classes pai legais da nova classe, ou seja, as classes que podem conter instâncias da nova classe. As classes pai legais são especificadas nos atributos **possSuperior** e **systemPossSuperiors** da nova classe, bem como nos superiores possíveis herdados de suas superclasses, mas não de classes auxiliares.

Seja específico ao definir as classes pai legais para a nova classe. Decida onde você deseja que os usuários criem instâncias da sua classe. Por exemplo, especificar "contêiner" como um pai legal permitirá que o usuário crie instâncias em qualquer um dos contêineres padrão (**contêiner**, **OrganizationalUnit** e assim por diante), enquanto especificar "computador" permitiria que instâncias fossem criadas somente em instâncias do objeto de **computador** .

**Para criar uma classe**

1.  Escolha um nome para a classe. Para obter mais informações sobre como compor um nome de exibição de nome comum e de LDAP para uma nova classe, consulte [nomenclatura de atributos e classes](naming-attributes-and-classes.md).
2.  Obtenha um OID (identificador de objeto) para a classe. Para obter mais informações, consulte [obtendo um identificador de objeto](obtaining-an-object-identifier.md).
3.  Escolha uma "categoria de objeto padrão" para a classe. Para obter mais informações, consulte [classe de objeto e categoria de objeto](object-class-and-object-category.md).
4.  Escolha uma "categoria de classe de objeto" para a classe. Isso indica se a classe é abstrata, estrutural ou auxiliar. Para obter mais informações, consulte [classes estruturais, abstratas e auxiliares](structural-abstract-and-auxiliary-classes.md).
5.  Crie um novo objeto **classSchema** . Muitos atributos podem ser definidos para um objeto **classSchema** . Os seguintes atributos são essenciais para a definição de uma nova classe:

    -   Classes das quais a nova classe herda: **listas SubClassOf**, **auxiliaryClass** e **systemAuxiliaryClass**
    -   Nomes e identificadores para a nova classe: **CN**, **lDAPDisplayName**, **adminDisplayName**, **schemaIDGUID**, **governsID**
    -   Possíveis atributos da nova classe: **mustContain**, **systemMustContain**, **mayContain**, **systemMayContain**
    -   Possíveis pais da nova classe: **possSuperior**, **systemPossSuperiors**
    -   **objectClassCategory**
    -   **defaultObjectCategory**
    -   **defaultocultarvalue**
    -   **rDnAttId**
    -   **defaultSecurityDescriptor**
    -   **Descrição** (opcional)

    Para obter mais informações e descrições desses atributos, consulte [características das classes de objeto](characteristics-of-object-classes.md).

    Lembre-se de que as classes especificadas em **listas SubClassOf**, **possSuperior**, **systemPossSuperiors**, **auxiliaryClass** e **systemAuxiliaryClass** devem existir quando a nova classe for gravada no diretório; caso contrário, o objeto **classSchema** não será adicionado ao diretório. Da mesma forma, os atributos especificados em **mustContain**, **systemMustContain**, **mayContain** e **systemMayContain** devem existir ou a operação de criação de classe falhará.

6.  Grave o novo objeto **classSchema** no diretório.

**Para adicionar um atributo à propriedade mayContain**

1.  Obtenha o objeto **classSchema** para a classe a ser modificada.
2.  Adicione o novo atributo à propriedade de valores múltiplos **mayContain** .
3.  Grave o objeto **classSchema** alterado de volta no diretório.

Novos atributos podem ser criados ao mesmo tempo que novas classes; a ordem de criação dos novos atributos e classes é importante. Para obter mais informações, consulte [o que a instalação deve fazer](what-the-installation-must-do.md).

**Para adicionar novos atributos e novas classes ao mesmo tempo**

1.  Defina todos os novos atributos primeiro. Para obter mais informações, consulte [definindo um novo atributo](defining-a-new-attribute.md).
2.  Atualize o cache de esquema antes de definir novas classes. Para obter mais informações, consulte [atualizando o cache de esquema](updating-the-schema-cache.md).
3.  Crie as novas classes.
4.  Adicione os atributos desejados às novas classes.
5.  Atualize o cache de esquema novamente.

 

 




