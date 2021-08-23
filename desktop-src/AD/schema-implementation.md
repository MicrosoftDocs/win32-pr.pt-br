---
title: Implementação de esquema
description: No Active Directory Domain Services, as definições de classe e de atributo são armazenadas no diretório como instâncias das classes classSchema e attributeSchema, respectivamente.
ms.assetid: 917f8e65-df2c-457e-bfd8-3f1ce0d0fbae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2d35d29b4e10d27b1369c0f064e17a0ed4430cbe2d6cc59329380724cd444e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025014"
---
# <a name="schema-implementation"></a>Implementação de esquema

No Active Directory Domain Services, as definições de classe e de atributo são armazenadas no diretório como instâncias das classes [**classSchema**](/windows/desktop/ADSchema/c-classschema) e [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) , respectivamente. **classSchema** e **attributeSchema** são classes definidas no esquema. Para manipular o esquema de Active Directory, use as mesmas operações LDAP usadas para manipular outro objeto. Como o esquema é uma parte fundamental do diretório que afeta toda a floresta, restrições especiais se aplicam a extensões de esquema. Para obter mais informações sobre restrições, consulte [restrições em extensões de esquema](restrictions-on-schema-extension.md).

Para resumir a implementação do esquema:

-   As instâncias da classe [**classSchema**](/windows/desktop/ADSchema/c-classschema) definem cada classe de objeto com suporte pelo Active Directory Domain Services. Os atributos de um objeto **classSchema** , por exemplo, seus [**atributos mayContain**](/windows/desktop/ADSchema/a-maycontain) e [**mustContain**](/windows/desktop/ADSchema/a-mustcontain) , descrevem uma classe de objeto, da mesma forma que os atributos de um objeto de usuário, por exemplo, seus atributos [**userPrincipalName**](/windows/desktop/ADSchema/a-userprincipalname) e [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber) , descrevem esse usuário. Para obter mais informações, consulte [características das classes de objeto](characteristics-of-object-classes.md).
-   As instâncias da classe [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) são usadas para definir cada atributo com suporte pelo Active Directory Domain Services. Os atributos de um objeto **attributeSchema** , por exemplo, seus atributos **attributeSyntax** e **isSingleValued** , descrevem um atributo, da mesma forma que os atributos de um objeto de usuário descrevem esse usuário. Para obter mais informações, consulte [características dos atributos](characteristics-of-attributes.md).
-   As instâncias das classes [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) e [**classSchema**](/windows/desktop/ADSchema/c-classschema) são armazenadas em um local bem conhecido no diretório, o contêiner de esquema. O contêiner de esquema sempre tem um nome distinto do formulário:

    ```C++
    CN=Schema,CN=Configuration,<DC=forestroot>
    ```

    

    em que " &lt; DC = forestroot &gt; " é o nome distinto da raiz da floresta, por exemplo, "DC = Fabrikam, DC = com".

    Para obter o nome distinto do contêiner de esquema, leia o atributo **schemaNamingContext** de RootDSE. Para obter mais informações sobre rootDSE e seus atributos, consulte [associação sem servidor e RootDSE](serverless-binding-and-rootdse.md).

Ao pensar sobre o esquema, lembre-se:

-   As alterações de esquema são globais. Há um único esquema para uma floresta inteira. O esquema é replicado globalmente: existe uma cópia do esquema em cada controlador de domínio na floresta. Ao estender o esquema, você o faz para toda a floresta.
-   As adições de esquema não são reversível. Quando uma nova classe ou atributo é adicionado ao esquema, ele não pode ser removido. Um atributo ou classe existente pode ser desabilitado, mas não removido. Para obter mais informações, consulte [desabilitando classes e atributos existentes](disabling-existing-classes-and-attributes.md).
-   Desabilitar uma classe ou atributo não afeta as instâncias existentes da classe ou do atributo, mas impede que novas instâncias sejam criadas. Você não poderá desabilitar um atributo se ele estiver incluído em qualquer classe que não esteja desabilitada.

 

 