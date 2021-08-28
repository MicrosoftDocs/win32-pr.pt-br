---
description: Uma ação é executada no Windows Instalador chamando a função MsiDoAction ou incluindo a ação em uma tabela de sequência.
ms.assetid: ee5bdc72-adf4-46f4-ae1f-4c41d22a1ed8
title: Usando ações padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60696e79c12b054739d87ffe5696e898a8eb955c4c7bfe0aa9c2341db7c2d720
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996206"
---
# <a name="using-standard-actions"></a>Usando ações padrão

Uma ação é executada no Windows Instalador chamando a [**função MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) ou incluindo a ação em uma tabela de sequência. Como a maioria das ações encapsula uma única finalidade, a maneira mais comum de usar ações é ordenar uma série de ações em uma sequência para realizar uma tarefa maior. O instalador tem três ações padrão de nível superior que chamam um conjunto associado de tabelas de sequência. Essas tabelas de sequência associadas podem conter ações padrão, ações personalizadas e elementos de interface do usuário. Cada ação em uma tabela de sequência tem um número de sequência associado e também pode ter uma expressão condicional associada. Todas as ações em uma tabela de sequência são visitadas na ordem e só serão executadas se a expressão condicional for avaliada como True.

Embora uma ação padrão possa ter qualquer número de sequência associado a ela, muitos têm restrições de sequência que devem ser seguidas para que a ação funcione corretamente. Por exemplo, [a ação FileCost](filecost-action.md), deve ser chamada após a [ação CostInitialize](costinitialize-action.md). Para obter mais informações sobre restrições [](actions-with-sequencing-restrictions.md)de sequenciamento de ação padrão, consulte Ações com restrições de sequenciamento, [Ações](actions-without-sequencing-restrictions.md)sem restrições de sequenciamento ou Referência de [ações padrão](standard-actions-reference.md).

Os tópicos a seguir fornecem mais informações sobre como usar ações padrão.

-   [Publicando produtos, recursos e componentes](publishing-products-features-and-components.md)
-   [Pesquisa de arquivos](file-searching.md)
-   [Custo do arquivo](file-costing.md)
-   [Instalação de arquivo](file-installation.md)
-   [Modificando o Registro](modifying-the-registry.md)
-   [Executando ações](running-actions.md)

Consulte também [Sobre ações padrão ou](about-standard-actions.md) Referência de ações [padrão](standard-actions-reference.md).

 

 



