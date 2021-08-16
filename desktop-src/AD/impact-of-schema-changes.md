---
title: Impacto das alterações de esquema
description: Este tópico descreve como uma extensão de esquema afeta a floresta do Active Directory.
ms.assetid: df604fb4-9256-4028-86d3-4ae1bc680324
ms.tgt_platform: multiple
keywords:
- Impacto do AD de alterações de esquema
- schema AD , impacto da alteração do esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afa9cc0ee4cdcd0da3581d6bf009837799387949e43dc68989612442352df591
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187715"
---
# <a name="impact-of-schema-changes"></a>Impacto das alterações de esquema

Uma extensão de esquema afeta uma floresta de domínio controlada por Active Directory Domain Services de várias maneiras:

-   As alterações de esquema são globais. Há um único esquema para uma floresta inteira. O esquema é replicado globalmente: existe uma cópia do esquema em cada DC na floresta. Quando você estende o esquema, ele é estendido para toda a floresta.
-   As adições de objeto de esquema não podem ser revertidas. Quando uma nova classe ou objeto de atributo é adicionado ao esquema, ele não pode ser removido. Um atributo ou classe existente pode ser desabilitado, mas não removido. Para obter mais informações, [consulte Desabilitando classes e atributos existentes.](disabling-existing-classes-and-attributes.md) Desabilitar uma classe ou atributo não afeta instâncias existentes da classe ou atributo, mas impede a criação de novas instâncias. Você não poderá desabilitar um atributo se ele estiver incluído em qualquer classe que não está desabilitada.
-   Os OIDs devem ser exclusivos. Quando um atributo ou classe é adicionado ao esquema, nenhum atributo ou classe com o mesmo OID pode ser adicionado. Isso é verdadeiro mesmo que uma classe ou atributo tenha sido desabilitado. Por esse motivo, você deve usar OIDs válidos. Não sintetize um OID e não reutilizar um OID existente. Para obter mais informações sobre como obter um OID válido, consulte [Obtendo um identificador de objeto raiz](obtaining-an-object-identifier.md).
-   Algumas alterações podem ser feitas após a criação:

    -   Para uma classe de categoria 1 ou categoria 2, você pode adicionar ou remover valores no **atributo possSuperiors.** Os **valores possSuperiors** especificam as classes de objeto que podem conter a classe .
    -   Para uma classe de categoria 1 ou categoria 2, você pode adicionar ou remover valores no **atributo mayContain.** Os **valores mayContain** especificam os atributos opcionais, mas podem estar presentes em uma instância da classe .

-   O **lDAPDisplayName para** uma classe ou atributo de Categoria 2 pode ser alterado após sua criação. Normalmente, você não deve alterar **o lDAPDisplayName.** No entanto, há um motivo legítimo para alterar o nome LDAP e isso ocorre se você cometer um erro ao definir o atributo ou classe e deve criar um novo para substituir o antigo. Você não precisa renomear o RDN (nome diferenciado relativo) do atributo ou esquema de classe para fazer isso. Quando o nome LDAP é alterado, isso permite que você trabalhe com um erro em vez de recriar toda a infraestrutura Windows 2000. Para obter mais informações, [consulte Desabilitando classes e atributos existentes.](disabling-existing-classes-and-attributes.md)

    O **lDAPDisplayName para** classes ou atributos predefinidos (categoria 1) não pode ser alterado. Para obter mais informações sobre objetos de esquema de categoria 1 e 2, consulte [Restrições na extensão de esquema](restrictions-on-schema-extension.md).

 

 




