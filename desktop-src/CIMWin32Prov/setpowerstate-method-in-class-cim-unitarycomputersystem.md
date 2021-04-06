---
description: O método SetPowerState da classe CIM \_ UnitaryComputerSystem define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.
ms.assetid: a02991d5-3c93-4579-b1f5-f70ad7c7052b
ms.tgt_platform: multiple
title: Método SetPowerState da classe CIM_UnitaryComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_UnitaryComputerSystem.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4d9b69306c7bb362dceaee254be5dae8f5d37a52
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920128"
---
# <a name="setpowerstate-method-of-the-cim_unitarycomputersystem-class"></a><span data-ttu-id="fab9b-103">Método SetPowerState da classe CIM \_ UnitaryComputerSystem</span><span class="sxs-lookup"><span data-stu-id="fab9b-103">SetPowerState method of the CIM\_UnitaryComputerSystem class</span></span>

<span data-ttu-id="fab9b-104">O método **SetPowerState** da classe CIM \_ UnitaryComputerSystem define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="fab9b-104">The **SetPowerState** method of the CIM\_UnitaryComputerSystem class sets the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="fab9b-105">Em uma subclasse, o conjunto de códigos de retorno possíveis deve ser especificado usando um qualificador **ValueMap** no método.</span><span class="sxs-lookup"><span data-stu-id="fab9b-105">In a subclass, the set of possible return codes should be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="fab9b-106">As cadeias de caracteres nas quais o conteúdo de **ValueMap** são traduzidos também devem ser especificadas na subclasse como um qualificador de matriz de **valores** .</span><span class="sxs-lookup"><span data-stu-id="fab9b-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="fab9b-107">Esse método é herdado [**do \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fab9b-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fab9b-108">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="fab9b-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="fab9b-109">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="fab9b-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="fab9b-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fab9b-110">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="fab9b-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fab9b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fab9b-112">*PowerState* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fab9b-112">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fab9b-113">Um valor de **ValueMap** que especifica o estado de energia desejado para esse dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="fab9b-113">A **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span data-ttu-id="fab9b-114"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Energia completa** (1)</span><span class="sxs-lookup"><span data-stu-id="fab9b-114"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Full Power** (1)</span></span>


</dt> <dd>

<span data-ttu-id="fab9b-115">Potência total.</span><span class="sxs-lookup"><span data-stu-id="fab9b-115">Full power.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="fab9b-116"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (2)</span><span class="sxs-lookup"><span data-stu-id="fab9b-116"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (2)</span></span>


</dt> <dd>

<span data-ttu-id="fab9b-117">Economia de energia no modo de baixa energia.</span><span class="sxs-lookup"><span data-stu-id="fab9b-117">Power save   low-power mode.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="fab9b-118"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (3)</span><span class="sxs-lookup"><span data-stu-id="fab9b-118"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (3)</span></span>


</dt> <dd>

<span data-ttu-id="fab9b-119">Power Save em espera.</span><span class="sxs-lookup"><span data-stu-id="fab9b-119">Power save   standby.</span></span>

</dd> <dt>

<span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>

<span data-ttu-id="fab9b-120"><span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>Economia **de energia-outro** (4)</span><span class="sxs-lookup"><span data-stu-id="fab9b-120"><span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>**Power Save - Other** (4)</span></span>


</dt> <dd>

<span data-ttu-id="fab9b-121">Economia de energia diferente.</span><span class="sxs-lookup"><span data-stu-id="fab9b-121">Power save   other.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="fab9b-122"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (5)</span><span class="sxs-lookup"><span data-stu-id="fab9b-122"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (5)</span></span>


</dt> <dd>

<span data-ttu-id="fab9b-123">Ciclo de energia.</span><span class="sxs-lookup"><span data-stu-id="fab9b-123">Power cycle.</span></span>

</dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="fab9b-124"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (6** )</span><span class="sxs-lookup"><span data-stu-id="fab9b-124"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (6)</span></span>


</dt> <dd>

<span data-ttu-id="fab9b-125">Desligar.</span><span class="sxs-lookup"><span data-stu-id="fab9b-125">Power off.</span></span>

</dd> <dt>

