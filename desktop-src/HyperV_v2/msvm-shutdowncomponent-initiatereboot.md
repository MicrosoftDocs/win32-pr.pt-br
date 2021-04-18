---
description: Inicia uma operação de reinicialização do sistema operacional na máquina virtual filho associada.
ms.assetid: 9f3ebbaf-ee0f-4c01-8f73-1f37c08a0feb
title: Método InitiateReboot da classe Msvm_ShutdownComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ShutdownComponent.InitiateReboot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 527569e8a5d6c2bb0a54294637ae19c13f5e3af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752674"
---
# <a name="initiatereboot-method-of-the-msvm_shutdowncomponent-class"></a><span data-ttu-id="dacbc-103">Método InitiateReboot da \_ classe ShutdownComponent Msvm</span><span class="sxs-lookup"><span data-stu-id="dacbc-103">InitiateReboot method of the Msvm\_ShutdownComponent class</span></span>

<span data-ttu-id="dacbc-104">Inicia uma operação de reinicialização do sistema operacional na máquina virtual filho associada.</span><span class="sxs-lookup"><span data-stu-id="dacbc-104">Initiates an operating system reboot operation on the associated child virtual machine.</span></span>

<span data-ttu-id="dacbc-105">Se zero (0) for retornado, a reinicialização foi iniciada com êxito.</span><span class="sxs-lookup"><span data-stu-id="dacbc-105">If zero (0) is returned, then the reboot was initiated successfully.</span></span> <span data-ttu-id="dacbc-106">Qualquer outro código de retorno indica uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="dacbc-106">Any other return code indicates an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="dacbc-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dacbc-107">Syntax</span></span>


```mof
uint32 InitiateReboot(
  [in] boolean Force,
  [in] string  Reason
);
```



## <a name="parameters"></a><span data-ttu-id="dacbc-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dacbc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dacbc-109">*Forçar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dacbc-109">*Force* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dacbc-110">Um sinalizador que, se verdadeiro, força os aplicativos a serem fechados, apesar de terem dados não salvos.</span><span class="sxs-lookup"><span data-stu-id="dacbc-110">A flag which, if TRUE, forces applications to be closed despite having unsaved data.</span></span>

</dd> <dt>

<span data-ttu-id="dacbc-111">*Motivo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dacbc-111">*Reason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dacbc-112">O motivo para a operação de reinicialização.</span><span class="sxs-lookup"><span data-stu-id="dacbc-112">The reason for the reboot operation.</span></span> <span data-ttu-id="dacbc-113">Esta é uma cadeia de caracteres definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="dacbc-113">This is a user-defined string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dacbc-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dacbc-114">Return value</span></span>

<span data-ttu-id="dacbc-115">Esse método retorna um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="dacbc-115">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="dacbc-116">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="dacbc-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dacbc-117">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="dacbc-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="dacbc-118">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="dacbc-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="dacbc-119">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="dacbc-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="dacbc-120">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="dacbc-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="dacbc-121">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="dacbc-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="dacbc-122">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="dacbc-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="dacbc-123">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="dacbc-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="dacbc-124">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="dacbc-124">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="dacbc-125">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="dacbc-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="dacbc-126">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="dacbc-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="dacbc-127">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="dacbc-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="dacbc-128">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="dacbc-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="dacbc-129">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="dacbc-129">**File not found** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="dacbc-130">**O sistema não está pronto** (32780)</span><span class="sxs-lookup"><span data-stu-id="dacbc-130">**The system is not ready** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="dacbc-131">**A máquina está bloqueada e não pode ser desligada sem a opção Force** (32781)</span><span class="sxs-lookup"><span data-stu-id="dacbc-131">**The machine is locked and cannot be shut down without the force option** (32781)</span></span>
</dt> <dt>

<span data-ttu-id="dacbc-132">**Um desligamento do sistema está em andamento** (32782)</span><span class="sxs-lookup"><span data-stu-id="dacbc-132">**A system shutdown is in progress** (32782)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="dacbc-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dacbc-133">Requirements</span></span>



| <span data-ttu-id="dacbc-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="dacbc-134">Requirement</span></span> | <span data-ttu-id="dacbc-135">Valor</span><span class="sxs-lookup"><span data-stu-id="dacbc-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dacbc-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dacbc-136">Minimum supported client</span></span><br/> | <span data-ttu-id="dacbc-137">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="dacbc-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="dacbc-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dacbc-138">Minimum supported server</span></span><br/> | <span data-ttu-id="dacbc-139">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="dacbc-139">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="dacbc-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="dacbc-140">Namespace</span></span><br/>                | <span data-ttu-id="dacbc-141">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="dacbc-141">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="dacbc-142">MOF</span><span class="sxs-lookup"><span data-stu-id="dacbc-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dacbc-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dacbc-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dacbc-144">DLL</span><span class="sxs-lookup"><span data-stu-id="dacbc-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dacbc-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dacbc-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dacbc-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="dacbc-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dacbc-147">**Msvm \_ ShutdownComponent**</span><span class="sxs-lookup"><span data-stu-id="dacbc-147">**Msvm\_ShutdownComponent**</span></span>](msvm-shutdowncomponent.md)
</dt> </dl>

 

 




