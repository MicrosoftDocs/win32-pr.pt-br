---
description: Configura os adaptadores de rede no sistema operacional convidado.
ms.assetid: 698e0c17-f8bd-433f-b982-5481f9701ba6
title: Método SetGuestNetworkAdapterConfiguration da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.SetGuestNetworkAdapterConfiguration
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 02c79df7aa08faa842e2b702b4cf18944e96bdfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505857"
---
# <a name="setguestnetworkadapterconfiguration-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="83f2e-103">Método SetGuestNetworkAdapterConfiguration da \_ classe VirtualSystemManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="83f2e-103">SetGuestNetworkAdapterConfiguration method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="83f2e-104">Configura os adaptadores de rede no sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="83f2e-104">Configures the network adapters within the guest operating system.</span></span> <span data-ttu-id="83f2e-105">Esses parâmetros de configuração são aplicados imediatamente após o estabelecimento da comunicação com o componente de integração do KVP Exchange em execução no sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="83f2e-105">These configuration parameters are applied immediately upon establishing communication with the KVP Exchange integration component running within the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="83f2e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="83f2e-106">Syntax</span></span>


```mof
uint32 SetGuestNetworkAdapterConfiguration(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 NetworkConfiguration[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="83f2e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="83f2e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83f2e-108">*ComputerSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="83f2e-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83f2e-109">Uma referência à instância [**de \_ ComputerSystem do CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) cujos adaptadores de rede devem ser configurados.</span><span class="sxs-lookup"><span data-stu-id="83f2e-109">A reference to the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance whose network adapters are to be configured.</span></span>

</dd> <dt>

<span data-ttu-id="83f2e-110">*NetworkConfiguration* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="83f2e-110">*NetworkConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83f2e-111">Uma matriz de instâncias inseridas da classe [**Msvm \_ GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="83f2e-111">An array of embedded instances of the [**Msvm\_GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md) class.</span></span> <span data-ttu-id="83f2e-112">Cada instância descreve os parâmetros de configuração para um dos adaptadores de rede na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="83f2e-112">Each instance describes the configuration parameters for one of the network adapters within the virtual machine.</span></span> <span data-ttu-id="83f2e-113">A propriedade **DHCPEnabled** deve ser especificada para cada instância.</span><span class="sxs-lookup"><span data-stu-id="83f2e-113">The **DHCPEnabled** property must be specified for each instance.</span></span>

</dd> <dt>

<span data-ttu-id="83f2e-114">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="83f2e-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="83f2e-115">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="83f2e-115">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83f2e-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="83f2e-116">Return value</span></span>

<span data-ttu-id="83f2e-117">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="83f2e-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="83f2e-118">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="83f2e-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="83f2e-119">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="83f2e-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="83f2e-120">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="83f2e-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="83f2e-121">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="83f2e-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="83f2e-122">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="83f2e-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="83f2e-123">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="83f2e-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="83f2e-124">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="83f2e-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="83f2e-125">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="83f2e-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="83f2e-126">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="83f2e-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="83f2e-127">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="83f2e-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="83f2e-128">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="83f2e-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="83f2e-129">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="83f2e-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="83f2e-130">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="83f2e-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="83f2e-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83f2e-131">Requirements</span></span>



| <span data-ttu-id="83f2e-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="83f2e-132">Requirement</span></span> | <span data-ttu-id="83f2e-133">Valor</span><span class="sxs-lookup"><span data-stu-id="83f2e-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83f2e-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83f2e-134">Minimum supported client</span></span><br/> | <span data-ttu-id="83f2e-135">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="83f2e-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="83f2e-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83f2e-136">Minimum supported server</span></span><br/> | <span data-ttu-id="83f2e-137">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="83f2e-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="83f2e-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="83f2e-138">Namespace</span></span><br/>                | <span data-ttu-id="83f2e-139">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="83f2e-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="83f2e-140">MOF</span><span class="sxs-lookup"><span data-stu-id="83f2e-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="83f2e-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="83f2e-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="83f2e-142">DLL</span><span class="sxs-lookup"><span data-stu-id="83f2e-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83f2e-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="83f2e-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="83f2e-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="83f2e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83f2e-145">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="83f2e-145">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

