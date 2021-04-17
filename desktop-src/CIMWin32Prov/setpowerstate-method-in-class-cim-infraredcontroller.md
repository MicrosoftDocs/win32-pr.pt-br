---
description: O método SetPowerState da classe CIM \_ InfraredController define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.
ms.assetid: dce688f3-b7c2-4e43-a26f-7318ce0011b8
ms.tgt_platform: multiple
title: Método SetPowerState da classe CIM_InfraredController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_InfraredController.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1730071111d1ebf86af229236826647626ca8f71
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753975"
---
# <a name="setpowerstate-method-of-the-cim_infraredcontroller-class"></a><span data-ttu-id="686a0-103">Método SetPowerState da classe CIM \_ InfraredController</span><span class="sxs-lookup"><span data-stu-id="686a0-103">SetPowerState method of the CIM\_InfraredController class</span></span>

<span data-ttu-id="686a0-104">O método **SetPowerState** da classe CIM \_ InfraredController define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="686a0-104">The **SetPowerState** method of the CIM\_InfraredController class sets the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="686a0-105">Em uma subclasse, o conjunto de códigos de retorno possíveis deve ser especificado usando um qualificador **ValueMap** no método.</span><span class="sxs-lookup"><span data-stu-id="686a0-105">In a subclass, the set of possible return codes should be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="686a0-106">As cadeias de caracteres nas quais o conteúdo de **ValueMap** são traduzidos também devem ser especificadas na subclasse como um qualificador de matriz de **valores** .</span><span class="sxs-lookup"><span data-stu-id="686a0-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="686a0-107">Esse método é herdado [**do \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="686a0-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="686a0-108">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="686a0-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="686a0-109">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="686a0-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="686a0-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="686a0-110">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="686a0-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="686a0-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="686a0-112">*PowerState* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="686a0-112">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="686a0-113">Um valor de **ValueMap** que especifica o estado de energia desejado para o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="686a0-113">A **ValueMap** value that specifies the desired power state for the logical device.</span></span>

<dt>

<span data-ttu-id="686a0-114">1</span><span class="sxs-lookup"><span data-stu-id="686a0-114">1</span></span>
</dt> <dd>

<span data-ttu-id="686a0-115">Potência total.</span><span class="sxs-lookup"><span data-stu-id="686a0-115">Full power.</span></span>

</dd> <dt>

<span data-ttu-id="686a0-116">2</span><span class="sxs-lookup"><span data-stu-id="686a0-116">2</span></span>
</dt> <dd>

<span data-ttu-id="686a0-117">Economia de energia no modo de baixa energia.</span><span class="sxs-lookup"><span data-stu-id="686a0-117">Power save   low-power mode.</span></span>

</dd> <dt>

<span data-ttu-id="686a0-118">3</span><span class="sxs-lookup"><span data-stu-id="686a0-118">3</span></span>
</dt> <dd>

<span data-ttu-id="686a0-119">Power Save em espera.</span><span class="sxs-lookup"><span data-stu-id="686a0-119">Power save   standby.</span></span>

</dd> <dt>

<span data-ttu-id="686a0-120">4</span><span class="sxs-lookup"><span data-stu-id="686a0-120">4</span></span>
</dt> <dd>

<span data-ttu-id="686a0-121">Economia de energia diferente.</span><span class="sxs-lookup"><span data-stu-id="686a0-121">Power save   other.</span></span>

</dd> <dt>

<span data-ttu-id="686a0-122">5</span><span class="sxs-lookup"><span data-stu-id="686a0-122">5</span></span>
</dt> <dd>

<span data-ttu-id="686a0-123">Ciclo de energia.</span><span class="sxs-lookup"><span data-stu-id="686a0-123">Power cycle.</span></span>

</dd> <dt>

<span data-ttu-id="686a0-124">6</span><span class="sxs-lookup"><span data-stu-id="686a0-124">6</span></span>
</dt> <dd>

<span data-ttu-id="686a0-125">Desligar.</span><span class="sxs-lookup"><span data-stu-id="686a0-125">Power off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="686a0-126">*Tempo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="686a0-126">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="686a0-127">Especifica quando o estado de energia deve ser definido, seja como um valor de data/hora regular ou como um valor de intervalo (em que o intervalo começa quando a invocação do método é recebida).</span><span class="sxs-lookup"><span data-stu-id="686a0-127">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="686a0-128">Quando o parâmetro *PowerState* é igual a 5 ("ciclo de energia"), o parâmetro *time* indica quando o dispositivo deve ligar novamente.</span><span class="sxs-lookup"><span data-stu-id="686a0-128">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="686a0-129">A desligamento é imediata.</span><span class="sxs-lookup"><span data-stu-id="686a0-129">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="686a0-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="686a0-130">Return value</span></span>

<span data-ttu-id="686a0-131">Retornará 0 (zero) se for bem-sucedido, 1 (um) se o *PowerState* e a solicitação de *tempo* especificados não forem suportados e outro valor se ocorrer algum outro erro.</span><span class="sxs-lookup"><span data-stu-id="686a0-131">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="686a0-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="686a0-132">Remarks</span></span>

<span data-ttu-id="686a0-133">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="686a0-133">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="686a0-134">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="686a0-134">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="686a0-135">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="686a0-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="686a0-136">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="686a0-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="686a0-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="686a0-137">Requirements</span></span>



| <span data-ttu-id="686a0-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="686a0-138">Requirement</span></span> | <span data-ttu-id="686a0-139">Valor</span><span class="sxs-lookup"><span data-stu-id="686a0-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="686a0-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="686a0-140">Minimum supported client</span></span><br/> | <span data-ttu-id="686a0-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="686a0-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="686a0-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="686a0-142">Minimum supported server</span></span><br/> | <span data-ttu-id="686a0-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="686a0-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="686a0-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="686a0-144">Namespace</span></span><br/>                | <span data-ttu-id="686a0-145">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="686a0-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="686a0-146">MOF</span><span class="sxs-lookup"><span data-stu-id="686a0-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="686a0-147"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="686a0-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="686a0-148">DLL</span><span class="sxs-lookup"><span data-stu-id="686a0-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="686a0-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="686a0-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="686a0-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="686a0-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="686a0-151">\_INFRAREDCONTROLLER CIM</span><span class="sxs-lookup"><span data-stu-id="686a0-151">CIM\_InfraredController</span></span>](setpowerstate-method-in-class-cim-infraredcontroller.md)
</dt> <dt>

[<span data-ttu-id="686a0-152">**\_INFRAREDCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="686a0-152">**CIM\_InfraredController**</span></span>](cim-infraredcontroller.md)
</dt> </dl>

 

 




