---
description: O KTM define as seguintes máscaras de acesso à inscrição a serem usadas ao abrir inscrições.
ms.assetid: 93773eb7-141a-49f3-9306-ffbda2f4ab9f
title: Máscaras de acesso à inscrição (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63e4ebd67f93368215ebcdcd362595d0341adb52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760177"
---
# <a name="enlistment-access-masks"></a><span data-ttu-id="2ff1c-103">Máscaras de acesso à inscrição</span><span class="sxs-lookup"><span data-stu-id="2ff1c-103">Enlistment Access Masks</span></span>

<span data-ttu-id="2ff1c-104">O KTM define as seguintes máscaras de acesso à inscrição a serem usadas ao abrir inscrições.</span><span class="sxs-lookup"><span data-stu-id="2ff1c-104">KTM defines the following enlistment access masks to be used when opening enlistments.</span></span>

<dl> <dt>

<span data-ttu-id="2ff1c-105"><span id="ENLISTMENT_QUERY_INFORMATION"></span><span id="enlistment_query_information"></span>**\_informações de consulta de inscrição \_**</span><span class="sxs-lookup"><span data-stu-id="2ff1c-105"><span id="ENLISTMENT_QUERY_INFORMATION"></span><span id="enlistment_query_information"></span>**ENLISTMENT\_QUERY\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ff1c-106">0x00001</span><span class="sxs-lookup"><span data-stu-id="2ff1c-106">0x00001</span></span>
</dt> <dt>



<span data-ttu-id="2ff1c-107">O chamador pode consultar o KTM para obter informações sobre a inscrição.</span><span class="sxs-lookup"><span data-stu-id="2ff1c-107">The caller can query KTM for information about the enlistment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ff1c-108"><span id="ENLISTMENT_SET_INFORMATION"></span><span id="enlistment_set_information"></span>**\_informações do conjunto de inscrição \_**</span><span class="sxs-lookup"><span data-stu-id="2ff1c-108"><span id="ENLISTMENT_SET_INFORMATION"></span><span id="enlistment_set_information"></span>**ENLISTMENT\_SET\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ff1c-109">0x00002</span><span class="sxs-lookup"><span data-stu-id="2ff1c-109">0x00002</span></span>
</dt> <dt>



<span data-ttu-id="2ff1c-110">O chamador pode definir informações sobre a inscrição.</span><span class="sxs-lookup"><span data-stu-id="2ff1c-110">The caller can set information about the enlistment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ff1c-111"><span id="ENLISTMENT_RECOVER"></span><span id="enlistment_recover"></span>**recuperação de inscrição \_**</span><span class="sxs-lookup"><span data-stu-id="2ff1c-111"><span id="ENLISTMENT_RECOVER"></span><span id="enlistment_recover"></span>**ENLISTMENT\_RECOVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ff1c-112">0x00004</span><span class="sxs-lookup"><span data-stu-id="2ff1c-112">0x00004</span></span>
</dt> <dt>



<span data-ttu-id="2ff1c-113">O chamador pode recuperar uma inscrição.</span><span class="sxs-lookup"><span data-stu-id="2ff1c-113">The caller can recover an enlistment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ff1c-114"><span id="ENLISTMENT_SUBORDINATE_RIGHTS"></span><span id="enlistment_subordinate_rights"></span>**\_direitos subordinados à inscrição \_**</span><span class="sxs-lookup"><span data-stu-id="2ff1c-114"><span id="ENLISTMENT_SUBORDINATE_RIGHTS"></span><span id="enlistment_subordinate_rights"></span>**ENLISTMENT\_SUBORDINATE\_RIGHTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ff1c-115">0x00008</span><span class="sxs-lookup"><span data-stu-id="2ff1c-115">0x00008</span></span>
</dt> <dt>



<span data-ttu-id="2ff1c-116">O chamador pode concluir ações que um Gerenciador de recursos faz em nome da transação.</span><span class="sxs-lookup"><span data-stu-id="2ff1c-116">The caller can complete actions that a resource manager does on behalf of the transaction.</span></span> <span data-ttu-id="2ff1c-117">A seguir está uma lista de ações:</span><span class="sxs-lookup"><span data-stu-id="2ff1c-117">The following is a list of actions:</span></span>

-   [<span data-ttu-id="2ff1c-118">**CommitComplete**</span><span class="sxs-lookup"><span data-stu-id="2ff1c-118">**CommitComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
-   [<span data-ttu-id="2ff1c-119">**PrepareComplete**</span><span class="sxs-lookup"><span data-stu-id="2ff1c-119">**PrepareComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
-   [<span data-ttu-id="2ff1c-120">**PrePrepareComplete**</span><span class="sxs-lookup"><span data-stu-id="2ff1c-120">**PrePrepareComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)
-   [<span data-ttu-id="2ff1c-121">**RollbackComplete**</span><span class="sxs-lookup"><span data-stu-id="2ff1c-121">**RollbackComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackcomplete)
-   [<span data-ttu-id="2ff1c-122">**ReadOnlyEnlistment**</span><span class="sxs-lookup"><span data-stu-id="2ff1c-122">**ReadOnlyEnlistment**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-readonlyenlistment)
-   [<span data-ttu-id="2ff1c-123">**RollbackEnlistment**</span><span class="sxs-lookup"><span data-stu-id="2ff1c-123">**RollbackEnlistment**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment)
-   [<span data-ttu-id="2ff1c-124">**SinglePhaseReject**</span><span class="sxs-lookup"><span data-stu-id="2ff1c-124">**SinglePhaseReject**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ff1c-125"><span id="ENLISTMENT_SUPERIOR_RIGHTS"></span><span id="enlistment_superior_rights"></span>**\_direitos superiores de inscrição \_**</span><span class="sxs-lookup"><span data-stu-id="2ff1c-125"><span id="ENLISTMENT_SUPERIOR_RIGHTS"></span><span id="enlistment_superior_rights"></span>**ENLISTMENT\_SUPERIOR\_RIGHTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ff1c-126">0x00010</span><span class="sxs-lookup"><span data-stu-id="2ff1c-126">0x00010</span></span>
</dt> <dt>



<span data-ttu-id="2ff1c-127">O chamador pode se inscrever na transação como um Gerenciador de transações superior.</span><span class="sxs-lookup"><span data-stu-id="2ff1c-127">The caller can enlist in the transaction as a superior transaction manager.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ff1c-128"><span id="ENLISTMENT_GENERIC_READ"></span><span id="enlistment_generic_read"></span>**\_leitura genérica de inscrição \_**</span><span class="sxs-lookup"><span data-stu-id="2ff1c-128"><span id="ENLISTMENT_GENERIC_READ"></span><span id="enlistment_generic_read"></span>**ENLISTMENT\_GENERIC\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ff1c-129">0x20001</span><span class="sxs-lookup"><span data-stu-id="2ff1c-129">0x20001</span></span>
</dt> <dt>



<span data-ttu-id="2ff1c-130">O chamador tem os seguintes privilégios: **\_ \_ informações** **padrão de \_ \_ leitura** e consulta de inscrição.</span><span class="sxs-lookup"><span data-stu-id="2ff1c-130">The caller has the following privileges: **STANDARD\_RIGHTS\_READ** and **ENLISTMENT\_QUERY\_INFORMATION**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ff1c-131"><span id="ENLISTMENT_GENERIC_WRITE"></span><span id="enlistment_generic_write"></span>**\_gravação genérica de inscrição \_**</span><span class="sxs-lookup"><span data-stu-id="2ff1c-131"><span id="ENLISTMENT_GENERIC_WRITE"></span><span id="enlistment_generic_write"></span>**ENLISTMENT\_GENERIC\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ff1c-132">0x2001E</span><span class="sxs-lookup"><span data-stu-id="2ff1c-132">0x2001E</span></span>
</dt> <dt>



<span data-ttu-id="2ff1c-133">O chamador tem os seguintes privilégios: **\_ \_ gravação de direitos padrão**, **\_ \_ informações de conjunto de inscrição** e **\_ recuperação de inscrição**.</span><span class="sxs-lookup"><span data-stu-id="2ff1c-133">The caller has the following privileges: **STANDARD\_RIGHTS\_WRITE**, **ENLISTMENT\_SET\_INFORMATION**, and **ENLISTMENT\_RECOVER**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ff1c-134"><span id="ENLISTMENT_GENERIC_EXECUTE"></span><span id="enlistment_generic_execute"></span>**\_execução genérica de inscrição \_**</span><span class="sxs-lookup"><span data-stu-id="2ff1c-134"><span id="ENLISTMENT_GENERIC_EXECUTE"></span><span id="enlistment_generic_execute"></span>**ENLISTMENT\_GENERIC\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ff1c-135">0x2001C</span><span class="sxs-lookup"><span data-stu-id="2ff1c-135">0x2001C</span></span>
</dt> <dt>



<span data-ttu-id="2ff1c-136">O chamador tem os seguintes privilégios: **\_ direitos de \_ execução padrão**, **\_ recuperação de inscrição** e **\_ \_ direitos subordinados à inscrição**.</span><span class="sxs-lookup"><span data-stu-id="2ff1c-136">The caller has the following privileges: **STANDARD\_RIGHTS\_EXECUTE**, **ENLISTMENT\_RECOVER**, and **ENLISTMENT\_SUBORDINATE\_RIGHTS**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ff1c-137"><span id="ENLISTMENT_ALL_ACCESS"></span><span id="enlistment_all_access"></span>**\_todos os \_ acessos à inscrição**</span><span class="sxs-lookup"><span data-stu-id="2ff1c-137"><span id="ENLISTMENT_ALL_ACCESS"></span><span id="enlistment_all_access"></span>**ENLISTMENT\_ALL\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ff1c-138">0xF001F</span><span class="sxs-lookup"><span data-stu-id="2ff1c-138">0xF001F</span></span>
</dt> <dt>



<span data-ttu-id="2ff1c-139">Esse valor define todos os bits válidos para um valor de acesso à inscrição.</span><span class="sxs-lookup"><span data-stu-id="2ff1c-139">This value sets all valid bits for an enlistment access value.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2ff1c-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ff1c-140">Requirements</span></span>



| <span data-ttu-id="2ff1c-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ff1c-141">Requirement</span></span> | <span data-ttu-id="2ff1c-142">Valor</span><span class="sxs-lookup"><span data-stu-id="2ff1c-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2ff1c-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ff1c-143">Minimum supported client</span></span><br/> | <span data-ttu-id="2ff1c-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2ff1c-144">Windows Vista</span></span><br/>                                                           |
| <span data-ttu-id="2ff1c-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ff1c-145">Minimum supported server</span></span><br/> | <span data-ttu-id="2ff1c-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2ff1c-146">Windows Server 2008</span></span><br/>                                                     |
| <span data-ttu-id="2ff1c-147">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2ff1c-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ff1c-148"><dt>WinNT. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ff1c-148"><dt>WinNT.h</dt></span></span> </dl> |



 

 




