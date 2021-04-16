---
description: Define as configurações de IP de adaptadores de rede a serem aplicadas a uma máquina virtual após um failover.
ms.assetid: a49d089e-f5dc-4bfb-9f66-2593304b9795
title: Método SetFailoverNetworkAdapterSettings da classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.SetFailoverNetworkAdapterSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: da5bb8c820e1dbca5103c430a7b2ce2a525a8fca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787097"
---
# <a name="setfailovernetworkadaptersettings-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="9d327-103">Método SetFailoverNetworkAdapterSettings da \_ classe ReplicationService Msvm</span><span class="sxs-lookup"><span data-stu-id="9d327-103">SetFailoverNetworkAdapterSettings method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="9d327-104">Define as configurações de IP do adaptador de rede a serem aplicadas a uma máquina virtual após um failover.</span><span class="sxs-lookup"><span data-stu-id="9d327-104">Configures the network adapter's IP settings to be applied to a virtual machine after a failover.</span></span> <span data-ttu-id="9d327-105">Esses parâmetros de configuração são aplicados após uma operação de failover, imediatamente após o estabelecimento da comunicação com o componente de integração do Exchange KVP em execução no sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="9d327-105">These configuration parameters are applied after a failover operation, immediately upon establishing communication with the KVP Exchange integration component running within the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d327-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9d327-106">Syntax</span></span>


```mof
uint32 SetFailoverNetworkAdapterSettings(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 NetworkSettings[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="9d327-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9d327-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d327-108">*ComputerSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9d327-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d327-109">Uma referência a uma instância de [**\_ sistema**](/windows/desktop/CIMWin32Prov/cim-computersystem) de computador CIM que representa a máquina virtual cujos adaptadores de rede devem ser configurados.</span><span class="sxs-lookup"><span data-stu-id="9d327-109">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine whose network adapters are to be configured.</span></span>

</dd> <dt>

<span data-ttu-id="9d327-110">*NetworkSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9d327-110">*NetworkSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d327-111">Uma matriz de instâncias inseridas de objetos [**Msvm \_ FailoverNetworkAdapterSettingData**](msvm-failovernetworkadaptersettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="9d327-111">An array of embedded instances of [**Msvm\_FailoverNetworkAdapterSettingData**](msvm-failovernetworkadaptersettingdata.md) objects.</span></span> <span data-ttu-id="9d327-112">Cada instância descreve os parâmetros de configuração para um dos adaptadores de rede na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9d327-112">Each instance describes the configuration parameters for one of the network adapters within the virtual machine.</span></span> <span data-ttu-id="9d327-113">As propriedades **ipaddresss** e **DHCPEnabled** devem ser especificadas em cada instância.</span><span class="sxs-lookup"><span data-stu-id="9d327-113">The **IPAddresses** and **DHCPEnabled** properties must be specified on each instance.</span></span>

</dd> <dt>

<span data-ttu-id="9d327-114">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="9d327-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d327-115">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9d327-115">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d327-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9d327-116">Return value</span></span>

<span data-ttu-id="9d327-117">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="9d327-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="9d327-118">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="9d327-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9d327-119">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="9d327-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="9d327-120">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="9d327-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="9d327-121">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="9d327-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="9d327-122">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="9d327-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="9d327-123">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="9d327-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="9d327-124">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="9d327-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="9d327-125">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="9d327-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="9d327-126">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="9d327-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="9d327-127">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="9d327-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="9d327-128">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="9d327-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="9d327-129">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="9d327-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="9d327-130">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="9d327-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="9d327-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d327-131">Requirements</span></span>



| <span data-ttu-id="9d327-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d327-132">Requirement</span></span> | <span data-ttu-id="9d327-133">Valor</span><span class="sxs-lookup"><span data-stu-id="9d327-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d327-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9d327-134">Minimum supported client</span></span><br/> | <span data-ttu-id="9d327-135">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9d327-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9d327-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9d327-136">Minimum supported server</span></span><br/> | <span data-ttu-id="9d327-137">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9d327-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9d327-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="9d327-138">Namespace</span></span><br/>                | <span data-ttu-id="9d327-139">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="9d327-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9d327-140">MOF</span><span class="sxs-lookup"><span data-stu-id="9d327-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9d327-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9d327-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9d327-142">DLL</span><span class="sxs-lookup"><span data-stu-id="9d327-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d327-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9d327-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9d327-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="9d327-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d327-145">**InitiateFailover**</span><span class="sxs-lookup"><span data-stu-id="9d327-145">**InitiateFailover**</span></span>](initiatefailover-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="9d327-146">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="9d327-146">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="9d327-147">**RevertFailover**</span><span class="sxs-lookup"><span data-stu-id="9d327-147">**RevertFailover**</span></span>](revertfailover-msvm-replicationservice.md)
</dt> </dl>

 

