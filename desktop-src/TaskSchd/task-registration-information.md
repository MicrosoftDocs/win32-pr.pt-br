---
title: Informações de registro da tarefa
description: As informações de registro fornecem uma maneira de identificar uma tarefa de várias maneiras diferentes. Por exemplo, uma tarefa pode ser identificada pelo autor, como ela foi criada (conhecida como a origem da tarefa) e a data de registro.
ms.assetid: 45c9fa99-2718-4202-8987-4b506bd677e9
keywords:
- Agendador de Tarefas de informações de registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b12e3dc9163b1074eff12be6b872780184b112b6c8a2512e3a68901d083f9c85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139279"
---
# <a name="task-registration-information"></a>Informações de registro da tarefa

As informações de registro fornecem uma maneira de identificar uma tarefa de várias maneiras diferentes. Por exemplo, uma tarefa pode ser identificada pelo autor, como ela foi criada (conhecida como a origem da tarefa) e a data de registro.

## <a name="using-registration-information"></a>Usando informações de registro

As informações de registro normalmente são especificadas quando a tarefa é criada e, em seguida, usada das seguintes maneiras:

-   Exibido pela interface do usuário do Agendador de Tarefas.
-   Obter ou definir por aplicativos ou scripts do C++.
-   Em um ambiente corporativo, usado como critério de pesquisa ao enumerar todas as tarefas registradas.

## <a name="types-of-registration-information"></a>Tipos de informações de registro

As informações de registro de tarefa são definidas pelas propriedades do objeto [**RegistrationInfo**](registrationinfo.md) para aplicativos de script, as propriedades da interface [**IRegistrationInfo**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationinfo) para aplicativos C++ e os elementos filho do [**elemento RegistrationInfo (TaskType)**](taskschedulerschema-registrationinfo-tasktype-element.md) para leitura ou gravação de XML.

Essas propriedades permitem o acesso aos seguintes tipos de informações de registro:

-   Autor da tarefa

    Agendador de Tarefas define o autor da tarefa quando ela é criada.

-   Data de registro da tarefa

    Agendador de Tarefas define essa data quando a tarefa é registrada.

-   Descrição da tarefa

    Uma descrição definida pelo usuário que pode incluir quais gatilhos são usados para iniciar a tarefa ou quais ações a tarefa executa.

-   Documentação da tarefa

    Documentação fornecida pelo usuário que é necessária para a tarefa.

-   Descritor de segurança da tarefa

    Um descritor de segurança fornecido pelo usuário.

-   Origem da tarefa

    Informações fornecidas pelo usuário que descrevem de onde a tarefa foi originada. Por exemplo, uma tarefa pode se originar de um componente, serviço, aplicativo ou usuário.

-   URI da tarefa

    Um URI (Uniform Resource Identifier) para a tarefa.

-   Versão da Tarefa

    Informações fornecidas pelo usuário que são usadas quando há várias versões de uma tarefa.

-   Texto XML

    Uma versão formatada em XML das informações de registro. Observe que você pode definir ou modificar as informações de registro diretamente por meio desse XML e as propriedades apropriadas de objeto e de interface serão atualizadas de acordo.

## <a name="registering-tasks"></a>Registrando tarefas

Uma tarefa pode ser registrada depois que as definições de tarefa são criadas e as informações de registro e os valores de configuração são fornecidos pelo usuário. Uma tarefa é registrada usando o método [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) para aplicativos de script ou o método [**ITaskFolder:: RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) para aplicativos C++. Se você quiser registrar uma tarefa usando XML para definir a tarefa, use o método [**TaskFolder. RegisterTask**](taskfolder-registertask.md) para aplicativos de script e o método [**ITaskFolder:: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) para aplicativos C++.

Nos métodos mencionados acima, você pode especificar o contexto de segurança para executar a tarefa. Você precisa ser um administrador no sistema para agendar trabalhos para serem executados em contextos diferentes do seu próprio. Para obter mais informações sobre os contextos de segurança para executar tarefas, consulte [contextos de segurança para tarefas em execução](security-contexts-for-running-tasks.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o Agendador de Tarefas](about-the-task-scheduler.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 




