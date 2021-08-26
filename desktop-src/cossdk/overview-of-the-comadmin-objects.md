---
description: Os objetos COMAdmin oferecem um modelo de objeto simples que fornece acesso ao catálogo COM+.
ms.assetid: 84cee7a7-f7a6-41a0-afd5-fae56365612e
title: Visão geral dos objetos COMAdmin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ad382fcfab6e53a2eb8bfec9914a070d8a78e6ef2a29253005c324c8df8257e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070386"
---
# <a name="overview-of-the-comadmin-objects"></a>Visão geral dos objetos COMAdmin

Os objetos COMAdmin oferecem um modelo de objeto simples que fornece acesso ao catálogo COM+. Ao fazer isso, eles servem para modelar toda a funcionalidade fornecida pela ferramenta administrativa serviços de componentes. Sempre que você fizer qualquer tipo de administração COM+, estará interagindo com o catálogo COM+. Para obter uma descrição do catálogo, consulte [acessando o catálogo com+](accessing-the-com--catalog.md).

As informações obtidas da ferramenta administrativa serviços de componentes ou usando os objetos COMAdmin são estruturadas da mesma forma, e as ações executadas em qualquer contexto são análogas. A correlação básica entre usar o snap-in Serviços de componentes e a administração programática é que as pastas na árvore de console do snap-in correspondem às coleções no catálogo COM+. Ou seja, assim como cada pasta no snap-in contém itens de um tipo; por exemplo, **os aplicativos com+** mantêm aplicativos com+ instalados – cada coleção no catálogo com+ contém itens de um tipo uniforme. Além disso, assim como cada item em uma pasta tem propriedades que podem ser definidas em uma folha de propriedades, cada item em uma coleção expõe as propriedades que podem ser definidas.

Para permitir que você configure objetos nessa estrutura, os objetos COMAdmin fornecem os meios para fazer o seguinte:

-   Acessar o catálogo COM+
-   Coleções de acesso no catálogo
-   Acessar itens em coleções
-   Acessar propriedades nos itens nas coleções

Para dar suporte a essas ações, a biblioteca COMAdmin fornece as três seguintes classes:

-   [**COMAdminCatalog**](comadmincatalog.md), que representa o próprio catálogo.
-   [**COMAdminCatalogCollection**](comadmincatalogcollection.md), que representa qualquer coleção.
-   [**COMAdminCatalogObject**](comadmincatalogobject.md), que representa qualquer item em uma coleção.

Para obter descrições mais completas dessas classes, consulte [descrição resumida das classes COMAdmin](summary-description-of-the-comadmin-classes.md) nesta seção.

Para ter uma ideia rápida das ações típicas executadas na administração programática, consulte [o exemplo introdutório usando o catálogo de administração do com+](introductory-example-using-the-com--administration-catalog.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Operações de administração COM+ em transações](com--administration-operations-within-transactions.md)
</dt> <dt>

[Manipulando erros de administração COM+](handling-com--administration-errors.md)
</dt> <dt>

[Exemplo introdutório usando o catálogo de administração do COM+](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[Recuperando coleções no catálogo COM+](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[Definindo propriedades e salvando alterações no catálogo COM+](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



