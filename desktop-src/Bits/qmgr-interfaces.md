---
title: Interfaces QMGR
description: Use as seguintes interfaces do Gerenciador de filas (QMGR) para baixar arquivos e monitorar trabalhos na fila de download.
ms.assetid: b5b59d4f-fa18-4225-8b6f-5d4033c61650
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51cc571dcc5bbf182b3f715ee34bb6c3e94b5502
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159355"
---
# <a name="qmgr-interfaces"></a><span data-ttu-id="47e6c-103">Interfaces QMGR</span><span class="sxs-lookup"><span data-stu-id="47e6c-103">QMGR Interfaces</span></span>

<span data-ttu-id="47e6c-104">\[As interfaces do Gerenciador de filas (QMGR) estão disponíveis para uso nos sistemas operacionais especificados na seção requisitos de um tópico.</span><span class="sxs-lookup"><span data-stu-id="47e6c-104">\[Queue Manager (QMGR) interfaces are available for use in the operating systems specified in a topic's Requirements section.</span></span> <span data-ttu-id="47e6c-105">Eles podem ter sido alterados ou não estarem disponíveis em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="47e6c-105">They may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="47e6c-106">Em vez disso, use as [interfaces bits](bits-interfaces.md).\]</span><span class="sxs-lookup"><span data-stu-id="47e6c-106">Instead, use the [BITS interfaces](bits-interfaces.md).\]</span></span>

<span data-ttu-id="47e6c-107">Use as seguintes interfaces do Gerenciador de filas (QMGR) para baixar arquivos e monitorar trabalhos na fila de download.</span><span class="sxs-lookup"><span data-stu-id="47e6c-107">Use the following Queue Manager (QMGR) interfaces to download files and monitor jobs within the download queue.</span></span>



| <span data-ttu-id="47e6c-108">Interface</span><span class="sxs-lookup"><span data-stu-id="47e6c-108">Interface</span></span>                                                                 | <span data-ttu-id="47e6c-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="47e6c-109">Description</span></span>                                                                                                                                                   |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="47e6c-110">**IBackgroundCopyCallback1**</span><span class="sxs-lookup"><span data-stu-id="47e6c-110">**IBackgroundCopyCallback1**</span></span>](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopycallback1)<br/>   | <span data-ttu-id="47e6c-111">Implemente para receber notificações quando ocorrerem eventos.</span><span class="sxs-lookup"><span data-stu-id="47e6c-111">Implement to receive notification when events occur.</span></span><br/>                                                                                               |
| [<span data-ttu-id="47e6c-112">**IBackgroundCopyGroup**</span><span class="sxs-lookup"><span data-stu-id="47e6c-112">**IBackgroundCopyGroup**</span></span>](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopygroup)<br/>           | <span data-ttu-id="47e6c-113">Use o para gerenciar o grupo.</span><span class="sxs-lookup"><span data-stu-id="47e6c-113">Use to manage the group.</span></span> <span data-ttu-id="47e6c-114">Por exemplo, adicione um trabalho ao grupo, defina as propriedades do grupo e inicie e interrompa o grupo na fila de download.</span><span class="sxs-lookup"><span data-stu-id="47e6c-114">For example, add a job to the group, set the properties of the group, and start and stop the group in the download queue.</span></span><br/> |
| [<span data-ttu-id="47e6c-115">**IBackgroundCopyJob1**</span><span class="sxs-lookup"><span data-stu-id="47e6c-115">**IBackgroundCopyJob1**</span></span>](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopyjob1)<br/>             | <span data-ttu-id="47e6c-116">Use para adicionar arquivos ao trabalho e recuperar o status do trabalho.</span><span class="sxs-lookup"><span data-stu-id="47e6c-116">Use to add files to the job and retrieve the job's status.</span></span><br/>                                                                                         |
| [<span data-ttu-id="47e6c-117">**IBackgroundCopyQMgr**</span><span class="sxs-lookup"><span data-stu-id="47e6c-117">**IBackgroundCopyQMgr**</span></span>](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopyqmgr)<br/>             | <span data-ttu-id="47e6c-118">Use para criar um novo grupo, recuperar um grupo existente ou enumerar todos os grupos na fila.</span><span class="sxs-lookup"><span data-stu-id="47e6c-118">Use to create a new group, retrieve an existing group, or enumerate all groups in the queue.</span></span><br/>                                                       |
| [<span data-ttu-id="47e6c-119">**IEnumBackgroundCopyGroups**</span><span class="sxs-lookup"><span data-stu-id="47e6c-119">**IEnumBackgroundCopyGroups**</span></span>](/windows/desktop/api/Qmgr/nn-qmgr-ienumbackgroundcopygroups)<br/> | <span data-ttu-id="47e6c-120">Use para recuperar uma lista de grupos na fila de download.</span><span class="sxs-lookup"><span data-stu-id="47e6c-120">Use to retrieve a list of groups in the download queue.</span></span><br/>                                                                                            |
| [<span data-ttu-id="47e6c-121">**IEnumBackgroundCopyJobs1**</span><span class="sxs-lookup"><span data-stu-id="47e6c-121">**IEnumBackgroundCopyJobs1**</span></span>](/windows/desktop/api/Qmgr/nn-qmgr-ienumbackgroundcopyjobs1)<br/>   | <span data-ttu-id="47e6c-122">Use para recuperar uma lista de trabalhos no grupo.</span><span class="sxs-lookup"><span data-stu-id="47e6c-122">Use to retrieve a list of jobs in the group.</span></span><br/>                                                                                                       |



 

 

 





