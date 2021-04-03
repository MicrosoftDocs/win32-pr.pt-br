---
title: Propriedades de ITsSbTaskInfo
description: A interface ITsSbTaskInfo expõe as propriedades a seguir.
ms.assetid: 402B8502-DE17-440B-867D-45922582C30E
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c0e4c8fefc2e443778b2ce177e61a314a3e0ef9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638496"
---
# <a name="itssbtaskinfo-properties"></a><span data-ttu-id="73e7b-103">Propriedades de ITsSbTaskInfo</span><span class="sxs-lookup"><span data-stu-id="73e7b-103">ITsSbTaskInfo Properties</span></span>

<span data-ttu-id="73e7b-104">A interface [**ITsSbTaskInfo**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo) expõe as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="73e7b-104">The [**ITsSbTaskInfo**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo) interface exposes the following properties.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="73e7b-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="73e7b-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="73e7b-106">**Propriedade de contexto**</span><span class="sxs-lookup"><span data-stu-id="73e7b-106">**Context property**</span></span>](itssbtaskinfo-context.md)
</dt> <dd>

<span data-ttu-id="73e7b-107">Recupera os bytes de contexto associados à tarefa.</span><span class="sxs-lookup"><span data-stu-id="73e7b-107">Retrieves the context bytes associated with the task.</span></span>

</dd> <dt>

[<span data-ttu-id="73e7b-108">**Propriedade prazo**</span><span class="sxs-lookup"><span data-stu-id="73e7b-108">**Deadline property**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_deadline)
</dt> <dd>

<span data-ttu-id="73e7b-109">Recupera a hora pela qual a tarefa deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="73e7b-109">Retrieves the time by which the task must be initiated.</span></span> <span data-ttu-id="73e7b-110">Isso é usado para priorizar patches.</span><span class="sxs-lookup"><span data-stu-id="73e7b-110">This is used to prioritize patches.</span></span> <span data-ttu-id="73e7b-111">O patch com o prazo mais antigo será iniciado primeiro.</span><span class="sxs-lookup"><span data-stu-id="73e7b-111">The patch with the earliest deadline will get initiated first.</span></span>

</dd> <dt>

[<span data-ttu-id="73e7b-112">**Propriedade EndTime**</span><span class="sxs-lookup"><span data-stu-id="73e7b-112">**EndTime property**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_endtime)
</dt> <dd>

<span data-ttu-id="73e7b-113">Recupera a hora mais recente em que o agente de tarefa pode iniciar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="73e7b-113">Retrieves the latest time the task agent can start the task.</span></span>

</dd> <dt>

[<span data-ttu-id="73e7b-114">**Propriedade do identificador**</span><span class="sxs-lookup"><span data-stu-id="73e7b-114">**Identifier property**</span></span>](itssbtaskinfo-identifier.md)
</dt> <dd>

<span data-ttu-id="73e7b-115">Recupera um GUID que é usado como um identificador exclusivo pelo agente de tarefa.</span><span class="sxs-lookup"><span data-stu-id="73e7b-115">Retrieves a GUID that is used as a unique identifier by the task agent.</span></span>

</dd> <dt>

[<span data-ttu-id="73e7b-116">**Propriedade do rótulo**</span><span class="sxs-lookup"><span data-stu-id="73e7b-116">**Label property**</span></span>](itssbtaskinfo-label.md)
</dt> <dd>

<span data-ttu-id="73e7b-117">Recupera o rótulo que descreve a finalidade da tarefa.</span><span class="sxs-lookup"><span data-stu-id="73e7b-117">Retrieves the label that describes the purpose of the task.</span></span>

</dd> <dt>

[<span data-ttu-id="73e7b-118">**Propriedade plugin**</span><span class="sxs-lookup"><span data-stu-id="73e7b-118">**Plugin property**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_plugin)
</dt> <dd>

<span data-ttu-id="73e7b-119">Recupera o nome de exibição do agente de tarefa.</span><span class="sxs-lookup"><span data-stu-id="73e7b-119">Retrieves the display name of the task agent.</span></span>

</dd> <dt>

[<span data-ttu-id="73e7b-120">**Propriedade StartTime**</span><span class="sxs-lookup"><span data-stu-id="73e7b-120">**StartTime property**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_starttime)
</dt> <dd>

<span data-ttu-id="73e7b-121">Recupera a hora mais antiga em que o agente de tarefa pode iniciar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="73e7b-121">Retrieves the earliest time the task agent can start the task.</span></span>

</dd> <dt>

[<span data-ttu-id="73e7b-122">**Propriedade de status**</span><span class="sxs-lookup"><span data-stu-id="73e7b-122">**Status property**</span></span>](itssbtaskinfo-status.md)
</dt> <dd>

<span data-ttu-id="73e7b-123">Recupera um valor de enumeração de [**\_ \_ status da tarefa RDV**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) que representa o estado da tarefa.</span><span class="sxs-lookup"><span data-stu-id="73e7b-123">Retrieves an [**RDV\_TASK\_STATUS**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) enumeration value that represents the state of the task.</span></span>

</dd> <dt>

[<span data-ttu-id="73e7b-124">**Propriedade TargetId**</span><span class="sxs-lookup"><span data-stu-id="73e7b-124">**TargetId property**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_targetid)
</dt> <dd>

<span data-ttu-id="73e7b-125">Recupera o identificador de destino.</span><span class="sxs-lookup"><span data-stu-id="73e7b-125">Retrieves the target identifier.</span></span>

</dd> </dl>

 

 




