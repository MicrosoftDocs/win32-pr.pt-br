---
description: Este exemplo demonstra como usar ações personalizadas para criar contas de usuário em um computador local ao instalar um componente.
ms.assetid: fc06dd7b-46d7-45a0-85b3-26f808c64f89
title: Usando uma ação personalizada para criar contas de usuário em um computador local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfd3bf002c0fa1d661c6bfebb6d1a18cbc4b0652
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296964"
---
# <a name="using-a-custom-action-to-create-user-accounts-on-a-local-computer"></a>Usando uma ação personalizada para criar contas de usuário em um computador local

Este exemplo demonstra como usar ações personalizadas para criar contas de usuário em um computador local ao instalar um componente. A remoção de um componente remove as contas de usuário local criadas pela ação personalizada. Várias ações personalizadas são demonstradas, incluindo [ações personalizadas de execução adiada](deferred-execution-custom-actions.md) e [ações personalizadas de reversão](rollback-custom-actions.md).

O exemplo atende às especificações a seguir.

-   A instalação cria contas de usuário somente se estiver executando o Windows 2000.
-   A instalação criará contas de usuário somente se o componente estiver sendo instalado para ser executado localmente. Isso impede a criação de contas de usuário durante o reparo ou reinstalação do componente.
-   O instalador remove as contas quando o componente é removido.
-   As informações de conta de usuário são lidas de uma tabela personalizada no banco de dados de instalação e não são embutidas em código no código de ação personalizado.
-   Como a criação ou remoção de contas de usuário requer privilégios elevados, algumas das ações personalizadas devem ser capazes de fazer alterações no sistema que exigem privilégios elevados. Essas ações personalizadas devem ser ações personalizadas adiadas que são executadas quando no script de execução.
-   Cada conta tem uma ação personalizada de reversão para garantir que a conta seja removida na reversão da instalação do componente. Isso não inclui a reversão de uma exclusão de conta durante a remoção de um componente.
-   Ações personalizadas enviam mensagens ActionData para cada conta que é criada ou removida. Isso não inclui o fornecimento de mensagens de progresso para o ProgressBar.
-   Ações personalizadas relatarão um erro se uma conta não puder ser criada.
-   A senha para a conta é obtida por meio da interação do usuário com a interface do usuário, ou no caso de uma instalação na interface do usuário básica ou nenhum [nível de interface de usuários](user-interface-levels.md), como uma propriedade passada na linha de comando.
-   Os dados confidenciais ficam ocultos do arquivo de log.

O exemplo inclui um componente hipotético chamado TestAccount. A discussão nas seções a seguir pressupõe que você já criou os recursos exigidos pelo TestAccount e criou o [recurso](feature-table.md), o [componente](component-table.md), o [arquivo](file-table.md), o [diretório](directory-table.md)e as tabelas [FeatureComponents](featurecomponents-table.md) no banco de dados de exemplo necessário para instalar esse componente. Para obter mais informações, consulte [um exemplo de instalação](an-installation-example.md).

Os tópicos a seguir contêm informações sobre como criar ações personalizadas necessárias e adicioná-las a um pacote de instalação.

-   [Criando as ações personalizadas](authoring-the-custom-actions.md)
-   [Adicionando uma tabela CustomUserAccounts personalizada](adding-a-custom-customuseraccounts-table.md)
-   [Criando a tabela CustomAction](authoring-the-customaction-table.md)
-   [Criando as tabelas de erro e ActionText](authoring-the-actiontext-and-error-tables.md)
-   [Criando a tabela InstallExecuteSequence](authoring-the-installexecutesequence-table.md)
-   [Criando a interface do usuário para entrada de senha](authoring-the-user-interface-for-password-input.md)
-   [Protegendo a instalação](securing-the-installation.md)

 

 



