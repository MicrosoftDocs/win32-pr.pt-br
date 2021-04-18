---
description: Uma operação é uma ação de computador de baixo nível.
ms.assetid: d75bc507-3502-417c-af05-cbff807a5778
title: Operações e tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a198d8844a9f34030b8b6a40eba759eed4057119
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756567"
---
# <a name="operations-and-tasks"></a>Operações e tarefas

Uma operação é uma ação de computador de baixo nível. Na API do Gerenciador de autorização, uma operação é representada por um objeto [**IAzOperation**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) . Em geral, as operações são muitos em número e um nível muito baixo para facilitar a administração. Agrupe operações em tarefas para simplificar a administração da política de autorização.

Uma tarefa é representada por um objeto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) e pode conter um ou mais objetos [**IAzOperation**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) . Um objeto **IAzTask** também pode conter outros objetos **IAzTask** , para que as tarefas possam ser aninhadas. Para facilitar a administração, um objeto **IAzTask** deve representar uma tarefa que um usuário real deseja executar.

O acesso às operações contidas por uma tarefa pode ser qualificado em tempo de execução por um script de regra de negócio associado ao objeto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) que representa essa tarefa. Para obter mais informações sobre scripts de regra de negócio, consulte [regras de negócio](business-rules.md).

Um objeto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) também pode representar uma definição de função definindo sua propriedade [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) como **true**. A interface do usuário do snap-in MMC do **Gerenciador de autorização** exibe esse objeto **IAzTask** como uma função. Para obter mais informações sobre definições de função, consulte [funções](roles.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Definindo operações em C++](defining-operations-in-c--.md)
</dt> <dt>

[Agrupando operações em tarefas em C++](grouping-operations-into-tasks-in-c--.md)
</dt> <dt>

[Agrupando tarefas em funções em C++](grouping-tasks-into-roles-in-c--.md)
</dt> <dt>

[Usuários e grupos](users-and-groups.md)
</dt> </dl>

 

 



