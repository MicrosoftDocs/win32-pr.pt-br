---
description: Define a entrada de autorização de replicação para uma máquina virtual.
ms.assetid: 39b6b0c4-5515-4863-9038-4c37421abe65
title: Método SetAuthorizationEntry da classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.SetAuthorizationEntry
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 03b2c2c37a38e957a1b560e2314845abf204ee01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758631"
---
# <a name="setauthorizationentry-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="b4491-103">Método SetAuthorizationEntry da \_ classe ReplicationService Msvm</span><span class="sxs-lookup"><span data-stu-id="b4491-103">SetAuthorizationEntry method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="b4491-104">Define a entrada de autorização de replicação para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b4491-104">Sets the replication authorization entry for a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4491-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b4491-105">Syntax</span></span>


```mof
uint32 SetAuthorizationEntry(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 AuthorizationEntry,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="b4491-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b4491-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4491-107">*ComputerSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b4491-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4491-108">Uma referência a uma instância de [**\_ sistema**](/windows/desktop/CIMWin32Prov/cim-computersystem) de computador CIM que representa a máquina virtual para a qual definir a entrada de autorização.</span><span class="sxs-lookup"><span data-stu-id="b4491-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine to set the authorization entry for.</span></span>

</dd> <dt>

<span data-ttu-id="b4491-109">*AuthorizationEntry* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b4491-109">*AuthorizationEntry* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4491-110">Uma representação de cadeia de caracteres de uma instância da classe [**Msvm \_ ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md) que define a entrada de autorização a ser usada para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b4491-110">A string representation of an instance of the [**Msvm\_ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md) class that defines the authorization entry to be used for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="b4491-111">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="b4491-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4491-112">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b4491-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4491-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b4491-113">Return value</span></span>

<span data-ttu-id="b4491-114">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="b4491-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="b4491-115">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="b4491-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b4491-116">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="b4491-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="b4491-117">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="b4491-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="b4491-118">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="b4491-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="b4491-119">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="b4491-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="b4491-120">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="b4491-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="b4491-121">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="b4491-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="b4491-122">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="b4491-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="b4491-123">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="b4491-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="b4491-124">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="b4491-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="b4491-125">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="b4491-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="b4491-126">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="b4491-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="b4491-127">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="b4491-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="b4491-128">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="b4491-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="b4491-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4491-129">Requirements</span></span>



| <span data-ttu-id="b4491-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4491-130">Requirement</span></span> | <span data-ttu-id="b4491-131">Valor</span><span class="sxs-lookup"><span data-stu-id="b4491-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4491-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b4491-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b4491-133">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b4491-133">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b4491-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b4491-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b4491-135">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b4491-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b4491-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="b4491-136">Namespace</span></span><br/>                | <span data-ttu-id="b4491-137">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="b4491-137">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b4491-138">MOF</span><span class="sxs-lookup"><span data-stu-id="b4491-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b4491-139"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b4491-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b4491-140">DLL</span><span class="sxs-lookup"><span data-stu-id="b4491-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4491-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b4491-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b4491-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="b4491-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4491-143">**AddAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="b4491-143">**AddAuthorizationEntry**</span></span>](addauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="b4491-144">**ModifyAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="b4491-144">**ModifyAuthorizationEntry**</span></span>](modifyauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="b4491-145">**RemoveAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="b4491-145">**RemoveAuthorizationEntry**</span></span>](removeauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="b4491-146">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="b4491-146">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

