---
description: Uma ação é executada no Windows Installer chamando a função MsiDoAction ou incluindo a ação em uma tabela de sequência.
ms.assetid: ee5bdc72-adf4-46f4-ae1f-4c41d22a1ed8
title: Usando ações padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f52118580f4e18f07f86bd15da73f9aafb453c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750589"
---
# <a name="using-standard-actions"></a>Usando ações padrão

Uma ação é executada no Windows Installer chamando a função [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) ou incluindo a ação em uma tabela de sequência. Como a maioria das ações encapsula uma única finalidade, a maneira mais comum de usar ações é ordenar uma série de ações em uma sequência para realizar uma tarefa maior. O instalador tem três ações de nível superior padrão que chamam um conjunto associado de tabelas de sequência. Essas tabelas de sequência associadas podem conter ações padrão, ações personalizadas e elementos de interface do usuário. Cada ação em uma tabela de sequência tem um número de sequência associado e também pode ter uma expressão condicional associada. Todas as ações em uma tabela de sequência são visitadas em ordem e são executadas somente se a expressão condicional for avaliada como true.

Embora uma ação padrão possa ter qualquer número de sequência associado a ela, muitas têm restrições de sequência que devem ser seguidas para que a ação funcione corretamente. Por exemplo, a [ação filecusto](filecost-action.md)deve ser chamada após a [ação CostInitialize](costinitialize-action.md). Para obter mais informações sobre as restrições de sequenciamento de ação padrão, consulte [ações com restrições de sequenciamento](actions-with-sequencing-restrictions.md), [ações sem restrições de sequenciamento](actions-without-sequencing-restrictions.md)ou [referência de ações padrão](standard-actions-reference.md).

Os tópicos a seguir fornecem mais informações sobre o uso de ações padrão.

-   [Publicando produtos, recursos e componentes](publishing-products-features-and-components.md)
-   [Pesquisa de arquivos](file-searching.md)
-   [Custo do arquivo](file-costing.md)
-   [Instalação de arquivo](file-installation.md)
-   [Modificando o registro](modifying-the-registry.md)
-   [Executando ações](running-actions.md)

Consulte também [sobre ações padrão](about-standard-actions.md) ou [referência de ações padrão](standard-actions-reference.md).

 

 



