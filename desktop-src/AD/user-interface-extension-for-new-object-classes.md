---
title: Extensão da interface do usuário para novas classes de objeto
description: Active Directory Domain Services e sua interface do usuário do snap-in administrativo do MMC podem ser personalizadas para se adaptar aos requisitos de administradores e usuários.
ms.assetid: 38e3b800-20ad-4da8-ad40-4e90838acfb5
ms.tgt_platform: multiple
keywords:
- Extensão da interface do usuário para o novo AD de classes de objeto
- ANÚNCIO de objeto, extensão de interface do usuário para novas classes de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 154b64a23eff72bf5751085a8e50691cd222abd6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915929"
---
# <a name="user-interface-extension-for-new-object-classes"></a>Extensão da interface do usuário para novas classes de objeto

Active Directory Domain Services e sua interface do usuário do snap-in administrativo do MMC podem ser personalizadas para se adaptar aos requisitos de administradores e usuários. Active Directory Domain Services habilitar o esquema a ser modificado criando novas classes e atributos, ou modificando classes existentes. Os especificadores de exibição para as classes podem ser modificados para refletir os novos elementos da interface do usuário que as modificações de esquema exigem.

A tabela a seguir lista os atributos que podem ser usados para modificar como os snap-ins administrativos exibirão objetos de uma classe específica.



| Atributo                  | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **defaultocultarvalue**     | O atributo **Defaultocultarvalue** é um atributo de um objeto **classSchema** . Esse atributo contém um valor booliano que, se verdadeiro, faz com que instâncias da classe de objeto sejam ocultadas nos snap-ins administrativos e no Shell do Windows. Isso também significa que um item de menu para a nova classe de objeto não aparece no **novo** menu de contexto dos snap-ins administrativos, mesmo que as propriedades apropriadas do assistente de criação sejam definidas no objeto **displaySpecifier** da nova classe de objeto. Se esse atributo for FALSE, as instâncias da classe ficarão visíveis nos snap-ins administrativos e no Shell. Isso também faz com que um item de menu crie uma nova instância de objeto a ser adicionada ao **novo** menu dos snap-ins administrativos.<br/> Se nenhum valor for definido para esse atributo, o valor padrão será TRUE. Isso significa que, por padrão, as instâncias do objeto ficam ocultas.<br/>                                                                |
| **showInAdvancedViewOnly** | O atributo **showInAdvancedViewOnly** contém um valor booliano que, se verdadeiro, faz com que as instâncias da classe de objeto apareçam no snap-in usuários e computadores somente na exibição avançada e não apareçam no Shell do Windows. Se essa propriedade for falsa, as instâncias da classe ficarão visíveis no modo de exibição normal no snap-in usuários e computadores e no Shell do Windows.<br/> Se nenhum valor for definido para esse atributo, o valor padrão será TRUE.<br/> Esse atributo pode ser definido em um objeto individual para substituir o valor definido na classe de objeto. Por exemplo, a classe de **contêiner** tem esse atributo definido como true, mas o contêiner de **usuário** tem esse valor definido como false. Por isso, o contêiner de **usuário** aparece no Shell e no modo de exibição normal no snap-in usuários e computadores, mas outros contêineres que não têm **SHOWINADVANCEDVIEWONLY** definido como false aparecem somente no modo de exibição avançado no snap-in usuários e computadores.<br/> |



 

## <a name="creating-display-specifiers-for-new-classes"></a>Criando especificadores de exibição para novas classes

Para personalizar a interface do usuário para uma nova classe, crie um objeto de especificador de exibição para a nova classe para cada localidade com suporte e, em seguida, defina os atributos desejados para o especificador de exibição.

## <a name="inheriting-display-specifiers-for-derived-classes"></a>Herdando especificadores de exibição para classes derivadas

Uma nova classe que herda de uma classe existente não herda o especificador de exibição da classe pai. Se a nova classe for usar algumas ou todas as propriedades do especificador de exibição de classe pai, crie um novo especificador de exibição para a nova classe e copie as propriedades do especificador de exibição da classe pai para o novo especificador de exibição de objeto. Isso deve ser feito para todas as localidades para as quais as propriedades do especificador de exibição da classe pai se aplicam.

Determinadas partes do conjunto de recursos da interface do usuário, como os itens de menu e o assistente de criação da classe User, são implementadas internamente e não estão disponíveis para uso por um objeto derivado. Nessas instâncias, é melhor estender uma classe existente do que usar uma classe derivada.

## <a name="modifying-existing-classes"></a>Modificando classes existentes

Novos atributos podem ser adicionados a uma classe existente. Novos componentes da interface do usuário (páginas de propriedades, itens de menu e nomes de exibição de atributo) podem ser adicionados ou a interface do usuário existente foi substituída. Também é possível criar novas páginas de propriedades que exponham menos atributos de uma classe e criar menus de contexto com menos ações. Para obter mais informações, consulte [páginas de propriedades para uso com especificadores de exibição](property-pages-for-use-with-display-specifiers.md), [menus de contexto para uso com especificadores de exibição](context-menus-for-use-with-display-specifiers.md)e nomes de exibição de [classe e atributo](class-and-attribute-display-names.md).

 

 