<span id="Hibernate"></span><span id="hibernate"></span><span id="HIBERNATE"></span>

<span data-ttu-id="fab9b-126"><span id="Hibernate"></span><span id="hibernate"></span><span id="HIBERNATE"></span>**Hibernação** (7)</span><span class="sxs-lookup"><span data-stu-id="fab9b-126"><span id="Hibernate"></span><span id="hibernate"></span><span id="HIBERNATE"></span>**Hibernate** (7)</span></span>


</dt> <dd>

<span data-ttu-id="fab9b-127">Hibernação.</span><span class="sxs-lookup"><span data-stu-id="fab9b-127">Hibernate.</span></span>

</dd> <dt>

<span id="Soft_Off"></span><span id="soft_off"></span><span id="SOFT_OFF"></span>

<span data-ttu-id="fab9b-128"><span id="Soft_Off"></span><span id="soft_off"></span><span id="SOFT_OFF"></span>**Soft off** (8)</span><span class="sxs-lookup"><span data-stu-id="fab9b-128"><span id="Soft_Off"></span><span id="soft_off"></span><span id="SOFT_OFF"></span>**Soft Off** (8)</span></span>


</dt> <dd>

<span data-ttu-id="fab9b-129">Soft off.</span><span class="sxs-lookup"><span data-stu-id="fab9b-129">Soft off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="fab9b-130">*Tempo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fab9b-130">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fab9b-131">Especifica quando o estado de energia deve ser definido, seja como um valor de data/hora regular ou como um valor de intervalo (em que o intervalo começa quando a invocação do método é recebida).</span><span class="sxs-lookup"><span data-stu-id="fab9b-131">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="fab9b-132">Quando o parâmetro *PowerState* é igual a 5 ("ciclo de energia"), o parâmetro *time* indica quando o dispositivo deve ligar novamente.</span><span class="sxs-lookup"><span data-stu-id="fab9b-132">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="fab9b-133">A desligamento é imediata.</span><span class="sxs-lookup"><span data-stu-id="fab9b-133">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fab9b-134">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fab9b-134">Return value</span></span>

<span data-ttu-id="fab9b-135">Retornará 0 (zero) se for bem-sucedido, 1 (um) se o *PowerState* e a solicitação de *tempo* especificados não forem suportados e outro valor se ocorrer algum outro erro.</span><span class="sxs-lookup"><span data-stu-id="fab9b-135">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="fab9b-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="fab9b-136">Remarks</span></span>

<span data-ttu-id="fab9b-137">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="fab9b-137">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="fab9b-138">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="fab9b-138">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="fab9b-139">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="fab9b-139">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="fab9b-140">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="fab9b-140">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="fab9b-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fab9b-141">Requirements</span></span>



| <span data-ttu-id="fab9b-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="fab9b-142">Requirement</span></span> | <span data-ttu-id="fab9b-143">Valor</span><span class="sxs-lookup"><span data-stu-id="fab9b-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fab9b-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fab9b-144">Minimum supported client</span></span><br/> | <span data-ttu-id="fab9b-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fab9b-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fab9b-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fab9b-146">Minimum supported server</span></span><br/> | <span data-ttu-id="fab9b-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fab9b-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fab9b-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="fab9b-148">Namespace</span></span><br/>                | <span data-ttu-id="fab9b-149">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="fab9b-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fab9b-150">MOF</span><span class="sxs-lookup"><span data-stu-id="fab9b-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fab9b-151"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fab9b-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fab9b-152">DLL</span><span class="sxs-lookup"><span data-stu-id="fab9b-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fab9b-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fab9b-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fab9b-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="fab9b-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fab9b-155">\_UNITARYCOMPUTERSYSTEM CIM</span><span class="sxs-lookup"><span data-stu-id="fab9b-155">CIM\_UnitaryComputerSystem</span></span>](setpowerstate-method-in-class-cim-unitarycomputersystem.md)
</dt> <dt>

[<span data-ttu-id="fab9b-156">**\_UNITARYCOMPUTERSYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="fab9b-156">**CIM\_UnitaryComputerSystem**</span></span>](cim-unitarycomputersystem.md)
</dt> </dl>

 

 




