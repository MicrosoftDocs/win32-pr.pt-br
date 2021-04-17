---
description: Recupera os objetos de erro para o trabalho, caso existam.
ms.assetid: B4B4F60C-9221-4125-8D42-F0F1D32C3E79
title: Método GetErrorEx da classe Msvm_ConcreteJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e938d41afad430051bebb08fc77d6edf6da44691
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770222"
---
# <a name="geterrorex-method-of-the-msvm_concretejob-class"></a><span data-ttu-id="5e5cb-103">Método GetErrorEx da \_ classe ConcreteJob Msvm</span><span class="sxs-lookup"><span data-stu-id="5e5cb-103">GetErrorEx method of the Msvm\_ConcreteJob class</span></span>

<span data-ttu-id="5e5cb-104">Recupera os objetos de erro para o trabalho, caso existam.</span><span class="sxs-lookup"><span data-stu-id="5e5cb-104">Retrieves the error objects for the job, if any exist.</span></span> <span data-ttu-id="5e5cb-105">Quando o trabalho está em execução ou foi encerrado sem erros, esse método não retorna nenhuma instância de [**\_ erro Msvm**](msvm-error.md) .</span><span class="sxs-lookup"><span data-stu-id="5e5cb-105">When the job is executing or has terminated without error, then this method returns no [**Msvm\_Error**](msvm-error.md) instance.</span></span> <span data-ttu-id="5e5cb-106">No entanto, se o trabalho falhou devido a algum problema interno ou porque o trabalho foi encerrado por um cliente, uma ou mais instâncias de **\_ erro Msvm** são retornadas.</span><span class="sxs-lookup"><span data-stu-id="5e5cb-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then one or more **Msvm\_Error** instances are returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e5cb-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5e5cb-107">Syntax</span></span>


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a><span data-ttu-id="5e5cb-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5e5cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e5cb-109">*Erros* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="5e5cb-109">*Errors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5e5cb-110">Tipo: **cadeia \[ \] de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5cb-110">Type: **string\[\]**</span></span>

<span data-ttu-id="5e5cb-111">Se o status operacional do trabalho não for 2 (OK), esse método retornará uma ou mais instâncias inseridas da classe [**de \_ erro Msvm**](msvm-error.md) , no formato CIM-XML, que representa os erros encontrados no trabalho.</span><span class="sxs-lookup"><span data-stu-id="5e5cb-111">If the operational status of the job is not 2 (OK), this method returns one or more embedded instances of the [**Msvm\_Error**](msvm-error.md) class, in CIM-XML format, that represent the errors encountered in the job.</span></span> <span data-ttu-id="5e5cb-112">Se o status operacional do trabalho for 2 (OK), será retornado **NULL** .</span><span class="sxs-lookup"><span data-stu-id="5e5cb-112">If the operational status of the job is 2 (OK), then **Null** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e5cb-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5e5cb-113">Return value</span></span>

<span data-ttu-id="5e5cb-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e5cb-114">Type: **uint32**</span></span>

<span data-ttu-id="5e5cb-115">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="5e5cb-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="5e5cb-116">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="5e5cb-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5e5cb-117">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="5e5cb-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="5e5cb-118">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="5e5cb-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="5e5cb-119">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="5e5cb-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="5e5cb-120">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="5e5cb-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="5e5cb-121">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="5e5cb-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="5e5cb-122">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="5e5cb-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="5e5cb-123">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="5e5cb-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="5e5cb-124">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="5e5cb-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="5e5cb-125">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="5e5cb-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="5e5cb-126">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="5e5cb-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="5e5cb-127">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="5e5cb-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="5e5cb-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="5e5cb-128">Remarks</span></span>

<span data-ttu-id="5e5cb-129">O acesso à classe [**Msvm \_ ConcreteJob**](msvm-concretejob.md) pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="5e5cb-129">Access to the [**Msvm\_ConcreteJob**](msvm-concretejob.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="5e5cb-130">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="5e5cb-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="5e5cb-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e5cb-131">Requirements</span></span>



| <span data-ttu-id="5e5cb-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e5cb-132">Requirement</span></span> | <span data-ttu-id="5e5cb-133">Valor</span><span class="sxs-lookup"><span data-stu-id="5e5cb-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e5cb-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e5cb-134">Minimum supported client</span></span><br/> | <span data-ttu-id="5e5cb-135">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="5e5cb-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5e5cb-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e5cb-136">Minimum supported server</span></span><br/> | <span data-ttu-id="5e5cb-137">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="5e5cb-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5e5cb-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="5e5cb-138">Namespace</span></span><br/>                | <span data-ttu-id="5e5cb-139">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="5e5cb-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5e5cb-140">MOF</span><span class="sxs-lookup"><span data-stu-id="5e5cb-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5e5cb-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5e5cb-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5e5cb-142">DLL</span><span class="sxs-lookup"><span data-stu-id="5e5cb-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e5cb-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5e5cb-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5e5cb-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="5e5cb-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e5cb-145">**Msvm \_ ConcreteJob**</span><span class="sxs-lookup"><span data-stu-id="5e5cb-145">**Msvm\_ConcreteJob**</span></span>](msvm-concretejob.md)
</dt> </dl>

 

