---
description: Cada item em uma coleção expõe propriedades.
ms.assetid: d9af57ea-c5b3-4017-bdc2-e43b86b3ddcd
title: Editando propriedades no catálogo COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50ace2809fef4510a9c89b5faf31df555cb76426a06dd445aff9438c0d19e887
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546223"
---
# <a name="editing-properties-in-the-com-catalog"></a>Editando propriedades no catálogo COM+

Cada item em uma coleção expõe propriedades. Essas propriedades servem para manter os dados de configuração para qualquer elemento que o item representa. Na ferramenta administrativa serviços de componentes, essas propriedades aparecem em uma página de propriedades que você acessa clicando com o botão direito do mouse em um item em uma pasta.

Como os itens em uma determinada coleção representam o mesmo tipo de coisa, esses itens expõem um conjunto de propriedades que é consistente na coleção. Por exemplo, a coleção de [**aplicativos**](applications.md) expõe uma propriedade Name, uma propriedade AppID e assim por diante. Isso é análogo a como cada aplicativo na ferramenta administrativa serviços de componentes tem uma página de propriedades estruturada consistentemente disponível para ele. Para obter uma lista de propriedades disponíveis para a coleção de **aplicativos** , consulte **aplicativos**. Para obter uma lista de propriedades disponíveis para a coleção de [**componentes**](components.md) , consulte **componentes**.

Para obter uma lista completa das propriedades expostas por itens em cada coleção, consulte [coleções de administração do com+](com--administration-collections.md).

Você representa um item em uma coleção usando um objeto criado a partir da classe [**COMAdminCatalogObject**](comadmincatalogobject.md) . Esse objeto permite que você defina e obtenha qualquer uma das propriedades expostas pelo item. Ao definir propriedades, também é possível que você esteja contendendo com outro gravador para o catálogo COM+. Para obter mais informações, consulte [obtendo e Configurando Propriedades](getting-and-setting-properties.md).

Depois de definir as propriedades, nenhuma alteração será realmente confirmada até que você salve explicitamente as alterações. Para obter mais informações, consulte [salvando ou descartando alterações](saving-or-discarding-changes.md).

Quando você salva as alterações, o catálogo COM+ impõe algumas lógicas de configuração para garantir que você não defina coisas para configurações incompatíveis. Ele também altera algumas propriedades para você quando você altera explicitamente determinadas propriedades. Para obter mais informações, consulte [interdependências entre Propriedades](interdependencies-between-properties.md).

Além disso, o COM+ tem um recurso que permite a consulta dinâmica para ver quais propriedades estão disponíveis para os itens em uma determinada coleção. Para obter detalhes, consulte [consultando as propriedades disponíveis](querying-for-available-properties.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Operações de administração COM+ em transações](com--administration-operations-within-transactions.md)
</dt> <dt>

[Manipulando erros de administração COM+](handling-com--administration-errors.md)
</dt> <dt>

[Exemplo introdutório usando o catálogo de administração do COM+](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[Visão geral dos objetos COMAdmin](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Recuperando coleções no catálogo COM+](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



