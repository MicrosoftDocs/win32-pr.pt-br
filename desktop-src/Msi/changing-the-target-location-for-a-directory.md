---
description: Se possível, a melhor maneira de especificar o local de destino de um diretório é criar a tabela de diretórios em seu pacote de instalação para fornecer o local correto. Para obter mais informações, consulte usando a tabela de diretórios.
ms.assetid: 2d16e036-2d7f-431d-b646-1addf2f65f3f
title: Alterando o local de destino de um diretório
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 818c4e9d555244dd1637e19eb249478f13ea2d48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169193"
---
# <a name="changing-the-target-location-for-a-directory"></a>Alterando o local de destino de um diretório

Se possível, a melhor maneira de especificar o local de destino de um diretório é criar a [tabela de diretórios](directory-table.md) em seu pacote de instalação para fornecer o local correto. Para obter mais informações, consulte [usando a tabela de diretórios](using-the-directory-table.md).

Se você precisar alterar o local do diretório no momento da instalação, terá as seguintes opções:

-   Especifique o local de um diretório definindo o valor de uma [propriedade pública](public-properties.md) na linha de comando. Durante a [ação CostFinalize](costfinalize-action.md), os caminhos de diretório internos usados pelo instalador são atualizados para o valor das propriedades listadas como chaves na [tabela de diretórios](directory-table.md). Para obter mais informações, consulte [usando Propriedades](using-properties.md) e [definindo valores de propriedade pública na linha de comando](setting-public-property-values-on-the-command-line.md).
-   Especifique o local de um diretório usando uma ação personalizada. Se a ação personalizada for executada antes da [ação CostFinalize](costfinalize-action.md), você poderá usar um [tipo de ação personalizada 51](custom-action-type-51.md) para definir o valor de uma propriedade de uma cadeia de caracteres de texto formatado. Se a ação personalizada for executada após a [ação CostFinalize](costfinalize-action.md), você poderá usar um [tipo de ação personalizada 35](custom-action-type-35.md) para definir o valor do caminho do diretório a partir de uma cadeia de caracteres de texto formatada. As ações personalizadas que alteram uma das [Propriedades da pasta do sistema](property-reference.md) devem ser incluídas nas tabelas de sequência de execução (tabela [InstallExecuteSequence](installexecutesequence-table.md) ou [tabela AdminExecuteSequence](adminexecutesequence-table.md)) e nas tabelas de sequência da interface do usuário ([tabela InstallUISequence](installuisequence-table.md) e [tabela AdminUISequence](adminuisequence-table.md)) para que a pasta seja alterada durante a [*interface do usuário completa*](f-gly.md) e as instalações [*básicas da interface*](b-gly.md) de usuário.
-   Se a instalação estiver executando uma [*interface do usuário completa*](f-gly.md), você poderá usar [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha) ou [SetTargetPath ControlEvent,](settargetpath-controlevent.md) para definir o caminho do diretório. Verifique a propriedade [**productstate**](productstate.md) para determinar se o produto que contém esse componente já está instalado antes de chamar **MsiSetTargetPath** ou SetTargetPath ControlEvent,. Não tente alterar o caminho do diretório de destino se alguns componentes que usam esse caminho já estiverem instalados para o usuário atual ou para um usuário diferente.

As seguintes restrições se aplicam a todas as opções acima:

-   Não tente alterar o caminho do diretório de destino se alguns componentes que usam o caminho já estiverem instalados para o usuário atual ou para um usuário diferente.
-   Não tente alterar o caminho do diretório de destino durante uma [instalação de manutenção](maintenance-installation.md).

 

 



