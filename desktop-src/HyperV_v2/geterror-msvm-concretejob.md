---
description: Recupera o objeto de erro para o trabalho, se houver um.
ms.assetid: 7E810CBE-F18F-4EFA-B52E-631CD071D136
title: Método GetError da classe Msvm_ConcreteJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 63279d8bc08f0b9f1955f694470a3744defd8054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756765"
---
# <a name="geterror-method-of-the-msvm_concretejob-class"></a><span data-ttu-id="d4f57-103">Método GetError da \_ classe Msvm ConcreteJob</span><span class="sxs-lookup"><span data-stu-id="d4f57-103">GetError method of the Msvm\_ConcreteJob class</span></span>

<span data-ttu-id="d4f57-104">Recupera o objeto de erro para o trabalho, se houver um.</span><span class="sxs-lookup"><span data-stu-id="d4f57-104">Retrieves the error object for the job, if one exists.</span></span> <span data-ttu-id="d4f57-105">Quando o trabalho está em execução ou termina sem erro, esse método não retorna um objeto de [**\_ erro CIM**](/previous-versions//cc150671(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d4f57-105">When the job is executing or has terminated without error, then this method does not return a [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)) object.</span></span> <span data-ttu-id="d4f57-106">No entanto, se o trabalho falhou devido a algum problema interno ou porque o trabalho foi encerrado por um cliente, uma instância de **\_ erro CIM** é retornada.</span><span class="sxs-lookup"><span data-stu-id="d4f57-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then a **CIM\_Error** instance is returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4f57-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d4f57-107">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="d4f57-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d4f57-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4f57-109">*Erro* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="d4f57-109">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4f57-110">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d4f57-110">Type: **string**</span></span>

<span data-ttu-id="d4f57-111">Se o status operacional do trabalho não for 2 (OK), esse método retornará uma instância inserida da classe [**de \_ erro Msvm**](msvm-error.md) , no formato CIM-XML.</span><span class="sxs-lookup"><span data-stu-id="d4f57-111">If the operational status of the job is not 2 (OK), this method returns an embedded instance of the [**Msvm\_Error**](msvm-error.md) class, in CIM-XML format.</span></span> <span data-ttu-id="d4f57-112">Se o status operacional do trabalho for 2 (OK), será retornado **NULL** .</span><span class="sxs-lookup"><span data-stu-id="d4f57-112">If the operational status of the job is 2 (OK), then **Null** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4f57-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d4f57-113">Return value</span></span>

<span data-ttu-id="d4f57-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d4f57-114">Type: **uint32**</span></span>

<span data-ttu-id="d4f57-115">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="d4f57-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="d4f57-116">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="d4f57-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d4f57-117">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="d4f57-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="d4f57-118">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="d4f57-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="d4f57-119">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="d4f57-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="d4f57-120">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="d4f57-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="d4f57-121">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="d4f57-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="d4f57-122">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="d4f57-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="d4f57-123">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="d4f57-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="d4f57-124">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="d4f57-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="d4f57-125">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="d4f57-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="d4f57-126">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="d4f57-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="d4f57-127">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="d4f57-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="d4f57-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="d4f57-128">Remarks</span></span>

<span data-ttu-id="d4f57-129">O acesso à classe [**Msvm \_ ConcreteJob**](msvm-concretejob.md) pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="d4f57-129">Access to the [**Msvm\_ConcreteJob**](msvm-concretejob.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="d4f57-130">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="d4f57-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="d4f57-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4f57-131">Requirements</span></span>



| <span data-ttu-id="d4f57-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4f57-132">Requirement</span></span> | <span data-ttu-id="d4f57-133">Valor</span><span class="sxs-lookup"><span data-stu-id="d4f57-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4f57-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d4f57-134">Minimum supported client</span></span><br/> | <span data-ttu-id="d4f57-135">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d4f57-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d4f57-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d4f57-136">Minimum supported server</span></span><br/> | <span data-ttu-id="d4f57-137">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d4f57-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d4f57-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="d4f57-138">Namespace</span></span><br/>                | <span data-ttu-id="d4f57-139">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="d4f57-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d4f57-140">MOF</span><span class="sxs-lookup"><span data-stu-id="d4f57-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d4f57-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d4f57-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d4f57-142">DLL</span><span class="sxs-lookup"><span data-stu-id="d4f57-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4f57-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d4f57-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d4f57-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="d4f57-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4f57-145">**Msvm \_ ConcreteJob**</span><span class="sxs-lookup"><span data-stu-id="d4f57-145">**Msvm\_ConcreteJob**</span></span>](msvm-concretejob.md)
</dt> </dl>

 

