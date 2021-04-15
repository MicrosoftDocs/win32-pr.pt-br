---
title: Impacto das alterações de esquema
description: Este tópico descreve como uma extensão de esquema afeta a floresta Active Directory.
ms.assetid: df604fb4-9256-4028-86d3-4ae1bc680324
ms.tgt_platform: multiple
keywords:
- Impacto do anúncio de alterações de esquema
- AD Schema, impacto da alteração do esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45aa43ed208b6eca5889220e09c78e8ada4a50a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105754016"
---
# <a name="impact-of-schema-changes"></a>Impacto das alterações de esquema

Uma extensão de esquema afeta uma floresta de domínio controlada por Active Directory Domain Services de várias maneiras:

-   As alterações de esquema são globais. Há um único esquema para uma floresta inteira. O esquema é replicado globalmente: existe uma cópia do esquema em todos os controladores de domínio na floresta. Quando você estende o esquema, ele é estendido para toda a floresta.
-   As adições de objeto de esquema não podem ser revertidas. Quando uma nova classe ou objeto de atributo é adicionado ao esquema, ele não pode ser removido. Um atributo ou classe existente pode ser desabilitado, mas não removido. Para obter mais informações, consulte [desabilitando classes e atributos existentes](disabling-existing-classes-and-attributes.md). Desabilitar uma classe ou atributo não afeta as instâncias existentes da classe ou do atributo, mas impede a criação de novas instâncias. Você não poderá desabilitar um atributo se ele estiver incluído em qualquer classe que não esteja desabilitada.
-   Os OIDs devem ser exclusivos. Quando um atributo ou classe é adicionado ao esquema, nenhum atributo ou classe com o mesmo OID pode ser adicionado. Isso é verdadeiro mesmo que uma classe ou um atributo tenha sido desabilitado. Por esse motivo, é necessário usar OIDs válidos. Não sintetiza um OID e não reutiliza um OID existente. Para obter mais informações sobre como obter um OID válido, consulte [obtendo um identificador de objeto raiz](obtaining-an-object-identifier.md).
-   Algumas alterações podem ser feitas após a criação:

    -   Para uma classe categoria 1 ou categoria 2, você pode adicionar ou remover valores no atributo **possSuperior** . Os valores de **possSuperior** especificam as classes de objeto que podem conter a classe.
    -   Para uma classe categoria 1 ou categoria 2, você pode adicionar ou remover valores no atributo **mayContain** . Os valores de **mayContain** especificam os atributos opcionais, mas podem estar presentes em uma instância da classe.

-   O **lDAPDisplayName** para uma classe ou atributo de categoria 2 pode ser alterado após ter sido criado. Normalmente, você não deve alterar o **lDAPDisplayName**. No entanto, há um motivo legítimo para alterar o nome LDAP e isso ocorre quando você cometeu um erro ao definir o atributo ou a classe e deve criar um novo para substituir o antigo. Você não precisa renomear o nome distinto relativo (RDN) do atributo ou do esquema de classe para fazer isso. Quando o nome LDAP é alterado, isso permite que você contorne um erro em vez de recompilar toda a sua infraestrutura do Windows 2000. Para obter mais informações, consulte [desabilitando classes e atributos existentes](disabling-existing-classes-and-attributes.md).

    O **lDAPDisplayName** para classes ou atributos predefinidos (categoria 1) não pode ser alterado. Para obter mais informações sobre objetos de esquema de categoria 1 e 2, consulte [restrições na extensão do esquema](restrictions-on-schema-extension.md).

 

 




