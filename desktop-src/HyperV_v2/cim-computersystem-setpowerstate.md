---
description: Define o estado de energia do computador. O uso deste método foi preterido. Em vez disso, use o método SetPowerState na classe PowerManagementService associada.
ms.assetid: c2196f35-f687-4d82-a068-f8499f77473a
title: Método SetPowerState da classe CIM_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystem.SetPowerState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9c9e264e8ec62c1e49e92226d1abc8ac902c0b2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011166"
---
# <a name="setpowerstate-method-of-the-cim_computersystem-class"></a><span data-ttu-id="517fb-105">Método SetPowerState da classe de \_ sistema CIM</span><span class="sxs-lookup"><span data-stu-id="517fb-105">SetPowerState method of the CIM\_ComputerSystem class</span></span>

<span data-ttu-id="517fb-106">Define o estado de energia do computador.</span><span class="sxs-lookup"><span data-stu-id="517fb-106">Sets the power state of the computer.</span></span> <span data-ttu-id="517fb-107">O uso deste método foi preterido.</span><span class="sxs-lookup"><span data-stu-id="517fb-107">The use of this method has been deprecated.</span></span> <span data-ttu-id="517fb-108">Em vez disso, use o método **SetPowerState** na classe **PowerManagementService** associada.</span><span class="sxs-lookup"><span data-stu-id="517fb-108">Instead, use the **SetPowerState** method in the associated **PowerManagementService** class.</span></span>

## <a name="syntax"></a><span data-ttu-id="517fb-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="517fb-109">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint32   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="517fb-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="517fb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="517fb-111">*PowerState* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="517fb-111">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="517fb-112">O estado desejado para o sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="517fb-112">The desired state for the computer system.</span></span>

<dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span data-ttu-id="517fb-113">**Energia completa** (1)</span><span class="sxs-lookup"><span data-stu-id="517fb-113">**Full Power** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="517fb-114">Economia **de energia-modo de baixa energia** (2)</span><span class="sxs-lookup"><span data-stu-id="517fb-114">**Power Save - Low Power Mode** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="517fb-115">**Power Save-em espera** (3)</span><span class="sxs-lookup"><span data-stu-id="517fb-115">**Power Save - Standby** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>

<span data-ttu-id="517fb-116">Economia **de energia-outro** (4)</span><span class="sxs-lookup"><span data-stu-id="517fb-116">**Power Save - Other** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="517fb-117">**Ciclo de energia** (5)</span><span class="sxs-lookup"><span data-stu-id="517fb-117">**Power Cycle** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="517fb-118">**Desligar (6** )</span><span class="sxs-lookup"><span data-stu-id="517fb-118">**Power Off** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Hibernate"></span><span id="hibernate"></span><span id="HIBERNATE"></span>

<span data-ttu-id="517fb-119">**Hibernação** (7)</span><span class="sxs-lookup"><span data-stu-id="517fb-119">**Hibernate** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Soft_Off"></span><span id="soft_off"></span><span id="SOFT_OFF"></span>

<span data-ttu-id="517fb-120">**Soft off** (8)</span><span class="sxs-lookup"><span data-stu-id="517fb-120">**Soft Off** (8)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="517fb-121">*Tempo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="517fb-121">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="517fb-122">Time indica quando o estado de energia deve ser definido como um valor de data/hora regular ou como um valor de intervalo (em que o intervalo começa quando a invocação do método é recebida).</span><span class="sxs-lookup"><span data-stu-id="517fb-122">Time indicates when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="517fb-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="517fb-123">Requirements</span></span>



| <span data-ttu-id="517fb-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="517fb-124">Requirement</span></span> | <span data-ttu-id="517fb-125">Valor</span><span class="sxs-lookup"><span data-stu-id="517fb-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="517fb-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="517fb-126">Minimum supported client</span></span><br/> | <span data-ttu-id="517fb-127">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="517fb-127">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="517fb-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="517fb-128">Minimum supported server</span></span><br/> | <span data-ttu-id="517fb-129">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="517fb-129">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="517fb-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="517fb-130">Namespace</span></span><br/>                | <span data-ttu-id="517fb-131">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="517fb-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="517fb-132">MOF</span><span class="sxs-lookup"><span data-stu-id="517fb-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="517fb-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="517fb-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="517fb-134">DLL</span><span class="sxs-lookup"><span data-stu-id="517fb-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="517fb-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="517fb-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="517fb-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="517fb-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="517fb-137">**\_Sistema de COMPUTERSYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="517fb-137">**CIM\_ComputerSystem**</span></span>](cim-computersystem.md)
</dt> </dl>

 

 




