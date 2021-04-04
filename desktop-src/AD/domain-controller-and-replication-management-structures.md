---
title: Estruturas de gerenciamento de replicação e controlador de domínio
description: O controlador de domínio e as funções de gerenciamento de replicação usam as seguintes estruturas.
ms.assetid: 42b20d3b-1799-4f5f-b74e-fe9284dd8ac3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4afe084e4285f4851457f9a519e747952e3bbd67
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103823662"
---
# <a name="domain-controller-and-replication-management-structures"></a><span data-ttu-id="377c8-103">Estruturas de gerenciamento de replicação e controlador de domínio</span><span class="sxs-lookup"><span data-stu-id="377c8-103">Domain Controller and Replication Management Structures</span></span>

<span data-ttu-id="377c8-104">O controlador de domínio e as funções de gerenciamento de replicação usam as seguintes estruturas:</span><span class="sxs-lookup"><span data-stu-id="377c8-104">The domain controller and replication management functions use the following structures:</span></span>

-   [<span data-ttu-id="377c8-105">**\_Informações do controlador de domínio DS \_ \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="377c8-105">**DS\_DOMAIN\_CONTROLLER\_INFO\_1**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_domain_controller_info_1a)
-   [<span data-ttu-id="377c8-106">**\_Informações do controlador de domínio DS \_ \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="377c8-106">**DS\_DOMAIN\_CONTROLLER\_INFO\_2**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_domain_controller_info_2a)
-   [<span data-ttu-id="377c8-107">**\_Informações do controlador de domínio DS \_ \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="377c8-107">**DS\_DOMAIN\_CONTROLLER\_INFO\_3**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_domain_controller_info_3a)
-   [<span data-ttu-id="377c8-108">**\_resultado do nome DS \_**</span><span class="sxs-lookup"><span data-stu-id="377c8-108">**DS\_NAME\_RESULT**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_name_resulta)
-   [<span data-ttu-id="377c8-109">**\_item de \_ resultado do nome DS \_**</span><span class="sxs-lookup"><span data-stu-id="377c8-109">**DS\_NAME\_RESULT\_ITEM**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_name_result_itema)
-   [<span data-ttu-id="377c8-110">**\_metadados de \_ attr de repl \_ DS \_**</span><span class="sxs-lookup"><span data-stu-id="377c8-110">**DS\_REPL\_ATTR\_META\_DATA**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_meta_data)
-   [<span data-ttu-id="377c8-111">**\_Metadados de attr de repl DS \_ \_ \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="377c8-111">**DS\_REPL\_ATTR\_META\_DATA\_2**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_meta_data_2)
-   [<span data-ttu-id="377c8-112">**\_blob de \_ metadados de attr DS repl \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="377c8-112">**DS\_REPL\_ATTR\_META\_DATA\_BLOB**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_meta_data_blob)
-   [<span data-ttu-id="377c8-113">**\_metadados de \_ \_ valor de \_ attr \_ do DS repl**</span><span class="sxs-lookup"><span data-stu-id="377c8-113">**DS\_REPL\_ATTR\_VALUE\_META\_DATA**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_value_meta_data)
-   [<span data-ttu-id="377c8-114">**Metadados do valor de attr do DS \_ repl \_ \_ \_ \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="377c8-114">**DS\_REPL\_ATTR\_VALUE\_META\_DATA\_2**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_value_meta_data_2)
-   [<span data-ttu-id="377c8-115">**EXT. de metadados do valor de attr do DS \_ repl \_ \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="377c8-115">**DS\_REPL\_ATTR\_VALUE\_META\_DATA\_EXT**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_value_meta_data_ext)
-   [<span data-ttu-id="377c8-116">**\_cursor repl \_ DS**</span><span class="sxs-lookup"><span data-stu-id="377c8-116">**DS\_REPL\_CURSOR**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor)
-   [<span data-ttu-id="377c8-117">**\_Cursor de repl DS \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="377c8-117">**DS\_REPL\_CURSOR\_2**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor_2)
-   [<span data-ttu-id="377c8-118">**\_Cursor de repl DS \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="377c8-118">**DS\_REPL\_CURSOR\_3**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor_3w)
-   [<span data-ttu-id="377c8-119">**\_blob de \_ cursor \_ repl DS**</span><span class="sxs-lookup"><span data-stu-id="377c8-119">**DS\_REPL\_CURSOR\_BLOB**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor_blob)
-   [<span data-ttu-id="377c8-120">**\_cursores de repl DS \_**</span><span class="sxs-lookup"><span data-stu-id="377c8-120">**DS\_REPL\_CURSORS**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors)
-   [<span data-ttu-id="377c8-121">**\_Cursores de repl do DS \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="377c8-121">**DS\_REPL\_CURSORS\_2**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors_2)
-   [<span data-ttu-id="377c8-122">**\_Cursores de repl do DS \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="377c8-122">**DS\_REPL\_CURSORS\_3**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors_3w)
-   [<span data-ttu-id="377c8-123">**\_falha de \_ DSA do KCC \_ \_ do DS repl**</span><span class="sxs-lookup"><span data-stu-id="377c8-123">**DS\_REPL\_KCC\_DSA\_FAILURE**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_kcc_dsa_failurew)
-   [<span data-ttu-id="377c8-124">**\_falhas do \_ DSA do KCC \_ \_ do DS repl**</span><span class="sxs-lookup"><span data-stu-id="377c8-124">**DS\_REPL\_KCC\_DSA\_FAILURES**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_kcc_dsa_failuresw)
-   [<span data-ttu-id="377c8-125">**\_ \_ \_ blob FAILUREW do DSA \_ de repl do DS \_**</span><span class="sxs-lookup"><span data-stu-id="377c8-125">**DS\_REPL\_KCC\_DSA\_FAILUREW\_BLOB**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_kcc_dsa_failurew_blob)
-   [<span data-ttu-id="377c8-126">**\_vizinho de repl DS \_**</span><span class="sxs-lookup"><span data-stu-id="377c8-126">**DS\_REPL\_NEIGHBOR**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborw)
-   [<span data-ttu-id="377c8-127">**\_vizinhos de repl DS \_**</span><span class="sxs-lookup"><span data-stu-id="377c8-127">**DS\_REPL\_NEIGHBORS**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborsw)
-   [<span data-ttu-id="377c8-128">**\_blob de \_ NEIGHBORW \_ repl DS**</span><span class="sxs-lookup"><span data-stu-id="377c8-128">**DS\_REPL\_NEIGHBORW\_BLOB**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborw_blob)
-   [<span data-ttu-id="377c8-129">**\_metadados de \_ obj \_ repl \_ DS**</span><span class="sxs-lookup"><span data-stu-id="377c8-129">**DS\_REPL\_OBJ\_META\_DATA**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_obj_meta_data)
-   [<span data-ttu-id="377c8-130">**\_Metadados obj do DS repl \_ \_ \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="377c8-130">**DS\_REPL\_OBJ\_META\_DATA\_2**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_obj_meta_data_2)
-   [<span data-ttu-id="377c8-131">**\_op de repl DS \_**</span><span class="sxs-lookup"><span data-stu-id="377c8-131">**DS\_REPL\_OP**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw)
-   [<span data-ttu-id="377c8-132">**\_blob de \_ OPW \_ repl DS**</span><span class="sxs-lookup"><span data-stu-id="377c8-132">**DS\_REPL\_OPW\_BLOB**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw_blob)
-   [<span data-ttu-id="377c8-133">**\_ \_ operações pendentes de repl DS \_**</span><span class="sxs-lookup"><span data-stu-id="377c8-133">**DS\_REPL\_PENDING\_OPS**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_pending_opsw)
-   [<span data-ttu-id="377c8-134">**\_STATISTICSW de \_ fila de repl DS \_**</span><span class="sxs-lookup"><span data-stu-id="377c8-134">**DS\_REPL\_QUEUE\_STATISTICSW**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_queue_statisticsw)
-   <span data-ttu-id="377c8-135">[**\_ \_ blob STATISTICSW da fila de repl DS \_ \_**](/previous-versions/windows/desktop/legacy/ms676274(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="377c8-135">[**DS\_REPL\_QUEUE\_STATISTICSW\_BLOB**](/previous-versions/windows/desktop/legacy/ms676274(v=vs.85))</span></span>
-   [<span data-ttu-id="377c8-136">**\_metadados de \_ valor de repl \_ DS \_**</span><span class="sxs-lookup"><span data-stu-id="377c8-136">**DS\_REPL\_VALUE\_META\_DATA**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data)
-   [<span data-ttu-id="377c8-137">**\_Metadados do valor de repl DS \_ \_ \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="377c8-137">**DS\_REPL\_VALUE\_META\_DATA\_2**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_2)
-   [<span data-ttu-id="377c8-138">**EXT. de metadados de valor de \_ repl DS \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="377c8-138">**DS\_REPL\_VALUE\_META\_DATA\_EXT**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_ext)
-   [<span data-ttu-id="377c8-139">**\_blob de \_ metadados de valor de repl DS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="377c8-139">**DS\_REPL\_VALUE\_META\_DATA\_BLOB**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_blob)
-   [<span data-ttu-id="377c8-140">**EXT. de blob de \_ metadados de valor de repl DS \_ \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="377c8-140">**DS\_REPL\_VALUE\_META\_DATA\_BLOB\_EXT**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_blob_ext)
-   [<span data-ttu-id="377c8-141">**\_ERRINFO REPSYNCALL \_ DS**</span><span class="sxs-lookup"><span data-stu-id="377c8-141">**DS\_REPSYNCALL\_ERRINFO**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repsyncall_errinfoa)
-   [<span data-ttu-id="377c8-142">**\_sincronização de REPSYNCALL DS \_**</span><span class="sxs-lookup"><span data-stu-id="377c8-142">**DS\_REPSYNCALL\_SYNC**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repsyncall_synca)
-   [<span data-ttu-id="377c8-143">**\_atualização de REPSYNCALL DS \_**</span><span class="sxs-lookup"><span data-stu-id="377c8-143">**DS\_REPSYNCALL\_UPDATE**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repsyncall_updatea)
-   [<span data-ttu-id="377c8-144">**\_mapa de \_ GUID de esquema DS \_**</span><span class="sxs-lookup"><span data-stu-id="377c8-144">**DS\_SCHEMA\_GUID\_MAP**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_schema_guid_mapa)
-   [<span data-ttu-id="377c8-145">**\_informações de \_ custo do site do DS \_**</span><span class="sxs-lookup"><span data-stu-id="377c8-145">**DS\_SITE\_COST\_INFO**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_site_cost_info)
-   [<span data-ttu-id="377c8-146">**AGENDAMENTO**</span><span class="sxs-lookup"><span data-stu-id="377c8-146">**SCHEDULE**</span></span>](/windows/desktop/api/Schedule/ns-schedule-schedule)
-   [<span data-ttu-id="377c8-147">**cabeçalho da agenda \_**</span><span class="sxs-lookup"><span data-stu-id="377c8-147">**SCHEDULE\_HEADER**</span></span>](/windows/desktop/api/Schedule/ns-schedule-schedule_header)

## <a name="related-topics"></a><span data-ttu-id="377c8-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="377c8-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="377c8-149">Estruturas no Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="377c8-149">Structures in Active Directory Domain Services</span></span>](structures-in-active-directory-domain-services.md)
</dt> </dl>

 

 