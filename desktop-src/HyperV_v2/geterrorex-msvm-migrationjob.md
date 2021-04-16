---
description: Recupera os objetos de erro para o trabalho de migração, se existir algum.
ms.assetid: 8526e28c-bfc8-42b3-850c-0a875a52a42c
title: Método GetErrorEx da classe Msvm_MigrationJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MigrationJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b51bc0c439add0e0959d3fd375fad477e51ba35f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757818"
---
# <a name="geterrorex-method-of-the-msvm_migrationjob-class"></a><span data-ttu-id="e5a44-103">Método GetErrorEx da \_ classe MigrationJob Msvm</span><span class="sxs-lookup"><span data-stu-id="e5a44-103">GetErrorEx method of the Msvm\_MigrationJob class</span></span>

<span data-ttu-id="e5a44-104">Recupera os objetos de erro para o trabalho de migração, se existir algum.</span><span class="sxs-lookup"><span data-stu-id="e5a44-104">Retrieves the error objects for the migration job, if any exist.</span></span> <span data-ttu-id="e5a44-105">Quando o trabalho está em execução ou foi encerrado sem erros, esse método não retorna nenhuma instância de [**\_ erro Msvm**](msvm-error.md) .</span><span class="sxs-lookup"><span data-stu-id="e5a44-105">When the job is executing or has terminated without error, then this method returns no [**Msvm\_Error**](msvm-error.md) instance.</span></span> <span data-ttu-id="e5a44-106">No entanto, se o trabalho falhou devido a algum problema interno ou porque o trabalho foi encerrado por um cliente, uma ou mais instâncias de **\_ erro Msvm** são retornadas.</span><span class="sxs-lookup"><span data-stu-id="e5a44-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then one or more **Msvm\_Error** instances are returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5a44-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e5a44-107">Syntax</span></span>


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a><span data-ttu-id="e5a44-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e5a44-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5a44-109">*Erros* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="e5a44-109">*Errors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5a44-110">Se o status operacional do trabalho não for 2 (OK), esse método retornará uma ou mais instâncias inseridas da classe [**de \_ erro Msvm**](msvm-error.md) , no formato CIM-XML, que representa os erros encontrados no trabalho.</span><span class="sxs-lookup"><span data-stu-id="e5a44-110">If the operational status of the job is not 2 (OK), this method returns one or more embedded instances of the [**Msvm\_Error**](msvm-error.md) class, in CIM-XML format, that represent the errors encountered in the job.</span></span> <span data-ttu-id="e5a44-111">Se o status operacional do trabalho for 2 (OK), será retornado **NULL** .</span><span class="sxs-lookup"><span data-stu-id="e5a44-111">If the operational status of the job is 2 (OK), then **Null** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5a44-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e5a44-112">Return value</span></span>

<span data-ttu-id="e5a44-113">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="e5a44-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="e5a44-114">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="e5a44-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e5a44-115">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="e5a44-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="e5a44-116">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="e5a44-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="e5a44-117">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="e5a44-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="e5a44-118">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="e5a44-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="e5a44-119">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="e5a44-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="e5a44-120">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="e5a44-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="e5a44-121">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="e5a44-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="e5a44-122">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="e5a44-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="e5a44-123">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="e5a44-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="e5a44-124">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="e5a44-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="e5a44-125">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="e5a44-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e5a44-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5a44-126">Requirements</span></span>



| <span data-ttu-id="e5a44-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5a44-127">Requirement</span></span> | <span data-ttu-id="e5a44-128">Valor</span><span class="sxs-lookup"><span data-stu-id="e5a44-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5a44-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5a44-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e5a44-130">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e5a44-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e5a44-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5a44-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e5a44-132">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e5a44-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e5a44-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="e5a44-133">Namespace</span></span><br/>                | <span data-ttu-id="e5a44-134">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="e5a44-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e5a44-135">MOF</span><span class="sxs-lookup"><span data-stu-id="e5a44-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e5a44-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e5a44-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e5a44-137">DLL</span><span class="sxs-lookup"><span data-stu-id="e5a44-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5a44-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e5a44-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e5a44-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="e5a44-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5a44-140">**Msvm \_ MigrationJob**</span><span class="sxs-lookup"><span data-stu-id="e5a44-140">**Msvm\_MigrationJob**</span></span>](msvm-migrationjob.md)
</dt> </dl>

 

 




