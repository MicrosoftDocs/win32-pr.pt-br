---
description: Uma operação é uma ação de computador de baixo nível.
ms.assetid: d75bc507-3502-417c-af05-cbff807a5778
title: Operações e tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e8e60923e9631e37087a28a6a19747dc63249ff2f1ae8224c20e859e1f13c25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118912402"
---
# <a name="operations-and-tasks"></a>Operações e tarefas

Uma operação é uma ação de computador de baixo nível. Na API do Gerenciador de Autorização, uma operação é representada por um [**objeto IAzOperation.**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) Em geral, as operações são muitas em número e muito baixas para facilitar a administração. Agrupar operações em tarefas para simplificar a administração da política de autorização.

Uma tarefa é representada por um objeto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) e pode conter um ou mais [**objetos IAzOperation.**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) Um **objeto IAzTask** também pode conter outros **objetos IAzTask** para que as tarefas possam ser aninhadas. Para facilitar a administração, **um objeto IAzTask** deve representar uma tarefa que um usuário real deseja executar.

O acesso às operações contidas por uma tarefa pode ser qualificado em tempo de operação por um script de regra de negócio associado ao objeto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) que representa essa tarefa. Para obter mais informações sobre scripts de regra de negócios, [consulte Business Rules](business-rules.md).

Um [**objeto IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) também pode representar uma definição de função definindo sua [**propriedade IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) como **TRUE.** A interface **do usuário** snap-in do MMC do Gerenciador de Autorização exibe o objeto **IAzTask** como uma função. Para obter mais informações sobre definições de função, consulte [Funções](roles.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Definindo operações em C++](defining-operations-in-c--.md)
</dt> <dt>

[Agrupando operações em tarefas em C++](grouping-operations-into-tasks-in-c--.md)
</dt> <dt>

[Agrupando tarefas em funções no C++](grouping-tasks-into-roles-in-c--.md)
</dt> <dt>

[Usuários e grupos](users-and-groups.md)
</dt> </dl>

 

 



