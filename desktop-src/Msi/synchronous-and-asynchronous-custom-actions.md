---
description: O Windows Installer processa ações personalizadas como um thread separado da instalação principal.
ms.assetid: 6451029c-87f4-44ee-aa2b-cc9a1c25bcc0
title: Ações personalizadas síncronas e assíncronas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 067c5b40840269f3a0393faee8fe670f5e522c7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768717"
---
# <a name="synchronous-and-asynchronous-custom-actions"></a><span data-ttu-id="8b60a-103">Ações personalizadas síncronas e assíncronas</span><span class="sxs-lookup"><span data-stu-id="8b60a-103">Synchronous and Asynchronous Custom Actions</span></span>

<span data-ttu-id="8b60a-104">O Windows Installer processa ações personalizadas como um thread separado da instalação principal.</span><span class="sxs-lookup"><span data-stu-id="8b60a-104">The Windows Installer processes custom actions as a separate thread from the main installation.</span></span> <span data-ttu-id="8b60a-105">Durante a execução síncrona de uma ação personalizada, o instalador aguarda que o thread da ação personalizada seja concluído antes de continuar a instalação principal.</span><span class="sxs-lookup"><span data-stu-id="8b60a-105">During synchronous execution of a custom action, the installer waits for the thread of the custom action to complete before continuing the main installation.</span></span> <span data-ttu-id="8b60a-106">Durante a execução assíncrona, o instalador executa a ação personalizada simultaneamente à medida que a instalação atual continua.</span><span class="sxs-lookup"><span data-stu-id="8b60a-106">During asynchronous execution, the installer runs the custom action simultaneously as the current installation continues.</span></span> <span data-ttu-id="8b60a-107">Os autores de ações personalizadas devem, portanto, estar cientes de quaisquer threads assíncronos que possam estar fazendo alterações no banco de dados de instalação entre chamadas de função.</span><span class="sxs-lookup"><span data-stu-id="8b60a-107">Authors of custom actions must therefore be aware of any asynchronous threads that may be making changes to the installation database between function calls.</span></span>

<span data-ttu-id="8b60a-108">Em particular, as chamadas para [**MsiGetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) e [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha) devem ser evitadas em ações personalizadas assíncronas.</span><span class="sxs-lookup"><span data-stu-id="8b60a-108">In particular, calls to [**MsiGetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) and [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha) should be avoided in asynchronous custom actions.</span></span> <span data-ttu-id="8b60a-109">Em vez disso, use [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) para obter um caminho de destino.</span><span class="sxs-lookup"><span data-stu-id="8b60a-109">Instead use [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) to obtain a target path.</span></span> <span data-ttu-id="8b60a-110">Operações de banco de dados em massa, como operações de importação, exportação e transformação, devem ser evitadas em qualquer tipo de ação personalizada.</span><span class="sxs-lookup"><span data-stu-id="8b60a-110">Bulk database operations such as import, export, and transform operations should be avoided in any type of custom action.</span></span>

<span data-ttu-id="8b60a-111">Os sinalizadores de opção podem ser definidos no campo tipo da [tabela CustomAction](customaction-table.md) para especificar que os threads de ação principal e personalizada sejam executados de forma síncrona ou assíncrona.</span><span class="sxs-lookup"><span data-stu-id="8b60a-111">Option flags can be set in the Type field of the [CustomAction table](customaction-table.md) to specify that the main and custom action threads run synchronously or asynchronously.</span></span> <span data-ttu-id="8b60a-112">Consulte [Opções de processamento de retorno de ação personalizada](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="8b60a-112">See [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

<span data-ttu-id="8b60a-113">O instalador só pode executar ações [personalizadas de reversão](rollback-custom-actions.md) e ações de [instalação simultânea](concurrent-installations.md) como ações personalizadas síncronas.</span><span class="sxs-lookup"><span data-stu-id="8b60a-113">The installer can only execute [Rollback Custom Actions](rollback-custom-actions.md) and [Concurrent Installation](concurrent-installations.md) actions as synchronous custom actions.</span></span>

 

 



