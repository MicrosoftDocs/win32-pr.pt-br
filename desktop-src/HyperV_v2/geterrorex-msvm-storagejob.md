---
description: Quando o trabalho está em execução ou foi encerrado sem erros, esse método não retorna nenhuma \_ instância de erro Msvm.
ms.assetid: 119E7EFD-78C9-46F1-8A53-C51A7A34B32E
title: Método GetErrorEx da classe Msvm_StorageJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 26d5aff37631de00cffccd49cf54f0ba09ce5a96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105769345"
---
# <a name="geterrorex-method-of-the-msvm_storagejob-class"></a><span data-ttu-id="532bb-103">Método GetErrorEx da \_ classe StorageJob Msvm</span><span class="sxs-lookup"><span data-stu-id="532bb-103">GetErrorEx method of the Msvm\_StorageJob class</span></span>

<span data-ttu-id="532bb-104">Quando o trabalho está em execução ou foi encerrado sem erros, esse método não retorna nenhuma instância de [**\_ erro Msvm**](msvm-error.md) .</span><span class="sxs-lookup"><span data-stu-id="532bb-104">When the job is executing or has terminated without error, then this method returns no [**Msvm\_Error**](msvm-error.md) instance.</span></span> <span data-ttu-id="532bb-105">No entanto, se o trabalho falhou devido a algum problema interno ou porque o trabalho foi encerrado por um cliente, uma ou mais instâncias de **\_ erro Msvm** são retornadas.</span><span class="sxs-lookup"><span data-stu-id="532bb-105">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then one or more **Msvm\_Error** instances are returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="532bb-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="532bb-106">Syntax</span></span>


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a><span data-ttu-id="532bb-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="532bb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="532bb-108">*Erros* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="532bb-108">*Errors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="532bb-109">Tipo: **cadeia \[ \] de caracteres**</span><span class="sxs-lookup"><span data-stu-id="532bb-109">Type: **string\[\]**</span></span>

<span data-ttu-id="532bb-110">Se o status operacional do trabalho não for "OK", esse método retornará uma matriz de instâncias [**de \_ erro Msvm**](msvm-error.md) .</span><span class="sxs-lookup"><span data-stu-id="532bb-110">If the operational status of the job is not "OK", this method returns an array of [**Msvm\_Error**](msvm-error.md) instances.</span></span> <span data-ttu-id="532bb-111">Caso contrário, se o trabalho for "OK", será retornado **nulo** .</span><span class="sxs-lookup"><span data-stu-id="532bb-111">Otherwise, if the job is "OK", **Null** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="532bb-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="532bb-112">Return value</span></span>

<span data-ttu-id="532bb-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="532bb-113">Type: **uint32**</span></span>

<span data-ttu-id="532bb-114">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="532bb-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="532bb-115">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="532bb-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="532bb-116">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="532bb-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="532bb-117">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="532bb-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="532bb-118">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="532bb-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="532bb-119">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="532bb-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="532bb-120">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="532bb-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="532bb-121">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="532bb-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="532bb-122">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="532bb-122">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="532bb-123">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="532bb-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="532bb-124">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="532bb-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="532bb-125">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="532bb-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="532bb-126">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="532bb-126">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="532bb-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="532bb-127">Remarks</span></span>

<span data-ttu-id="532bb-128">O acesso à classe [**Msvm \_ StorageJob**](msvm-storagejob.md) pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="532bb-128">Access to the [**Msvm\_StorageJob**](msvm-storagejob.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="532bb-129">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="532bb-129">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="532bb-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="532bb-130">Requirements</span></span>



| <span data-ttu-id="532bb-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="532bb-131">Requirement</span></span> | <span data-ttu-id="532bb-132">Valor</span><span class="sxs-lookup"><span data-stu-id="532bb-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="532bb-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="532bb-133">Minimum supported client</span></span><br/> | <span data-ttu-id="532bb-134">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="532bb-134">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="532bb-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="532bb-135">Minimum supported server</span></span><br/> | <span data-ttu-id="532bb-136">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="532bb-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="532bb-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="532bb-137">Namespace</span></span><br/>                | <span data-ttu-id="532bb-138">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="532bb-138">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="532bb-139">MOF</span><span class="sxs-lookup"><span data-stu-id="532bb-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="532bb-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="532bb-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="532bb-141">DLL</span><span class="sxs-lookup"><span data-stu-id="532bb-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="532bb-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="532bb-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="532bb-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="532bb-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="532bb-144">**Msvm \_ StorageJob**</span><span class="sxs-lookup"><span data-stu-id="532bb-144">**Msvm\_StorageJob**</span></span>](msvm-storagejob.md)
</dt> </dl>

 

