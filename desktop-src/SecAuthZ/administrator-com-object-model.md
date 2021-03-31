---
description: Um aplicativo em execução como um usuário padrão executa operações que exigem privilégios de administrador criando um objeto de Component Object Model elevado.
ms.assetid: 246fdf74-cc5b-47b1-b3a8-20441544e7be
title: Modelo de objeto COM do administrador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6c7d73cf31ce86c4788675374f34d04f6acf106
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829442"
---
# <a name="administrator-com-object-model"></a>Modelo de objeto COM do administrador

No modelo de objeto COM do administrador, um aplicativo em execução como usuário padrão executa operações que exigem privilégios de administrador, criando um objeto de [Component Object Model](/windows/desktop/com/component-object-model--com--portal) elevado. Para obter informações sobre como criar um objeto COM elevado, consulte [o moniker de elevação com](../com/the-com-elevation-moniker.md).

Uma desvantagem de usar o modelo de objeto COM de administrador é que o usuário é solicitado a cada vez que uma operação privilegiada é executada.

Qualquer interface do usuário que possa controlar o objeto COM deve ser apresentada pelo próprio objeto COM. Caso contrário, um processo sem privilégios poderá fazer com que o objeto COM elevado execute operações privilegiadas sem que o usuário seja solicitado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Desenvolvendo aplicativos que exigem privilégios de administrador](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[Modelo de agente do administrador](administrator-broker-model.md)
</dt> <dt>

[Modelo de tarefa elevada](elevated-task-model.md)
</dt> <dt>

[Modelo de serviço do sistema operacional](operating-system-service-model.md)
</dt> </dl>

 

 
