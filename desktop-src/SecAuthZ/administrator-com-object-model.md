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
# <a name="administrator-com-object-model"></a><span data-ttu-id="dc9fb-103">Modelo de objeto COM do administrador</span><span class="sxs-lookup"><span data-stu-id="dc9fb-103">Administrator COM Object Model</span></span>

<span data-ttu-id="dc9fb-104">No modelo de objeto COM do administrador, um aplicativo em execução como usuário padrão executa operações que exigem privilégios de administrador, criando um objeto de [Component Object Model](/windows/desktop/com/component-object-model--com--portal) elevado.</span><span class="sxs-lookup"><span data-stu-id="dc9fb-104">In the administrator COM object model, an application running as a standard user performs operations that require administrator privilege by creating an elevated [Component Object Model](/windows/desktop/com/component-object-model--com--portal) object.</span></span> <span data-ttu-id="dc9fb-105">Para obter informações sobre como criar um objeto COM elevado, consulte [o moniker de elevação com](../com/the-com-elevation-moniker.md).</span><span class="sxs-lookup"><span data-stu-id="dc9fb-105">For information about creating an elevated COM object, see [The COM Elevation Moniker](../com/the-com-elevation-moniker.md).</span></span>

<span data-ttu-id="dc9fb-106">Uma desvantagem de usar o modelo de objeto COM de administrador é que o usuário é solicitado a cada vez que uma operação privilegiada é executada.</span><span class="sxs-lookup"><span data-stu-id="dc9fb-106">One drawback to using the administrator COM object model is that the user is prompted each time a privileged operation is performed.</span></span>

<span data-ttu-id="dc9fb-107">Qualquer interface do usuário que possa controlar o objeto COM deve ser apresentada pelo próprio objeto COM.</span><span class="sxs-lookup"><span data-stu-id="dc9fb-107">Any user interface that can control the COM object must be presented by the COM object itself.</span></span> <span data-ttu-id="dc9fb-108">Caso contrário, um processo sem privilégios poderá fazer com que o objeto COM elevado execute operações privilegiadas sem que o usuário seja solicitado.</span><span class="sxs-lookup"><span data-stu-id="dc9fb-108">Otherwise, an unprivileged process could cause the elevated COM object to perform privileged operations without the user being prompted.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc9fb-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dc9fb-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc9fb-110">Desenvolvendo aplicativos que exigem privilégios de administrador</span><span class="sxs-lookup"><span data-stu-id="dc9fb-110">Developing Applications that Require Administrator Privilege</span></span>](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[<span data-ttu-id="dc9fb-111">Modelo de agente do administrador</span><span class="sxs-lookup"><span data-stu-id="dc9fb-111">Administrator Broker Model</span></span>](administrator-broker-model.md)
</dt> <dt>

[<span data-ttu-id="dc9fb-112">Modelo de tarefa elevada</span><span class="sxs-lookup"><span data-stu-id="dc9fb-112">Elevated Task Model</span></span>](elevated-task-model.md)
</dt> <dt>

[<span data-ttu-id="dc9fb-113">Modelo de serviço do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="dc9fb-113">Operating System Service Model</span></span>](operating-system-service-model.md)
</dt> </dl>

 

 
