---
description: A criar as tabelas de sequência é uma parte essencial do desenvolvimento de um pacote do instalador porque essas tabelas especificam a ordem de execução para as ações padrão que controlam o processo de instalação e exibem as caixas de diálogo da interface do usuário.
ms.assetid: db9a9cae-2a66-4e0d-a981-8de66d7c2a13
title: Usando uma tabela de sequência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16adf47a554bf70298b0efc893847f84eafd6e97313b09ba9ea3182398cdd97d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809006"
---
# <a name="using-a-sequence-table"></a>Usando uma tabela de sequência

A criar as tabelas de sequência é uma parte essencial do desenvolvimento de [](standard-actions.md) um pacote do instalador porque essas tabelas especificam a ordem de execução para as ações padrão que controlam o processo de instalação e exibem as caixas de diálogo da interface do usuário.

Há três modos de instalação e dois tipos de tabelas de sequência para cada modo.

Os três modos de instalação separados com suporte no momento pelo instalador são:

-   Instalação simples
-   Instalação administrativa
-   Instalação de anúncio

As tabelas de sequência têm três campos: Ação, Condição e Sequência. O campo Ação nomeia uma ação padrão ou personalizada ou uma caixa de diálogo definida pelo usuário ou uma sequência executada pelo instalador. O campo Condição permite que o autor especifique uma expressão lógica que controla se uma ação ou uma caixa de diálogo definida pelo usuário é executada ou exibida. Se o campo Condição estiver em branco ou contiver uma expressão que seja avaliada como True, a ação ou a caixa de diálogo será executada ou exibida. A ação ou a caixa de diálogo será ignorada se a expressão for avaliada como False. O campo Sequência especifica a ordem de execução de cada ação ou caixa de diálogo definida pelo usuário na tabela.

Cada um desses modos de instalação processa as tabelas de sequência de interface do usuário e as tabelas de sequência de execução. As tabelas de sequência de interface do usuário só serão processadas se o instalador tiver sido inicializado com o nível de exibição da interface do usuário definido como Reduzido ou Completo. Consulte a referência [**de MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) para obter mais informações sobre os níveis de exibição da interface do usuário.

As tabelas de sequência de interface do usuário normalmente contêm ações padrão relacionadas à coleta de informações do sistema exibidas ao usuário por meio da interface do usuário. A interface do usuário é exibida gravando as chaves [](dialog-table.md) estrangeiras nos nomes das caixas de diálogo na tabela de diálogo no campo Ação da tabela de sequência de interface do usuário. Em seguida, o usuário tem a oportunidade de modificar ou aceitar as informações do sistema e iniciar a instalação, que ocorre quando a tabela de sequência de execução é processada.

Durante uma instalação simples, a ação [INSTALL](install-action.md) de nível superior é executada, que, por sua vez, processa a tabela [InstallUISequence](installuisequence-table.md) e a [tabela InstallExecuteSequence](installexecutesequence-table.md).

Uma Instalação Administrativa normalmente é iniciada por um administrador de rede para atribuir e instalar aplicativos para usuários individuais e grupos de usuários. Durante esse tipo de [](admin-action.md) instalação, a ação de nível superior admin é executada, que processa a tabela [AdminUISequence](adminuisequence-table.md) e a [tabela AdminExecuteSequence](adminexecutesequence-table.md).

Para [anunciar um](advertisement.md) aplicativo ou recurso, o instalador deve ser iniciado com a ação [ADVERTISE.](advertise-action.md) Durante esse tipo de instalação, a [tabela AdvtExecuteSequence](advtexecutesequence-table.md) é processada.

Ao autorizar qualquer tabela de sequência, é uma boa prática usar o número de sequência para ações padrão das sequências sugeridas nos tópicos abaixo. Para ações padrão que não têm nenhuma posição padrão na tabela de sequência, como [ForceReboot,](forcereboot-action.md) [ValidateProductID](validateproductid-action.md)e [InstallExecute](installexecute-action.md), use um número de sequência que seja um múltiplo de dez para identificar a ação como uma ação padrão. Para ações personalizadas, use um número de sequência que não seja um múltiplo de dez para diferenciá-lo das ações padrão na tabela de sequência.

Para sequências de ação sugeridas para cada tabela de sequência, consulte os seguintes tópicos:

-   [InstallUISequence sugerido](suggested-installuisequence.md)
-   [Instalação SugeridaExecuteSequence](suggested-installexecutesequence.md)
-   [AdminUISequence sugerido](suggested-adminuisequence.md)
-   [AdminExecuteSequence sugerido](suggested-adminexecutesequence.md)
-   [AdvtUISequence sugerido](suggested-advtuisequence.md)
-   [AdvtExecuteSequence sugerido](suggested-advtexecutesequence.md)

Para uma descrição detalhada das tabelas de sequência e como as ações padrão são executadas, consulte o exemplo detalhado [da tabela de sequência.](sequence-table-detailed-example.md)

**Windows Instalador 3.0 e posterior: **

A partir do Windows 3.0, um pacote de patch pode conter a [tabela MsiPatchSequence](msipatchsequence-table.md). Esta tabela contém todas as informações que o instalador requer para determinar a sequência da aplicação de um pequeno patch de atualização em relação a todos os outros patches. Para obter mais informações, consulte [Patching and Upgrades](patching-and-upgrades.md).

> [!Note]
>
> [Os módulos de mesclagem](merge-modules.md) podem conter [tabelas de banco](merge-module-database-tables.md) de dados de módulo de mesclagem que modificam as tabelas de sequência de ação do arquivo .msi destino. Mesclar o módulo em um banco de dados pode modificar as informações na tabela de sequência, mas não adiciona essas tabelas ao arquivo .msi. Para obter mais informações, consulte [Authoring Merge Module Sequence Tables](authoring-merge-module-sequence-tables.md).

 

 

 



