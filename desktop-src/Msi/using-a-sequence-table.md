---
description: A criação das tabelas de sequência é uma parte essencial do desenvolvimento de um pacote do instalador, pois essas tabelas especificam a ordem de execução das ações padrão que controlam o processo de instalação e exibem as caixas de diálogo da interface do usuário.
ms.assetid: db9a9cae-2a66-4e0d-a981-8de66d7c2a13
title: Usando uma tabela de sequência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0be10082aba05429a63df69444ed28bea350aa5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828566"
---
# <a name="using-a-sequence-table"></a>Usando uma tabela de sequência

A criação das tabelas de sequência é uma parte essencial do desenvolvimento de um pacote do instalador, pois essas tabelas especificam a ordem de execução das [ações padrão](standard-actions.md) que controlam o processo de instalação e exibem as caixas de diálogo da interface do usuário.

Há três modos de instalação e dois tipos de tabelas de sequência para cada modo.

Os três modos de instalação separados com suporte no momento pelo instalador são:

-   Instalação simples
-   Instalação administrativa
-   Instalação do anúncio

As tabelas de sequência têm três campos: ação, condição e sequência. O campo de ação nomeia uma ação padrão ou personalizada ou uma caixa de diálogo definida pelo usuário ou sequência que o instalador executa. O campo condição permite que o autor especifique uma expressão lógica que controla se uma ação ou caixa de diálogo definida pelo usuário é executada ou exibida. Se o campo condição estiver em branco ou contiver uma expressão que seja avaliada como true, a ação ou a caixa de diálogo será executada ou exibida. A ação ou a caixa de diálogo será ignorada se a expressão for avaliada como false. O campo sequência especifica a ordem de execução de cada ação ou caixa de diálogo definida pelo usuário na tabela.

Cada um desses modos de instalação processa as tabelas de sequência da interface do usuário e as tabelas de sequência de execução. As tabelas de sequência da interface do usuário só serão processadas se o instalador tiver sido inicializado com o nível de exibição da interface do usuário definido como reduzido ou cheio. Consulte a referência de [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) para obter mais informações sobre os níveis de exibição da interface do usuário.

As tabelas de sequência da interface do usuário geralmente contêm ações padrão relacionadas à coleta de informações do sistema que são exibidas para o usuário por meio da interface do usuário. A interface do usuário é exibida gravando as chaves estrangeiras nos nomes das caixas de diálogo na [tabela de diálogo](dialog-table.md) no campo ação da tabela de sequência da interface do usuário. Em seguida, o usuário tem a oportunidade de modificar ou aceitar as informações do sistema e iniciar a instalação, que ocorre quando a tabela de sequências de execução é processada.

Durante uma instalação simples, a ação [instalar](install-action.md) nível superior é executada, o que, por sua vez, processa a [tabela InstallUISequence](installuisequence-table.md) e a [tabela InstallExecuteSequence](installexecutesequence-table.md).

Uma instalação administrativa normalmente é iniciada por um administrador de rede para atribuir e instalar aplicativos para usuários individuais e grupos de usuários. Durante esse tipo de instalação, a ação de nível superior do [administrador](admin-action.md) é executada, o que processa a [tabela AdminUISequence](adminuisequence-table.md) e a [tabela AdminExecuteSequence](adminexecutesequence-table.md).

Para [anunciar](advertisement.md) um aplicativo ou recurso, o instalador deve ser iniciado com a ação de [anúncio](advertise-action.md) . Durante esse tipo de instalação, a [tabela AdvtExecuteSequence](advtexecutesequence-table.md) é processada.

Ao criar qualquer tabela de sequência, é uma boa prática usar o número de sequência para ações padrão das sequências sugeridas nos tópicos abaixo. Para ações padrão que não têm nenhuma posição padrão na tabela de sequência, como [ForceReboot](forcereboot-action.md), [ValidateProductID](validateproductid-action.md)e [InstallExecute](installexecute-action.md), use um número de sequência que seja um múltiplo de dez para identificar a ação como uma ação padrão. Para ações personalizadas, use um número de sequência que não seja um múltiplo de dez para diferenciá-lo das ações padrão na tabela de sequência.

Para sequências de ação sugeridas para cada tabela de sequência, consulte os seguintes tópicos:

-   [InstallUISequence sugerido](suggested-installuisequence.md)
-   [InstallExecuteSequence sugerido](suggested-installexecutesequence.md)
-   [AdminUISequence sugerido](suggested-adminuisequence.md)
-   [AdminExecuteSequence sugerido](suggested-adminexecutesequence.md)
-   [AdvtUISequence sugerido](suggested-advtuisequence.md)
-   [AdvtExecuteSequence sugerido](suggested-advtexecutesequence.md)

Para obter uma descrição detalhada das tabelas de sequência e como as ações padrão são executadas, consulte o [exemplo de tabela de sequência detalhado](sequence-table-detailed-example.md).

* * Windows Installer 3,0 e posterior: * *

A partir do Windows Installer 3,0, um pacote de patch pode conter a [tabela MsiPatchSequence](msipatchsequence-table.md). Esta tabela contém todas as informações que o instalador requer para determinar a sequência do aplicativo de um patch de atualização pequeno em relação a todos os outros patches. Para obter mais informações, consulte [patches e atualizações](patching-and-upgrades.md).

> [!Note]
>
> [Módulos de mesclagem](merge-modules.md) podem conter [tabelas de banco de dados do módulo de mesclagem](merge-module-database-tables.md) que modificam as tabelas de sequência de ação do arquivo. msi de destino. A mesclagem do módulo em um banco de dados pode modificar as informações na tabela de sequência, mas não adiciona essas tabelas ao arquivo. msi. Para obter mais informações, consulte [criando tabelas de sequências do módulo de mesclagem](authoring-merge-module-sequence-tables.md).

 

 

 



