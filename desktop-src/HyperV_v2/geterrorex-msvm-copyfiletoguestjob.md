---
description: Recupera os objetos de erro para o trabalho, caso existam.
ms.assetid: 817AF83B-B601-4AE4-AB5B-CFEACB9A7F41
title: 'Método Msvm_CopyFileToGuestJob:: GetErrorEx'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 179ad3a70a985442d855d447ef4eab955d177f0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754672"
---
# <a name="msvm_copyfiletoguestjobgeterrorex-method"></a><span data-ttu-id="66ca8-103">\_Método Msvm CopyFileToGuestJob:: GetErrorEx</span><span class="sxs-lookup"><span data-stu-id="66ca8-103">Msvm\_CopyFileToGuestJob::GetErrorEx method</span></span>

<span data-ttu-id="66ca8-104">Recupera os objetos de erro para o trabalho, caso existam.</span><span class="sxs-lookup"><span data-stu-id="66ca8-104">Retrieves the error objects for the job, if any exist.</span></span> <span data-ttu-id="66ca8-105">Quando o trabalho está em execução ou foi encerrado sem erros, esse método não retorna nenhuma instância de [**\_ erro Msvm**](msvm-error.md) .</span><span class="sxs-lookup"><span data-stu-id="66ca8-105">When the job is executing or has terminated without error, this method returns no [**Msvm\_Error**](msvm-error.md) instance.</span></span> <span data-ttu-id="66ca8-106">No entanto, se o trabalho falhou devido a algum problema interno ou porque o trabalho foi encerrado por um cliente, uma ou mais instâncias de **\_ erro Msvm** são retornadas.</span><span class="sxs-lookup"><span data-stu-id="66ca8-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, one or more **Msvm\_Error** instances are returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="66ca8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66ca8-107">Syntax</span></span>


```C++
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a><span data-ttu-id="66ca8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66ca8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66ca8-109">*Erros* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="66ca8-109">*Errors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="66ca8-110">Se o status operacional do trabalho não for 2 (OK), esse método retornará uma ou mais instâncias inseridas da classe [**de \_ erro Msvm**](msvm-error.md) , no formato CIM-XML, que representa os erros encontrados no trabalho.</span><span class="sxs-lookup"><span data-stu-id="66ca8-110">If the operational status of the job is not 2 (OK), this method returns one or more embedded instances of the [**Msvm\_Error**](msvm-error.md) class, in CIM-XML format, that represent the errors encountered in the job.</span></span> <span data-ttu-id="66ca8-111">Se o status operacional do trabalho for 2 (OK), será retornado **NULL** .</span><span class="sxs-lookup"><span data-stu-id="66ca8-111">If the operational status of the job is 2 (OK), then **Null** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66ca8-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="66ca8-112">Return value</span></span>

<span data-ttu-id="66ca8-113">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="66ca8-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="66ca8-114">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="66ca8-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="66ca8-115">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="66ca8-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="66ca8-116">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="66ca8-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="66ca8-117">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="66ca8-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="66ca8-118">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="66ca8-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="66ca8-119">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="66ca8-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="66ca8-120">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="66ca8-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="66ca8-121">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="66ca8-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="66ca8-122">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="66ca8-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="66ca8-123">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="66ca8-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="66ca8-124">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="66ca8-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="66ca8-125">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="66ca8-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="66ca8-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66ca8-126">Requirements</span></span>



| <span data-ttu-id="66ca8-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="66ca8-127">Requirement</span></span> | <span data-ttu-id="66ca8-128">Valor</span><span class="sxs-lookup"><span data-stu-id="66ca8-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66ca8-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66ca8-129">Minimum supported client</span></span><br/> | <span data-ttu-id="66ca8-130">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="66ca8-130">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="66ca8-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66ca8-131">Minimum supported server</span></span><br/> | <span data-ttu-id="66ca8-132">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="66ca8-132">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="66ca8-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="66ca8-133">Namespace</span></span><br/>                | <span data-ttu-id="66ca8-134">\\\\\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="66ca8-134">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="66ca8-135">MOF</span><span class="sxs-lookup"><span data-stu-id="66ca8-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="66ca8-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="66ca8-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="66ca8-137">DLL</span><span class="sxs-lookup"><span data-stu-id="66ca8-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66ca8-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="66ca8-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="66ca8-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="66ca8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66ca8-140">**Msvm \_ CopyFileToGuestJob**</span><span class="sxs-lookup"><span data-stu-id="66ca8-140">**Msvm\_CopyFileToGuestJob**</span></span>](msvm-copyfiletoguestjob.md)
</dt> </dl>

 

 




