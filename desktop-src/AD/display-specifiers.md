---
title: Exibir especificadores
description: Em Active Directory Domain Services, uma classe de objeto, ou classe, define um tipo de objeto que pode ser criado em Active Directory Domain Services.
ms.assetid: 0c31b02b-9fd3-4547-9ebc-d511a10d7106
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1be9df0b81427bafa6ebe6707a33e86b6aff7416
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103917139"
---
# <a name="display-specifiers"></a>Exibir especificadores

Em Active Directory Domain Services, uma classe de objeto, ou classe, define um tipo de objeto que pode ser criado em Active Directory Domain Services. A definição de cada classe de objeto é armazenada como um objeto [**classSchema**](/windows/desktop/ADSchema/c-classschema) no [esquema de Active Directory](active-directory-schema.md). Além da definição **classSchema** , cada classe de objeto pode ter um ou mais especificadores de exibição que especificam os dados da interface do usuário para objetos dessa classe.

Um especificador de exibição é um objeto da classe [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) . Os atributos de um objeto **displaySpecifier** especificam dados de interface do usuário localizados que descrevem os vários elementos da interface de usuários para uma classe de objeto específica. Os especificadores de exibição armazenam dados para folhas de propriedades, menus de contexto, ícones, assistentes de criação e nomes de classe e atributo localizados. Para páginas de propriedades e menus de contexto, o Shell do Windows e os snap-ins administrativos do Active Directory usam esses dados para formar diferentes interfaces de usuário para administradores e usuários finais — um conjunto de páginas de propriedades e/ou menus de contexto podem ser associados a aplicativos administrativos, enquanto um conjunto diferente de elementos pode ser associado a aplicativos do usuário final.

Os objetos [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) são armazenados em contêineres específicos de localidade no contêiner DisplaySpecifiers no contêiner de configuração, que é replicado para cada controlador de domínio na floresta da empresa. O contêiner DisplaySpecifiers tem sub-recipientes que correspondem às várias localidades com suporte da instalação Enterprise. Esses subcontêineres são nomeados usando identificadores de idioma. Por exemplo, o nome do contêiner de localidade para US-English é 409, que corresponde ao identificador de idioma hexadecimal, 0x0409. Assim, uma classe de objeto pode ter vários especificadores de exibição: um em cada subcontêiner de localidade. Para obter mais informações e uma lista de possíveis identificadores de idioma, consulte [constantes e cadeias de caracteres de identificador de linguagem](/windows/desktop/Intl/language-identifier-constants-and-strings). Para obter mais informações sobre localidades, consulte [localidades e idiomas](/windows/desktop/Intl/locales-and-languages).

O nome de um objeto [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) é formado acrescentando a cadeia de caracteres "-display" ao [**lDAPDisplayName**](/windows/desktop/ADSchema/a-ldapdisplayname) da classe Object. Por exemplo, o nome de um objeto **displaySpecifier** para a classe [**User**](/windows/desktop/ADSchema/c-user) é "user-Display".

Você pode adicionar, excluir ou modificar propriedades de objetos [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) de uma classe para especificar os elementos da interface do usuário (nome da classe, nomes de atributo, folhas de propriedades, menus de contexto, ícone e assim por diante) que aparecem para cada instância de um objeto dessa classe.

Para obter mais informações sobre especificadores de exibição, consulte [contêiner DisplaySpecifiers](displayspecifiers-container.md).

 

 