---
description: Este exemplo demonstra como usar ações personalizadas para criar contas de usuário em um computador local ao instalar um componente.
ms.assetid: fc06dd7b-46d7-45a0-85b3-26f808c64f89
title: Usando uma ação personalizada para criar contas de usuário em um computador local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 408c80a5fbf32d9da758322bd6c5ebc881da73501d2b241c39f64cdd779d239d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499576"
---
# <a name="using-a-custom-action-to-create-user-accounts-on-a-local-computer"></a>Usando uma ação personalizada para criar contas de usuário em um computador local

Este exemplo demonstra como usar ações personalizadas para criar contas de usuário em um computador local ao instalar um componente. A remoção de um componente remove as contas de usuário locais criadas pela ação personalizada. Várias ações personalizadas são demonstradas, incluindo Ações [Personalizadas de](deferred-execution-custom-actions.md) Execução Adiada e [Ações Personalizadas de Reação](rollback-custom-actions.md).

O exemplo atende às especificações a seguir.

-   A instalação cria contas de usuário somente se Windows 2000.
-   A instalação criará contas de usuário somente se o componente estiver sendo instalado para ser executado localmente. Isso impede a criação de contas de usuário durante o reparo ou reinstalação do componente.
-   O Instalador remove as contas quando o componente é removido.
-   As informações da conta de usuário são lidas de uma tabela personalizada no banco de dados de instalação e não são codificadas no código de ação personalizado.
-   Como a criação ou remoção de contas de usuário requer privilégios elevados, algumas das ações personalizadas devem ser capazes de fazer alterações no sistema que exigem privilégios elevados. Essas ações personalizadas devem ser adiadas ações personalizadas que são executados quando no script de execução.
-   Cada conta tem uma ação personalizada de reação para garantir que a conta seja removida na remoção da instalação do componente. Isso não inclui a retribuição de uma exclusão de conta durante a remoção de um componente.
-   As ações personalizadas enviam mensagens ActionData para cada conta criada ou removida. Isso não inclui o fornecimento de mensagens de progresso para ProgressBar.
-   Ações personalizadas relatarão um erro se uma conta não puder ser criada.
-   A senha da conta é obtida por meio da interação do usuário com a interface do usuário ou, no caso de uma instalação na interface do usuário básica ou em Nenhum [nível Interface do Usuário](user-interface-levels.md), como uma propriedade passada na linha de comando.
-   Os dados confidenciais estão ocultos do arquivo de log.

O exemplo inclui um componente hipotético chamado TestAccount. A discussão nas seções a seguir pressupo que você já criou os recursos necessários para TestAccount e criou as tabelas [Recurso](feature-table.md) [,](component-table.md)Componente [,](file-table.md)Arquivo [,](directory-table.md)Diretório e [FeatureComponents](featurecomponents-table.md) no banco de dados de exemplo necessário para instalar esse componente. Para obter mais informações, consulte [Um exemplo de instalação](an-installation-example.md).

Os tópicos a seguir contêm informações sobre como criar ações personalizadas necessárias e adicioná-las a um pacote de instalação.

-   [Como fazer as ações personalizadas](authoring-the-custom-actions.md)
-   [Adicionando uma tabela CustomUserAccounts personalizada](adding-a-custom-customuseraccounts-table.md)
-   [Como fazer a tabela CustomAction](authoring-the-customaction-table.md)
-   [Como autor das tabelas ActionText e Error](authoring-the-actiontext-and-error-tables.md)
-   [Como fazer a tabela InstallExecuteSequence](authoring-the-installexecutesequence-table.md)
-   [Como Interface do Usuário entrada de senha](authoring-the-user-interface-for-password-input.md)
-   [Proteger a instalação](securing-the-installation.md)

 

 



