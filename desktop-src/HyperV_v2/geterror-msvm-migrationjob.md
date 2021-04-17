---
description: Recupera o objeto de erro para o trabalho de migração, se houver um.
ms.assetid: 83a68ded-086a-42d9-b76d-e46af70d9b43
title: Método GetError da classe Msvm_MigrationJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MigrationJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6dce1cb3728c854b1dac742099a3ca035d4865a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811875"
---
# <a name="geterror-method-of-the-msvm_migrationjob-class"></a><span data-ttu-id="9f6ed-103">Método GetError da \_ classe Msvm MigrationJob</span><span class="sxs-lookup"><span data-stu-id="9f6ed-103">GetError method of the Msvm\_MigrationJob class</span></span>

<span data-ttu-id="9f6ed-104">Recupera o objeto de erro para o trabalho de migração, se houver um.</span><span class="sxs-lookup"><span data-stu-id="9f6ed-104">Retrieves the error object for the migration job, if one exists.</span></span> <span data-ttu-id="9f6ed-105">Quando o trabalho está em execução ou termina sem erro, esse método não retorna um objeto de [**\_ erro CIM**](/previous-versions//cc150671(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9f6ed-105">When the job is executing or has terminated without error, then this method does not return a [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)) object.</span></span> <span data-ttu-id="9f6ed-106">No entanto, se o trabalho falhou devido a algum problema interno ou porque o trabalho foi encerrado por um cliente, uma instância de **\_ erro CIM** é retornada.</span><span class="sxs-lookup"><span data-stu-id="9f6ed-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then a **CIM\_Error** instance is returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f6ed-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f6ed-107">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="9f6ed-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9f6ed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f6ed-109">*Erro* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="9f6ed-109">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f6ed-110">Se o status operacional do trabalho não for 2 (OK), esse método retornará uma instância inserida da classe [**de \_ erro Msvm**](msvm-error.md) , no formato CIM-XML.</span><span class="sxs-lookup"><span data-stu-id="9f6ed-110">If the operational status of the job is not 2 (OK), this method returns an embedded instance of the [**Msvm\_Error**](msvm-error.md) class, in CIM-XML format.</span></span> <span data-ttu-id="9f6ed-111">Se o status operacional do trabalho for 2 (OK), será retornado **NULL** .</span><span class="sxs-lookup"><span data-stu-id="9f6ed-111">If the operational status of the job is 2 (OK), then **Null** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f6ed-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9f6ed-112">Return value</span></span>

<span data-ttu-id="9f6ed-113">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="9f6ed-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="9f6ed-114">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="9f6ed-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9f6ed-115">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="9f6ed-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="9f6ed-116">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="9f6ed-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="9f6ed-117">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="9f6ed-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="9f6ed-118">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="9f6ed-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="9f6ed-119">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="9f6ed-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="9f6ed-120">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="9f6ed-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="9f6ed-121">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="9f6ed-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="9f6ed-122">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="9f6ed-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="9f6ed-123">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="9f6ed-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="9f6ed-124">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="9f6ed-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="9f6ed-125">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="9f6ed-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="9f6ed-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f6ed-126">Requirements</span></span>



| <span data-ttu-id="9f6ed-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f6ed-127">Requirement</span></span> | <span data-ttu-id="9f6ed-128">Valor</span><span class="sxs-lookup"><span data-stu-id="9f6ed-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f6ed-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f6ed-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9f6ed-130">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9f6ed-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9f6ed-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f6ed-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9f6ed-132">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9f6ed-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9f6ed-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="9f6ed-133">Namespace</span></span><br/>                | <span data-ttu-id="9f6ed-134">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="9f6ed-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9f6ed-135">MOF</span><span class="sxs-lookup"><span data-stu-id="9f6ed-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f6ed-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9f6ed-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9f6ed-137">DLL</span><span class="sxs-lookup"><span data-stu-id="9f6ed-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f6ed-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9f6ed-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9f6ed-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="9f6ed-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f6ed-140">**Msvm \_ MigrationJob**</span><span class="sxs-lookup"><span data-stu-id="9f6ed-140">**Msvm\_MigrationJob**</span></span>](msvm-migrationjob.md)
</dt> </dl>

 

