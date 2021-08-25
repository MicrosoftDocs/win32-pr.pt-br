---
description: Um aplicativo em execução como um usuário padrão se comunica com um serviço em execução como sistema usando RPC (chamada de procedimento remoto).
ms.assetid: c0bcebe3-f7eb-471f-a21d-5840d2e26729
title: Modelo de serviço do sistema operacional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af797a7baad8390b1b4bc79fd7723a518c587ed58cc2dab27ab2898845335ca3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907796"
---
# <a name="operating-system-service-model"></a>Modelo de serviço do sistema operacional

No modelo de serviço do sistema operacional, um aplicativo em execução como um usuário padrão se comunica com um serviço em execução como **sistema** usando RPC ( [chamada de procedimento remoto](/windows/desktop/Rpc/rpc-start-page) ).

O aplicativo de usuário padrão é marcado no manifesto do aplicativo com um **requestedExecutionLevel** de **asInvoker**. Para executar uma operação que exige privilégio de administrador, o aplicativo de usuário padrão faz uma solicitação ao serviço.

Um uso para o modelo de serviço do sistema operacional é gerenciar aplicativos que podem afetar o sistema, como antivírus ou outros softwares indesejados e spyware. O aplicativo de usuário padrão permite que o usuário conectado controle alguns aspectos do serviço. O serviço é responsável por determinar quais operações ele executa para um aplicativo de usuário padrão. Por exemplo, um serviço antivírus pode permitir que um usuário padrão inicie uma verificação do sistema, mas pode não permitir que um usuário padrão desabilite a verificação de vírus em tempo real.

Uma grande vantagem de usar o modelo de serviço do sistema operacional é que não é necessária nenhuma solicitação de elevação.

Uma desvantagem de usar o modelo de serviço do sistema operacional é que um serviço em execução no sistema usa mais recursos do que uma tarefa, e um serviço não pode ser interrompido por um usuário padrão. Considere usar o [modelo de tarefa elevada](elevated-task-model.md) se for suficiente.

Para implementar o modelo de serviço do sistema operacional, crie um aplicativo cliente de usuário padrão e um serviço do sistema operacional. Instale o serviço no sistema operacional durante o tempo de instalação do produto.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Desenvolvendo aplicativos que exigem privilégios de administrador](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[Modelo de agente do administrador](administrator-broker-model.md)
</dt> <dt>

[Modelo de objeto COM do administrador](administrator-com-object-model.md)
</dt> <dt>

[Modelo de tarefa elevada](elevated-task-model.md)
</dt> </dl>

 

 
