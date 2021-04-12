---
description: O método SetPowerState da classe CIM \_ TapeDrive define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.
ms.assetid: 73f98d08-49da-4b21-91c4-cbe420c648e4
ms.tgt_platform: multiple
title: Método SetPowerState da classe CIM_TapeDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TapeDrive.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a6efcfe08dfddca3477081f65fac35780f713005
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501075"
---
# <a name="setpowerstate-method-of-the-cim_tapedrive-class"></a><span data-ttu-id="d0f1f-103">Método SetPowerState da classe CIM \_ TapeDrive</span><span class="sxs-lookup"><span data-stu-id="d0f1f-103">SetPowerState method of the CIM\_TapeDrive class</span></span>

<span data-ttu-id="d0f1f-104">O método **SetPowerState** da classe CIM \_ TapeDrive define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="d0f1f-104">The **SetPowerState** method of the CIM\_TapeDrive class sets the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="d0f1f-105">Em uma subclasse, o conjunto de códigos de retorno possíveis deve ser especificado usando um qualificador **ValueMap** no método.</span><span class="sxs-lookup"><span data-stu-id="d0f1f-105">In a subclass, the set of possible return codes should be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="d0f1f-106">As cadeias de caracteres nas quais o conteúdo de **ValueMap** são traduzidos também devem ser especificadas na subclasse como um qualificador de matriz de **valores** .</span><span class="sxs-lookup"><span data-stu-id="d0f1f-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="d0f1f-107">Esse método é herdado [**do \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d0f1f-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d0f1f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d0f1f-108">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="d0f1f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d0f1f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0f1f-110">*PowerState* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d0f1f-110">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0f1f-111">Um valor de **ValueMap** que especifica o estado de energia desejado para esse dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d0f1f-111">A **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span data-ttu-id="d0f1f-112">1</span><span class="sxs-lookup"><span data-stu-id="d0f1f-112">1</span></span>
</dt> <dd>

<span data-ttu-id="d0f1f-113">Potência total.</span><span class="sxs-lookup"><span data-stu-id="d0f1f-113">Full power.</span></span>

</dd> <dt>

<span data-ttu-id="d0f1f-114">2</span><span class="sxs-lookup"><span data-stu-id="d0f1f-114">2</span></span>
</dt> <dd>

<span data-ttu-id="d0f1f-115">Economia de energia no modo de baixa energia.</span><span class="sxs-lookup"><span data-stu-id="d0f1f-115">Power save   low-power mode.</span></span>

</dd> <dt>

<span data-ttu-id="d0f1f-116">3</span><span class="sxs-lookup"><span data-stu-id="d0f1f-116">3</span></span>
</dt> <dd>

<span data-ttu-id="d0f1f-117">Power Save em espera.</span><span class="sxs-lookup"><span data-stu-id="d0f1f-117">Power save   standby.</span></span>

</dd> <dt>

<span data-ttu-id="d0f1f-118">4</span><span class="sxs-lookup"><span data-stu-id="d0f1f-118">4</span></span>
</dt> <dd>

<span data-ttu-id="d0f1f-119">Economia de energia diferente.</span><span class="sxs-lookup"><span data-stu-id="d0f1f-119">Power save   other.</span></span>

</dd> <dt>

<span data-ttu-id="d0f1f-120">5</span><span class="sxs-lookup"><span data-stu-id="d0f1f-120">5</span></span>
</dt> <dd>

<span data-ttu-id="d0f1f-121">Ciclo de energia.</span><span class="sxs-lookup"><span data-stu-id="d0f1f-121">Power cycle.</span></span>

</dd> <dt>

<span data-ttu-id="d0f1f-122">6</span><span class="sxs-lookup"><span data-stu-id="d0f1f-122">6</span></span>
</dt> <dd>

<span data-ttu-id="d0f1f-123">Desligar.</span><span class="sxs-lookup"><span data-stu-id="d0f1f-123">Power off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d0f1f-124">*Tempo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d0f1f-124">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0f1f-125">Especifica quando o estado de energia deve ser definido, seja como um valor de data/hora regular ou como um valor de intervalo (em que o intervalo começa quando a invocação do método é recebida).</span><span class="sxs-lookup"><span data-stu-id="d0f1f-125">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="d0f1f-126">Quando o parâmetro *PowerState* é igual a 5 ("ciclo de energia"), o parâmetro *time* indica quando o dispositivo deve ligar novamente.</span><span class="sxs-lookup"><span data-stu-id="d0f1f-126">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="d0f1f-127">A desligamento é imediata.</span><span class="sxs-lookup"><span data-stu-id="d0f1f-127">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0f1f-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d0f1f-128">Return value</span></span>

<span data-ttu-id="d0f1f-129">Retornará 0 (zero) se for bem-sucedido, 1 (um) se o *PowerState* e a solicitação de *tempo* especificados não forem suportados e outro valor se ocorrer algum outro erro.</span><span class="sxs-lookup"><span data-stu-id="d0f1f-129">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0f1f-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="d0f1f-130">Remarks</span></span>

<span data-ttu-id="d0f1f-131">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="d0f1f-131">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="d0f1f-132">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="d0f1f-132">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="d0f1f-133">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="d0f1f-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d0f1f-134">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="d0f1f-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0f1f-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0f1f-135">Requirements</span></span>



| <span data-ttu-id="d0f1f-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0f1f-136">Requirement</span></span> | <span data-ttu-id="d0f1f-137">Valor</span><span class="sxs-lookup"><span data-stu-id="d0f1f-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0f1f-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d0f1f-138">Minimum supported client</span></span><br/> | <span data-ttu-id="d0f1f-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d0f1f-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d0f1f-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d0f1f-140">Minimum supported server</span></span><br/> | <span data-ttu-id="d0f1f-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d0f1f-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d0f1f-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="d0f1f-142">Namespace</span></span><br/>                | <span data-ttu-id="d0f1f-143">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d0f1f-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d0f1f-144">MOF</span><span class="sxs-lookup"><span data-stu-id="d0f1f-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d0f1f-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d0f1f-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d0f1f-146">DLL</span><span class="sxs-lookup"><span data-stu-id="d0f1f-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0f1f-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0f1f-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0f1f-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="d0f1f-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0f1f-149">\_TAPEDRIVE CIM</span><span class="sxs-lookup"><span data-stu-id="d0f1f-149">CIM\_TapeDrive</span></span>](setpowerstate-method-in-class-cim-tapedrive.md)
</dt> <dt>

[<span data-ttu-id="d0f1f-150">**\_TAPEDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="d0f1f-150">**CIM\_TapeDrive**</span></span>](cim-tapedrive.md)
</dt> </dl>

 

 




