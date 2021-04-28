---
description: 'Método Msvm_CopyFileToGuestJob:: GetError – recupera o objeto de erro para o trabalho, se existir um.'
ms.assetid: 478E9170-A523-4CE1-BD97-57D713FAF71B
title: 'Método Msvm_CopyFileToGuestJob:: GetError'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c7cecaf7254788ae064ca42f2ae0c26e8ad83d7e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119364"
---
# <a name="msvm_copyfiletoguestjobgeterror-method"></a><span data-ttu-id="eb127-103">\_Método Msvm CopyFileToGuestJob:: GetError</span><span class="sxs-lookup"><span data-stu-id="eb127-103">Msvm\_CopyFileToGuestJob::GetError method</span></span>

<span data-ttu-id="eb127-104">Recupera o objeto de erro para o trabalho, se houver um.</span><span class="sxs-lookup"><span data-stu-id="eb127-104">Retrieves the error object for the job, if one exists.</span></span> <span data-ttu-id="eb127-105">Quando o trabalho está em execução ou termina sem erro, esse método não retorna um objeto [**de \_ erro CIM**](/previous-versions//cc150671(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="eb127-105">When the job is executing or has terminated without error, this method does not return a [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)) object.</span></span> <span data-ttu-id="eb127-106">No entanto, se o trabalho falhou devido a algum problema interno ou porque o trabalho foi encerrado por um cliente, uma instância de **\_ erro CIM** é retornada.</span><span class="sxs-lookup"><span data-stu-id="eb127-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, a **CIM\_Error** instance is returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb127-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eb127-107">Syntax</span></span>


```C++
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="eb127-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eb127-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb127-109">*Erro* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="eb127-109">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb127-110">Se o status operacional do trabalho não for 2 (OK), esse método retornará uma instância inserida da classe [**de \_ erro Msvm**](msvm-error.md) , no formato CIM-XML.</span><span class="sxs-lookup"><span data-stu-id="eb127-110">If the operational status of the job is not 2 (OK), this method returns an embedded instance of the [**Msvm\_Error**](msvm-error.md) class, in CIM-XML format.</span></span> <span data-ttu-id="eb127-111">Se o status operacional do trabalho for 2 (OK), **NULL** será retornado.</span><span class="sxs-lookup"><span data-stu-id="eb127-111">If the operational status of the job is 2 (OK), **Null** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb127-112">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="eb127-112">Return value</span></span>

<span data-ttu-id="eb127-113">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="eb127-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="eb127-114">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="eb127-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="eb127-115">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="eb127-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="eb127-116">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="eb127-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="eb127-117">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="eb127-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="eb127-118">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="eb127-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="eb127-119">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="eb127-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="eb127-120">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="eb127-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="eb127-121">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="eb127-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="eb127-122">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="eb127-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="eb127-123">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="eb127-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="eb127-124">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="eb127-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="eb127-125">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="eb127-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="eb127-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb127-126">Requirements</span></span>



| <span data-ttu-id="eb127-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb127-127">Requirement</span></span> | <span data-ttu-id="eb127-128">Valor</span><span class="sxs-lookup"><span data-stu-id="eb127-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb127-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eb127-129">Minimum supported client</span></span><br/> | <span data-ttu-id="eb127-130">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="eb127-130">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="eb127-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eb127-131">Minimum supported server</span></span><br/> | <span data-ttu-id="eb127-132">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="eb127-132">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="eb127-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="eb127-133">Namespace</span></span><br/>                | <span data-ttu-id="eb127-134">\\\\\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="eb127-134">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="eb127-135">MOF</span><span class="sxs-lookup"><span data-stu-id="eb127-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eb127-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eb127-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="eb127-137">DLL</span><span class="sxs-lookup"><span data-stu-id="eb127-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb127-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="eb127-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="eb127-139">Consulte também</span><span class="sxs-lookup"><span data-stu-id="eb127-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb127-140">**Msvm \_ CopyFileToGuestJob**</span><span class="sxs-lookup"><span data-stu-id="eb127-140">**Msvm\_CopyFileToGuestJob**</span></span>](msvm-copyfiletoguestjob.md)
</dt> </dl>

 

