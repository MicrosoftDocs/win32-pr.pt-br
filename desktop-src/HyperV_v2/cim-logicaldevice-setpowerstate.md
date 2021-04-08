---
description: Define o estado de energia do dispositivo. O uso deste método foi preterido. Em vez disso, use o método SetPowerState na classe PowerManagementService associada.
ms.assetid: 2f53a8bd-18a8-45aa-92ad-68a33b6a42ab
title: Método SetPowerState da classe CIM_LogicalDevice (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.SetPowerState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a29f71806747e6d63f53618acd09d472ac8bdea5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922256"
---
# <a name="setpowerstate-method-of-the-cim_logicaldevice-class-hyper-v-management"></a><span data-ttu-id="87505-105">Método SetPowerState da classe CIM_LogicalDevice (gerenciamento do Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="87505-105">SetPowerState method of the CIM_LogicalDevice class (Hyper-V management)</span></span>

<span data-ttu-id="87505-106">Define o estado de energia do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="87505-106">Sets the power state of the Device.</span></span> <span data-ttu-id="87505-107">O uso deste método foi preterido.</span><span class="sxs-lookup"><span data-stu-id="87505-107">The use of this method has been deprecated.</span></span> <span data-ttu-id="87505-108">Em vez disso, use o método **SetPowerState** na classe **PowerManagementService** associada.</span><span class="sxs-lookup"><span data-stu-id="87505-108">Instead, use the **SetPowerState** method in the associated **PowerManagementService** class.</span></span>

## <a name="syntax"></a><span data-ttu-id="87505-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="87505-109">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="87505-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="87505-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87505-111">*PowerState* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="87505-111">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87505-112">O estado de energia a ser definido.</span><span class="sxs-lookup"><span data-stu-id="87505-112">The power state to set.</span></span>

<dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span data-ttu-id="87505-113">**Energia completa** (1)</span><span class="sxs-lookup"><span data-stu-id="87505-113">**Full Power** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="87505-114">Economia **de energia-modo de baixa energia** (2)</span><span class="sxs-lookup"><span data-stu-id="87505-114">**Power Save - Low Power Mode** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="87505-115">**Power Save-em espera** (3)</span><span class="sxs-lookup"><span data-stu-id="87505-115">**Power Save - Standby** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>

<span data-ttu-id="87505-116">Economia **de energia-outro** (4)</span><span class="sxs-lookup"><span data-stu-id="87505-116">**Power Save - Other** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="87505-117">**Ciclo de energia** (5)</span><span class="sxs-lookup"><span data-stu-id="87505-117">**Power Cycle** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="87505-118">**Desligar (6** )</span><span class="sxs-lookup"><span data-stu-id="87505-118">**Power Off** (6)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="87505-119">*Tempo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="87505-119">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87505-120">Time indica quando o estado de energia deve ser definido como um valor de data/hora regular ou como um valor de intervalo (em que o intervalo começa quando a invocação do método é recebida).</span><span class="sxs-lookup"><span data-stu-id="87505-120">Time indicates when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87505-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="87505-121">Return value</span></span>

<span data-ttu-id="87505-122">Retorna um 0 em caso de êxito; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="87505-122">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="87505-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87505-123">Requirements</span></span>



| <span data-ttu-id="87505-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="87505-124">Requirement</span></span> | <span data-ttu-id="87505-125">Valor</span><span class="sxs-lookup"><span data-stu-id="87505-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87505-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87505-126">Minimum supported client</span></span><br/> | <span data-ttu-id="87505-127">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="87505-127">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="87505-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87505-128">Minimum supported server</span></span><br/> | <span data-ttu-id="87505-129">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="87505-129">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="87505-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="87505-130">Namespace</span></span><br/>                | <span data-ttu-id="87505-131">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="87505-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="87505-132">MOF</span><span class="sxs-lookup"><span data-stu-id="87505-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="87505-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="87505-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="87505-134">DLL</span><span class="sxs-lookup"><span data-stu-id="87505-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87505-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="87505-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="87505-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="87505-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87505-137">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="87505-137">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




