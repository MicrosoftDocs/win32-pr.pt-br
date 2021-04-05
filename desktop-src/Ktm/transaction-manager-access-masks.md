---
description: O KTM define as seguintes máscaras de acesso à inscrição a serem usadas ao abrir um Gerenciador de transações (TM).
ms.assetid: 8f9b9d3d-e7ea-4df2-82b1-2d4c3e0766c0
title: Máscaras de acesso do Gerenciador de transações (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efae6c0bac1fc2bfa117e74e38aff8d439eb2f25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828113"
---
# <a name="transaction-manager-access-masks"></a><span data-ttu-id="5c87b-103">Máscaras de acesso do Gerenciador de transações</span><span class="sxs-lookup"><span data-stu-id="5c87b-103">Transaction Manager Access Masks</span></span>

<span data-ttu-id="5c87b-104">O KTM define as seguintes máscaras de acesso à inscrição a serem usadas ao abrir um Gerenciador de transações (TM).</span><span class="sxs-lookup"><span data-stu-id="5c87b-104">KTM defines the following enlistment access masks to be used when opening a transaction manager (TM).</span></span>

<dl> <dt>

<span data-ttu-id="5c87b-105"><span id="TRANSACTIONMANAGER_QUERY_INFORMATION"></span><span id="transactionmanager_query_information"></span>**informações de consulta TransactionManager \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5c87b-105"><span id="TRANSACTIONMANAGER_QUERY_INFORMATION"></span><span id="transactionmanager_query_information"></span>**TRANSACTIONMANAGER\_QUERY\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c87b-106">0x00001</span><span class="sxs-lookup"><span data-stu-id="5c87b-106">0x00001</span></span>
</dt> <dt>



<span data-ttu-id="5c87b-107">O chamador pode consultar informações sobre este TM.</span><span class="sxs-lookup"><span data-stu-id="5c87b-107">The caller can query information about this TM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5c87b-108"><span id="TRANSACTIONMANAGER_SET_INFORMATION"></span><span id="transactionmanager_set_information"></span>**informações de definição de TransactionManager \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5c87b-108"><span id="TRANSACTIONMANAGER_SET_INFORMATION"></span><span id="transactionmanager_set_information"></span>**TRANSACTIONMANAGER\_SET\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c87b-109">0x00002</span><span class="sxs-lookup"><span data-stu-id="5c87b-109">0x00002</span></span>
</dt> <dt>



<span data-ttu-id="5c87b-110">O chamador pode definir informações sobre este TM.</span><span class="sxs-lookup"><span data-stu-id="5c87b-110">The caller can set information about this TM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5c87b-111"><span id="TRANSACTIONMANAGER_RECOVER"></span><span id="transactionmanager_recover"></span>**recuperação de transacionator \_**</span><span class="sxs-lookup"><span data-stu-id="5c87b-111"><span id="TRANSACTIONMANAGER_RECOVER"></span><span id="transactionmanager_recover"></span>**TRANSACTIONMANAGER\_RECOVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c87b-112">0x00004</span><span class="sxs-lookup"><span data-stu-id="5c87b-112">0x00004</span></span>
</dt> <dt>



<span data-ttu-id="5c87b-113">O chamador pode recuperar este TM.</span><span class="sxs-lookup"><span data-stu-id="5c87b-113">The caller can recover this TM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5c87b-114"><span id="TRANSACTIONMANAGER_RENAME"></span><span id="transactionmanager_rename"></span>**renomeação de TransactionManager \_**</span><span class="sxs-lookup"><span data-stu-id="5c87b-114"><span id="TRANSACTIONMANAGER_RENAME"></span><span id="transactionmanager_rename"></span>**TRANSACTIONMANAGER\_RENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c87b-115">0x00008</span><span class="sxs-lookup"><span data-stu-id="5c87b-115">0x00008</span></span>
</dt> <dt>



<span data-ttu-id="5c87b-116">O chamador pode renomear uma instância de TM.</span><span class="sxs-lookup"><span data-stu-id="5c87b-116">The caller can rename a TM instance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5c87b-117"><span id="TRANSACTIONMANAGER_CREATE_RM"></span><span id="transactionmanager_create_rm"></span>**\_criar RM de transação \_**</span><span class="sxs-lookup"><span data-stu-id="5c87b-117"><span id="TRANSACTIONMANAGER_CREATE_RM"></span><span id="transactionmanager_create_rm"></span>**TRANSACTIONMANAGER\_CREATE\_RM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c87b-118">0x00010</span><span class="sxs-lookup"><span data-stu-id="5c87b-118">0x00010</span></span>
</dt> <dt>



<span data-ttu-id="5c87b-119">O chamador pode criar um Gerenciador de recursos associado a este TM.</span><span class="sxs-lookup"><span data-stu-id="5c87b-119">The caller can create a resource manager that is associated with this TM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5c87b-120"><span id="TRANSACTIONMANAGER_BIND_TRANSACTION"></span><span id="transactionmanager_bind_transaction"></span>**transação de associação TransactionManager \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5c87b-120"><span id="TRANSACTIONMANAGER_BIND_TRANSACTION"></span><span id="transactionmanager_bind_transaction"></span>**TRANSACTIONMANAGER\_BIND\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c87b-121">0x00020</span><span class="sxs-lookup"><span data-stu-id="5c87b-121">0x00020</span></span>
</dt> <dt>



<span data-ttu-id="5c87b-122">Esse valor é reservado.</span><span class="sxs-lookup"><span data-stu-id="5c87b-122">This value is reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5c87b-123"><span id="TRANSACTIONMANAGER_GENERIC_READ"></span><span id="transactionmanager_generic_read"></span>**leitura genérica TransactionManager \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5c87b-123"><span id="TRANSACTIONMANAGER_GENERIC_READ"></span><span id="transactionmanager_generic_read"></span>**TRANSACTIONMANAGER\_GENERIC\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c87b-124">0x20001</span><span class="sxs-lookup"><span data-stu-id="5c87b-124">0x20001</span></span>
</dt> <dt>



<span data-ttu-id="5c87b-125">O chamador tem os seguintes privilégios: **\_ \_ as informações de consulta de leitura e transacionator** de **\_ direitos \_ padrão** .</span><span class="sxs-lookup"><span data-stu-id="5c87b-125">The caller has the following privileges: **STANDARD\_RIGHTS\_READ** and **TRANSACTIONMANAGER\_QUERY\_INFORMATION**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5c87b-126"><span id="TRANSACTIONMANAGER_GENERIC_WRITE"></span><span id="transactionmanager_generic_write"></span>**gravação genérica TransactionManager \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5c87b-126"><span id="TRANSACTIONMANAGER_GENERIC_WRITE"></span><span id="transactionmanager_generic_write"></span>**TRANSACTIONMANAGER\_GENERIC\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c87b-127">0x2001E</span><span class="sxs-lookup"><span data-stu-id="5c87b-127">0x2001E</span></span>
</dt> <dt>



<span data-ttu-id="5c87b-128">O chamador tem os seguintes privilégios: **\_ \_ gravação de direitos padrão**, **Transações de \_ definição \_ de TransactionManager**, **\_ renomeação** de **transacionator, \_ recuperação** e **TransactionManager \_ criar \_ RM**.</span><span class="sxs-lookup"><span data-stu-id="5c87b-128">The caller has the following privileges: **STANDARD\_RIGHTS\_WRITE**, **TRANSACTIONMANAGER\_SET\_INFORMATION**, **TRANSACTIONMANAGER\_RECOVER**, **TRANSACTIONMANAGER\_RENAME**, and **TRANSACTIONMANAGER\_CREATE\_RM**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5c87b-129"><span id="TRANSACTIONMANAGER_GENERIC_EXECUTE"></span><span id="transactionmanager_generic_execute"></span>**execução genérica TransactionManager \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5c87b-129"><span id="TRANSACTIONMANAGER_GENERIC_EXECUTE"></span><span id="transactionmanager_generic_execute"></span>**TRANSACTIONMANAGER\_GENERIC\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c87b-130">0x20000</span><span class="sxs-lookup"><span data-stu-id="5c87b-130">0x20000</span></span>
</dt> <dt>



<span data-ttu-id="5c87b-131">O chamador tem o seguinte privilégio: **direitos padrão são \_ \_ executados**.</span><span class="sxs-lookup"><span data-stu-id="5c87b-131">The caller has the following privilege: **STANDARD\_RIGHTS\_EXECUTE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5c87b-132"><span id="TRANSACTIONMANAGER_ALL_ACCESS"></span><span id="transactionmanager_all_access"></span>**\_todos os acessos de TRANSacçãomanager \_**</span><span class="sxs-lookup"><span data-stu-id="5c87b-132"><span id="TRANSACTIONMANAGER_ALL_ACCESS"></span><span id="transactionmanager_all_access"></span>**TRANSACTIONMANAGER\_ALL\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c87b-133">0xF003F</span><span class="sxs-lookup"><span data-stu-id="5c87b-133">0xF003F</span></span>
</dt> <dt>



<span data-ttu-id="5c87b-134">Esse valor define todos os bits válidos para um valor de acesso TM.</span><span class="sxs-lookup"><span data-stu-id="5c87b-134">This value sets all valid bits for a TM access value.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5c87b-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c87b-135">Requirements</span></span>



| <span data-ttu-id="5c87b-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c87b-136">Requirement</span></span> | <span data-ttu-id="5c87b-137">Valor</span><span class="sxs-lookup"><span data-stu-id="5c87b-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5c87b-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c87b-138">Minimum supported client</span></span><br/> | <span data-ttu-id="5c87b-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5c87b-139">Windows Vista</span></span><br/>                                                           |
| <span data-ttu-id="5c87b-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c87b-140">Minimum supported server</span></span><br/> | <span data-ttu-id="5c87b-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5c87b-141">Windows Server 2008</span></span><br/>                                                     |
| <span data-ttu-id="5c87b-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5c87b-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c87b-143"><dt>WinNT. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c87b-143"><dt>WinNT.h</dt></span></span> </dl> |



 

 




