---
description: O método SetPowerState da classe CIM \_ LogicalDevice define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.
ms.assetid: 0d9678e0-a956-45d3-ac41-5c1604478fd7
ms.tgt_platform: multiple
title: Método SetPowerState da classe CIM_LogicalDevice (provedores WMI CIMWin32)
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
- CIMWin32.dll
ms.openlocfilehash: dd258a4372c16a7f98f2fe3ea8b84bbfef44f69e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749314"
---
# <a name="setpowerstate-method-of-the-cim_logicaldevice-class-cimwin32-wmi-providers"></a><span data-ttu-id="37444-103">Método SetPowerState da classe CIM_LogicalDevice (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="37444-103">SetPowerState method of the CIM_LogicalDevice class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="37444-104">O método **SetPowerState** da classe CIM \_ LogicalDevice define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="37444-104">The **SetPowerState** method of the CIM\_LogicalDevice class sets the desired power state for a logical device and when a device should be put into that state.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="37444-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="37444-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="37444-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="37444-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="37444-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="37444-107">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="37444-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="37444-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37444-109">*PowerState* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="37444-109">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37444-110">Um valor de **ValueMap** que especifica o estado de energia desejado para esse dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="37444-110">A **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span data-ttu-id="37444-111"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Energia completa** (1)</span><span class="sxs-lookup"><span data-stu-id="37444-111"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Full Power** (1)</span></span>


</dt> <dd>

<span data-ttu-id="37444-112">Potência total.</span><span class="sxs-lookup"><span data-stu-id="37444-112">Full power.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="37444-113"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (2)</span><span class="sxs-lookup"><span data-stu-id="37444-113"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (2)</span></span>


</dt> <dd>

<span data-ttu-id="37444-114">Economia de energia no modo de baixa energia.</span><span class="sxs-lookup"><span data-stu-id="37444-114">Power save   low-power mode.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="37444-115"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (3)</span><span class="sxs-lookup"><span data-stu-id="37444-115"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (3)</span></span>


</dt> <dd>

<span data-ttu-id="37444-116">Power Save em espera.</span><span class="sxs-lookup"><span data-stu-id="37444-116">Power save   standby.</span></span>

</dd> <dt>

<span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>

<span data-ttu-id="37444-117"><span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>Economia **de energia-outro** (4)</span><span class="sxs-lookup"><span data-stu-id="37444-117"><span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>**Power Save - Other** (4)</span></span>


</dt> <dd>

<span data-ttu-id="37444-118">Economia de energia diferente.</span><span class="sxs-lookup"><span data-stu-id="37444-118">Power save   other.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="37444-119"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (5)</span><span class="sxs-lookup"><span data-stu-id="37444-119"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (5)</span></span>


</dt> <dd>

<span data-ttu-id="37444-120">Ciclo de energia.</span><span class="sxs-lookup"><span data-stu-id="37444-120">Power cycle.</span></span>

</dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="37444-121"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (6** )</span><span class="sxs-lookup"><span data-stu-id="37444-121"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (6)</span></span>


</dt> <dd>

<span data-ttu-id="37444-122">Desligar.</span><span class="sxs-lookup"><span data-stu-id="37444-122">Power off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="37444-123">*Tempo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="37444-123">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37444-124">Especifica quando o estado de energia deve ser definido, seja como um valor de data/hora regular ou como um valor de intervalo (em que o intervalo começa quando a invocação do método é recebida).</span><span class="sxs-lookup"><span data-stu-id="37444-124">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="37444-125">Quando o parâmetro *PowerState* é igual a 5 ("ciclo de energia"), o parâmetro *time* indica quando o dispositivo deve ligar novamente.</span><span class="sxs-lookup"><span data-stu-id="37444-125">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="37444-126">A desligamento é imediata.</span><span class="sxs-lookup"><span data-stu-id="37444-126">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37444-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="37444-127">Return value</span></span>

<span data-ttu-id="37444-128">Retornará 0 (zero) se for bem-sucedido, 1 (um) se o *PowerState* e a solicitação de *tempo* especificados não forem suportados e outro valor se ocorrer algum outro erro.</span><span class="sxs-lookup"><span data-stu-id="37444-128">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="37444-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="37444-129">Remarks</span></span>

<span data-ttu-id="37444-130">Em uma subclasse, o conjunto de códigos de retorno possíveis deve ser especificado usando um qualificador **ValueMap** no método.</span><span class="sxs-lookup"><span data-stu-id="37444-130">In a subclass, the set of possible return codes should be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="37444-131">As cadeias de caracteres nas quais o conteúdo de **ValueMap** são traduzidos também devem ser especificadas na subclasse como um qualificador de matriz de **valores** .</span><span class="sxs-lookup"><span data-stu-id="37444-131">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="37444-132">Esse método é herdado [**do \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="37444-132">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="37444-133">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="37444-133">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="37444-134">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="37444-134">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="37444-135">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="37444-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="37444-136">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="37444-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="37444-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37444-137">Requirements</span></span>



| <span data-ttu-id="37444-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="37444-138">Requirement</span></span> | <span data-ttu-id="37444-139">Valor</span><span class="sxs-lookup"><span data-stu-id="37444-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="37444-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="37444-140">Minimum supported client</span></span><br/> | <span data-ttu-id="37444-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="37444-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="37444-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="37444-142">Minimum supported server</span></span><br/> | <span data-ttu-id="37444-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="37444-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="37444-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="37444-144">Namespace</span></span><br/>                | <span data-ttu-id="37444-145">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="37444-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="37444-146">MOF</span><span class="sxs-lookup"><span data-stu-id="37444-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37444-147"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="37444-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="37444-148">DLL</span><span class="sxs-lookup"><span data-stu-id="37444-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37444-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37444-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37444-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="37444-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37444-151">\_LOGICALDEVICE CIM</span><span class="sxs-lookup"><span data-stu-id="37444-151">CIM\_LogicalDevice</span></span>](setpowerstate-method-in-class-cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="37444-152">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="37444-152">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




