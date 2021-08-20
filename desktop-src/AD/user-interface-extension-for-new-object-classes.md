---
title: Interface do Usuário extensão para novas classes de objeto
description: Active Directory Domain Services e sua interface do usuário de snap-in do MMC administrativa podem ser personalizadas para se adaptar aos requisitos de administradores e usuários.
ms.assetid: 38e3b800-20ad-4da8-ad40-4e90838acfb5
ms.tgt_platform: multiple
keywords:
- Interface do Usuário extensão do AD para novas classes de objeto
- Object AD , Interface do Usuário para novas classes de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dd2f703e22619c8c3738b51a7a1f1464ca7e7d86b655abccd4c26258ac85810
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118182706"
---
# <a name="user-interface-extension-for-new-object-classes"></a>Interface do Usuário extensão para novas classes de objeto

Active Directory Domain Services e sua interface do usuário de snap-in do MMC administrativa podem ser personalizadas para se adaptar aos requisitos de administradores e usuários. Active Directory Domain Services permitir que o esquema seja modificado criando novas classes e atributos ou modificando classes existentes. Especificadores de exibição para as classes podem ser modificados para refletir os novos elementos de interface do usuário que as modificações de esquema exigem.

A tabela a seguir lista atributos podem ser usados para modificar como os snap-ins administrativos exibirão objetos de uma classe específica.



| Atributo                  | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **defaultHidingValue**     | O **atributo defaultHidingValue** é um atributo de **um objeto classSchema.** Esse atributo contém um valor booliana que, se TRUE, faz com que instâncias da classe de objeto sejam ocultadas nos snap-ins administrativos e no shell Windows. Isso também significa que um item de menu para  a nova classe de objeto não aparece no menu Novo contexto dos snap-ins administrativos, mesmo que as propriedades apropriadas do assistente de criação sejam definidas no objeto **displaySpecifier** da nova classe de objeto. Se esse atributo for FALSE, as instâncias da classe estarão visíveis nos snap-ins administrativos e no shell. Isso também faz com que um item de menu crie uma nova instância de objeto a ser adicionada ao menu **Novo** dos snap-ins administrativos.<br/> Se nenhum valor for definido para esse atributo, o valor padrão será TRUE. Isso significa que, por padrão, as instâncias do objeto estão ocultas.<br/>                                                                |
| **showInAdvancedViewOnly** | O **atributo showInAdvancedViewOnly** contém um valor booliana que, se TRUE, faz com que instâncias da classe de objeto apareçam no snap-in Usuários e Computadores somente na Exibição Avançada e não apareçam no shell Windows. Se essa propriedade for FALSE, as instâncias da classe estarão visíveis na exibição Normal no snap-in Usuários e Computadores e no shell Windows.<br/> Se nenhum valor for definido para esse atributo, o valor padrão será TRUE.<br/> Esse atributo pode ser definido em um objeto individual para substituir o valor definido na classe de objeto. Por exemplo, a **classe Container** tem esse atributo definido como TRUE, mas o **contêiner User** tem esse valor definido como FALSE. Por isso,  o contêiner Usuário aparece no shell e na exibição Normal no snap-in Usuários e Computadores, mas outros contêineres que não têm **showInAdvancedViewOnly** definido como FALSE aparecem somente na exibição Avançado no snap-in Usuários e Computadores.<br/> |



 

## <a name="creating-display-specifiers-for-new-classes"></a>Criando especificadores de exibição para novas classes

Para personalizar a interface do usuário para uma nova classe, crie um objeto especificador de exibição para a nova classe para cada localidade com suporte e, em seguida, de definir os atributos desejados para o especificador de exibição.

## <a name="inheriting-display-specifiers-for-derived-classes"></a>Herdando especificadores de exibição para classes derivadas

Uma nova classe que herda de uma classe existente não herda o especificador de exibição da classe pai. Se a nova classe for usar algumas ou todas as propriedades do especificador de exibição da classe pai, crie um novo especificador de exibição para a nova classe e copie as propriedades do especificador de exibição da classe pai para o novo especificador de exibição de objeto. Isso deve ser feito para todas as localidades para as quais as propriedades do especificador de exibição da classe pai se aplicam.

Determinadas partes do conjunto de recursos da interface do usuário, como os itens de menu e o assistente de criação para a classe de usuário, são implementadas internamente e não estão disponíveis para uso por um objeto derivado. Nesses casos, é melhor estender uma classe existente do que usar uma classe derivada.

## <a name="modifying-existing-classes"></a>Modificando classes existentes

Novos atributos podem ser adicionados a uma classe existente. Novos componentes da interface do usuário (páginas de propriedades, itens de menu e nomes de exibição de atributo) podem ser adicionados ou a interface do usuário existente é substituída. Também é possível criar novas páginas de propriedades que expõem menos atributos de uma classe e para criar menus de contexto com menos ações. Para obter mais informações, consulte [Páginas](property-pages-for-use-with-display-specifiers.md)de propriedades para uso com especificadores de exibição, [Menus](context-menus-for-use-with-display-specifiers.md)de contexto para uso com especificadores de exibição e Nomes de [exibição de](class-and-attribute-display-names.md)classe e atributo .

 

 





