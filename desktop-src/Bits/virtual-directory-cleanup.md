---
title: Limpeza do diretório virtual
description: O BITS estende os diretórios virtuais do IIS para dar suporte a carregamentos.
ms.assetid: 8214904e-8a95-4c4b-a1c5-91e84031587f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83fb689bb3c797a311ec7c2ef8134eb51ffd6f1a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917472"
---
# <a name="virtual-directory-cleanup"></a><span data-ttu-id="c6783-103">Limpeza do diretório virtual</span><span class="sxs-lookup"><span data-stu-id="c6783-103">Virtual Directory Cleanup</span></span>

<span data-ttu-id="c6783-104">O BITS estende os diretórios virtuais do IIS para dar suporte a carregamentos.</span><span class="sxs-lookup"><span data-stu-id="c6783-104">BITS extends IIS virtual directories to support uploads.</span></span> <span data-ttu-id="c6783-105">Cada diretório virtual tem uma propriedade de tempo limite de sessão (a propriedade de metabase [BITSSessionTimeout](bits-iis-extension-properties.md) do IIS) que especifica o período de tempo no qual o cliente do bits deve fazer o progresso no carregamento do arquivo.</span><span class="sxs-lookup"><span data-stu-id="c6783-105">Each virtual directory has a session time-out property (the IIS [BITSSessionTimeout](bits-iis-extension-properties.md) metabase property) that specifies the period of time in which the BITS client must make progress in uploading the file.</span></span> <span data-ttu-id="c6783-106">Se nenhum progresso for feito durante esse período (o temporizador é redefinido quando o andamento for feito), o BITS fechará a sessão.</span><span class="sxs-lookup"><span data-stu-id="c6783-106">If no progress is made during that period (the timer is reset when progress is made), BITS closes the session.</span></span> <span data-ttu-id="c6783-107">O tempo limite da sessão padrão é de 14 dias.</span><span class="sxs-lookup"><span data-stu-id="c6783-107">The default session time-out is 14 days.</span></span>

<span data-ttu-id="c6783-108">O BITS adiciona um item de trabalho à [Agendador de tarefas](/windows/desktop/TaskSchd/task-scheduler-start-page) para cada diretório virtual que você criar e habilitar.</span><span class="sxs-lookup"><span data-stu-id="c6783-108">BITS adds a work item to the [Task Scheduler](/windows/desktop/TaskSchd/task-scheduler-start-page) for each virtual directory you create and enable.</span></span> <span data-ttu-id="c6783-109">O item de trabalho exclui os recursos associados às sessões fechadas.</span><span class="sxs-lookup"><span data-stu-id="c6783-109">The work item deletes resources associated with the closed sessions.</span></span> <span data-ttu-id="c6783-110">Por padrão, a limpeza ocorre a cada 12 horas.</span><span class="sxs-lookup"><span data-stu-id="c6783-110">By default, the cleanup occurs every 12 hours.</span></span> <span data-ttu-id="c6783-111">Se dois diretórios virtuais apontarem para o mesmo diretório físico, o processo de limpeza iniciado por um dos diretórios excluirá os recursos associados a todas as sessões fechadas no diretório físico.</span><span class="sxs-lookup"><span data-stu-id="c6783-111">If two virtual directories point to the same physical directory, the cleanup process initiated by one of the directories deletes the resources associated with all closed sessions in the physical directory.</span></span>

<span data-ttu-id="c6783-112">Use a guia extensão BITS ou as interfaces [Agendador de tarefas](/windows/desktop/TaskSchd/task-scheduler-start-page) para alterar o agendamento de limpeza conforme apropriado para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c6783-112">Use the BITS Extension tab or the [Task Scheduler](/windows/desktop/TaskSchd/task-scheduler-start-page) interfaces to change the cleanup schedule as appropriate for your application.</span></span> <span data-ttu-id="c6783-113">Você também pode chamar o método [**IBITSExtensionSetup:: GetCleanupTask**](/windows/desktop/api/Bitscfg/nf-bitscfg-ibitsextensionsetup-getcleanuptask) para recuperar um ponteiro de interface para a tarefa de limpeza associada ao diretório virtual.</span><span class="sxs-lookup"><span data-stu-id="c6783-113">You can also call the [**IBITSExtensionSetup::GetCleanupTask**](/windows/desktop/api/Bitscfg/nf-bitscfg-ibitsextensionsetup-getcleanuptask) method to retrieve an interface pointer to the cleanup task associated with the virtual directory.</span></span>

> [!Note]  
> <span data-ttu-id="c6783-114">Se o Agendador de Tarefas for desabilitado depois que o diretório virtual for habilitado, o processo de limpeza do diretório virtual não funcionará.</span><span class="sxs-lookup"><span data-stu-id="c6783-114">If the Task Scheduler is disabled after the virtual directory is enabled, the virtual directory cleanup process will not work.</span></span>

 

 

 