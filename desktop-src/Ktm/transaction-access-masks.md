---
description: O KTM define as seguintes máscaras de acesso à transação a serem usadas ao abrir uma transação.
ms.assetid: 93ef3098-b3cc-4b24-ae82-1c10d937f14f
title: Máscaras de acesso à transação (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b815bcb04a97dbd059c85c6c615a7d607bf77ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780624"
---
# <a name="transaction-access-masks"></a><span data-ttu-id="d4c6f-103">Máscaras de acesso à transação</span><span class="sxs-lookup"><span data-stu-id="d4c6f-103">Transaction Access Masks</span></span>

<span data-ttu-id="d4c6f-104">O KTM define as seguintes máscaras de acesso à transação a serem usadas ao abrir uma transação.</span><span class="sxs-lookup"><span data-stu-id="d4c6f-104">KTM defines the following transaction access masks to be used when opening a transaction.</span></span>

<dl> <dt>

<span data-ttu-id="d4c6f-105"><span id="TRANSACTION_QUERY_INFORMATION"></span><span id="transaction_query_information"></span>**\_informações de consulta de transação \_**</span><span class="sxs-lookup"><span data-stu-id="d4c6f-105"><span id="TRANSACTION_QUERY_INFORMATION"></span><span id="transaction_query_information"></span>**TRANSACTION\_QUERY\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4c6f-106">0x000001</span><span class="sxs-lookup"><span data-stu-id="d4c6f-106">0x000001</span></span>
</dt> <dt>



<span data-ttu-id="d4c6f-107">O chamador pode consultar informações de transação.</span><span class="sxs-lookup"><span data-stu-id="d4c6f-107">The caller can query transaction information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4c6f-108"><span id="TRANSACTION_SET_INFORMATION"></span><span id="transaction_set_information"></span>**\_informações do conjunto de transações \_**</span><span class="sxs-lookup"><span data-stu-id="d4c6f-108"><span id="TRANSACTION_SET_INFORMATION"></span><span id="transaction_set_information"></span>**TRANSACTION\_SET\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4c6f-109">0x000002</span><span class="sxs-lookup"><span data-stu-id="d4c6f-109">0x000002</span></span>
</dt> <dt>



<span data-ttu-id="d4c6f-110">O chamador pode definir informações de transação.</span><span class="sxs-lookup"><span data-stu-id="d4c6f-110">The caller can set transaction information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4c6f-111"><span id="TRANSACTION_ENLIST"></span><span id="transaction_enlist"></span>**inscrição de transação \_**</span><span class="sxs-lookup"><span data-stu-id="d4c6f-111"><span id="TRANSACTION_ENLIST"></span><span id="transaction_enlist"></span>**TRANSACTION\_ENLIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4c6f-112">0x000004</span><span class="sxs-lookup"><span data-stu-id="d4c6f-112">0x000004</span></span>
</dt> <dt>



<span data-ttu-id="d4c6f-113">O chamador pode se inscrever nessa transação.</span><span class="sxs-lookup"><span data-stu-id="d4c6f-113">The caller can enlist in this transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4c6f-114"><span id="TRANSACTION_COMMIT"></span><span id="transaction_commit"></span>**confirmação de transação \_**</span><span class="sxs-lookup"><span data-stu-id="d4c6f-114"><span id="TRANSACTION_COMMIT"></span><span id="transaction_commit"></span>**TRANSACTION\_COMMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4c6f-115">0x000008</span><span class="sxs-lookup"><span data-stu-id="d4c6f-115">0x000008</span></span>
</dt> <dt>



<span data-ttu-id="d4c6f-116">O chamador pode confirmar essa transação.</span><span class="sxs-lookup"><span data-stu-id="d4c6f-116">The caller can commit this transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4c6f-117"><span id="TRANSACTION_ROLLBACK"></span><span id="transaction_rollback"></span>**reversão de transação \_**</span><span class="sxs-lookup"><span data-stu-id="d4c6f-117"><span id="TRANSACTION_ROLLBACK"></span><span id="transaction_rollback"></span>**TRANSACTION\_ROLLBACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4c6f-118">0x000010</span><span class="sxs-lookup"><span data-stu-id="d4c6f-118">0x000010</span></span>
</dt> <dt>



<span data-ttu-id="d4c6f-119">O chamador pode reverter essa transação.</span><span class="sxs-lookup"><span data-stu-id="d4c6f-119">The caller can roll back this transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4c6f-120"><span id="TRANSACTION_PROPAGATE"></span><span id="transaction_propagate"></span>**propagação de transações \_**</span><span class="sxs-lookup"><span data-stu-id="d4c6f-120"><span id="TRANSACTION_PROPAGATE"></span><span id="transaction_propagate"></span>**TRANSACTION\_PROPAGATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4c6f-121">0x000020</span><span class="sxs-lookup"><span data-stu-id="d4c6f-121">0x000020</span></span>
</dt> <dt>



<span data-ttu-id="d4c6f-122">O chamador pode propagar essa transação para um Gerenciador de recursos superior, como o Coordenador de Transações Distribuídas (DTC).</span><span class="sxs-lookup"><span data-stu-id="d4c6f-122">The caller can propagate this transaction to a superior resource manager, such as the Distributed Transaction Coordinator (DTC).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4c6f-123"><span id="TRANSACTION_GENERIC_READ"></span><span id="transaction_generic_read"></span>**\_leitura genérica da transação \_**</span><span class="sxs-lookup"><span data-stu-id="d4c6f-123"><span id="TRANSACTION_GENERIC_READ"></span><span id="transaction_generic_read"></span>**TRANSACTION\_GENERIC\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4c6f-124">0x120001</span><span class="sxs-lookup"><span data-stu-id="d4c6f-124">0x120001</span></span>
</dt> <dt>



<span data-ttu-id="d4c6f-125">O chamador tem os seguintes privilégios: **\_ \_ leitura de direitos padrão**, **\_ \_ informações de consulta de transação** e **sincronização**.</span><span class="sxs-lookup"><span data-stu-id="d4c6f-125">The caller has the following privileges: **STANDARD\_RIGHTS\_READ**, **TRANSACTION\_QUERY\_INFORMATION**, and **SYNCHRONIZE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4c6f-126"><span id="TRANSACTION_GENERIC_WRITE"></span><span id="transaction_generic_write"></span>**\_gravação genérica de transação \_**</span><span class="sxs-lookup"><span data-stu-id="d4c6f-126"><span id="TRANSACTION_GENERIC_WRITE"></span><span id="transaction_generic_write"></span>**TRANSACTION\_GENERIC\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4c6f-127">0x12003E</span><span class="sxs-lookup"><span data-stu-id="d4c6f-127">0x12003E</span></span>
</dt> <dt>



<span data-ttu-id="d4c6f-128">O chamador tem os seguintes privilégios: **\_ \_ gravação de direitos padrão**, **\_ \_ informações de conjunto de transações**, **\_ confirmação de transação**, **\_ inscrição de transação**, **\_ reversão de transação**, **\_ propagação de transações** e **sincronização**.</span><span class="sxs-lookup"><span data-stu-id="d4c6f-128">The caller has the following privileges: **STANDARD\_RIGHTS\_WRITE**, **TRANSACTION\_SET\_INFORMATION**, **TRANSACTION\_COMMIT**, **TRANSACTION\_ENLIST**, **TRANSACTION\_ROLLBACK**, **TRANSACTION\_PROPAGATE**, and **SYNCHRONIZE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4c6f-129"><span id="TRANSACTION_GENERIC_EXECUTE"></span><span id="transaction_generic_execute"></span>**\_execução genérica da transação \_**</span><span class="sxs-lookup"><span data-stu-id="d4c6f-129"><span id="TRANSACTION_GENERIC_EXECUTE"></span><span id="transaction_generic_execute"></span>**TRANSACTION\_GENERIC\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4c6f-130">0x120018</span><span class="sxs-lookup"><span data-stu-id="d4c6f-130">0x120018</span></span>
</dt> <dt>



<span data-ttu-id="d4c6f-131">O chamador tem os seguintes privilégios: **\_ \_ execução de direitos padrão**, **\_ confirmação de transação**, **\_ reversão de transação** e **sincronização**.</span><span class="sxs-lookup"><span data-stu-id="d4c6f-131">The caller has the following privileges: **STANDARD\_RIGHTS\_EXECUTE**, **TRANSACTION\_COMMIT**, **TRANSACTION\_ROLLBACK**, and **SYNCHRONIZE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4c6f-132"><span id="TRANSACTION_ALL_ACCESS"></span><span id="transaction_all_access"></span>**\_todos os \_ acessos à transação**</span><span class="sxs-lookup"><span data-stu-id="d4c6f-132"><span id="TRANSACTION_ALL_ACCESS"></span><span id="transaction_all_access"></span>**TRANSACTION\_ALL\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4c6f-133">0x12003F</span><span class="sxs-lookup"><span data-stu-id="d4c6f-133">0x12003F</span></span>
</dt> <dt>



<span data-ttu-id="d4c6f-134">O chamador tem o seguinte privilégio: **\_ direitos padrão \_ necessários**, **\_ \_ leitura genérica de transação**, **\_ \_ gravação genérica de transação** e **\_ \_ execução genérica de transação**.</span><span class="sxs-lookup"><span data-stu-id="d4c6f-134">The caller has the following privilege: **STANDARD\_RIGHTS\_REQUIRED**, **TRANSACTION\_GENERIC\_READ**, **TRANSACTION\_GENERIC\_WRITE**, and **TRANSACTION\_GENERIC\_EXECUTE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4c6f-135"><span id="TRANSACTION_RESOURCE_MANAGER_RIGHTS"></span><span id="transaction_resource_manager_rights"></span>**\_direitos do \_ Gerenciador de recursos de transação \_**</span><span class="sxs-lookup"><span data-stu-id="d4c6f-135"><span id="TRANSACTION_RESOURCE_MANAGER_RIGHTS"></span><span id="transaction_resource_manager_rights"></span>**TRANSACTION\_RESOURCE\_MANAGER\_RIGHTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4c6f-136">0x120037</span><span class="sxs-lookup"><span data-stu-id="d4c6f-136">0x120037</span></span>
</dt> <dt>



<span data-ttu-id="d4c6f-137">O chamador tem os seguintes privilégios: **\_ \_ leitura genérica de transação**, **\_ \_ gravação de direitos padrão**, **\_ \_ informações de conjunto de transações**, **\_ reversão de transação**, **\_ inscrição de transação**, **\_ propagação de transações** e **sincronização**.</span><span class="sxs-lookup"><span data-stu-id="d4c6f-137">The caller has the following privileges: **TRANSACTION\_GENERIC\_READ**, **STANDARD\_RIGHTS\_WRITE**, **TRANSACTION\_SET\_INFORMATION**, **TRANSACTION\_ROLLBACK**, **TRANSACTION\_ENLIST**, **TRANSACTION\_PROPAGATE**, and **SYNCHRONIZE**.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d4c6f-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="d4c6f-138">Remarks</span></span>

<span data-ttu-id="d4c6f-139">É recomendável que os gerenciadores de recursos, ao se enlistar em uma transação, especifiquem os direitos do Gerenciador de recursos de transação ao abrir uma transação. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d4c6f-139">It is recommended that resource managers, when enlisting in a transaction, specify **TRANSACTION\_RESOURCE\_MANAGER\_RIGHTS** when opening a transaction.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4c6f-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4c6f-140">Requirements</span></span>



| <span data-ttu-id="d4c6f-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4c6f-141">Requirement</span></span> | <span data-ttu-id="d4c6f-142">Valor</span><span class="sxs-lookup"><span data-stu-id="d4c6f-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d4c6f-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d4c6f-143">Minimum supported client</span></span><br/> | <span data-ttu-id="d4c6f-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d4c6f-144">Windows Vista</span></span><br/>                                                           |
| <span data-ttu-id="d4c6f-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d4c6f-145">Minimum supported server</span></span><br/> | <span data-ttu-id="d4c6f-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d4c6f-146">Windows Server 2008</span></span><br/>                                                     |
| <span data-ttu-id="d4c6f-147">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d4c6f-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4c6f-148"><dt>WinNT. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4c6f-148"><dt>WinNT.h</dt></span></span> </dl> |



 

 




