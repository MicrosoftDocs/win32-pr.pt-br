---
description: O método SetPowerState da classe de \_ processador CIM define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.
ms.assetid: 562c49c5-b349-402a-a3f0-2d7785a2c1ae
ms.tgt_platform: multiple
title: Método SetPowerState da classe CIM_Processor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Processor.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3622d96844bc90dc7e8a7bdcdd5e8805855944dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920596"
---
# <a name="setpowerstate-method-of-the-cim_processor-class"></a><span data-ttu-id="ee6e6-103">Método SetPowerState da classe de \_ processador CIM</span><span class="sxs-lookup"><span data-stu-id="ee6e6-103">SetPowerState method of the CIM\_Processor class</span></span>

<span data-ttu-id="ee6e6-104">O método **SetPowerState** da classe de \_ processador CIM define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="ee6e6-104">The **SetPowerState** method of the CIM\_Processor class sets the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="ee6e6-105">Em uma subclasse, o conjunto de códigos de retorno possíveis deve ser especificado usando um qualificador **ValueMap** no método.</span><span class="sxs-lookup"><span data-stu-id="ee6e6-105">In a subclass, the set of possible return codes should be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="ee6e6-106">As cadeias de caracteres nas quais o conteúdo de **ValueMap** são traduzidos também devem ser especificadas na subclasse como um qualificador de matriz de **valores** .</span><span class="sxs-lookup"><span data-stu-id="ee6e6-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="ee6e6-107">Esse método é herdado [**do \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ee6e6-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ee6e6-108">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="ee6e6-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ee6e6-109">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ee6e6-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="ee6e6-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ee6e6-110">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="ee6e6-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ee6e6-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee6e6-112">*PowerState* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ee6e6-112">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee6e6-113">Um valor de **ValueMap** que especifica o estado de energia desejado para esse dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="ee6e6-113">A **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span data-ttu-id="ee6e6-114">1</span><span class="sxs-lookup"><span data-stu-id="ee6e6-114">1</span></span>
</dt> <dd>

<span data-ttu-id="ee6e6-115">Potência total.</span><span class="sxs-lookup"><span data-stu-id="ee6e6-115">Full power.</span></span>

</dd> <dt>

<span data-ttu-id="ee6e6-116">2</span><span class="sxs-lookup"><span data-stu-id="ee6e6-116">2</span></span>
</dt> <dd>

<span data-ttu-id="ee6e6-117">Economia de energia no modo de baixa energia.</span><span class="sxs-lookup"><span data-stu-id="ee6e6-117">Power save   low-power mode.</span></span>

</dd> <dt>

<span data-ttu-id="ee6e6-118">3</span><span class="sxs-lookup"><span data-stu-id="ee6e6-118">3</span></span>
</dt> <dd>

<span data-ttu-id="ee6e6-119">Power Save em espera.</span><span class="sxs-lookup"><span data-stu-id="ee6e6-119">Power save   standby.</span></span>

</dd> <dt>

<span data-ttu-id="ee6e6-120">4</span><span class="sxs-lookup"><span data-stu-id="ee6e6-120">4</span></span>
</dt> <dd>

<span data-ttu-id="ee6e6-121">Economia de energia diferente.</span><span class="sxs-lookup"><span data-stu-id="ee6e6-121">Power save   other.</span></span>

</dd> <dt>

<span data-ttu-id="ee6e6-122">5</span><span class="sxs-lookup"><span data-stu-id="ee6e6-122">5</span></span>
</dt> <dd>

<span data-ttu-id="ee6e6-123">Ciclo de energia.</span><span class="sxs-lookup"><span data-stu-id="ee6e6-123">Power cycle.</span></span>

</dd> <dt>

<span data-ttu-id="ee6e6-124">6</span><span class="sxs-lookup"><span data-stu-id="ee6e6-124">6</span></span>
</dt> <dd>

<span data-ttu-id="ee6e6-125">Desligar.</span><span class="sxs-lookup"><span data-stu-id="ee6e6-125">Power off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ee6e6-126">*Tempo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ee6e6-126">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee6e6-127">Especifica quando o estado de energia deve ser definido, seja como um valor de data/hora regular ou como um valor de intervalo (em que o intervalo começa quando a invocação do método é recebida).</span><span class="sxs-lookup"><span data-stu-id="ee6e6-127">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="ee6e6-128">Quando o parâmetro *PowerState* é igual a 5 ("ciclo de energia"), o parâmetro *time* indica quando o dispositivo deve ligar novamente.</span><span class="sxs-lookup"><span data-stu-id="ee6e6-128">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="ee6e6-129">A desligamento é imediata.</span><span class="sxs-lookup"><span data-stu-id="ee6e6-129">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee6e6-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ee6e6-130">Return value</span></span>

<span data-ttu-id="ee6e6-131">Retornará 0 (zero) se for bem-sucedido, 1 (um) se o *PowerState* e a solicitação de *tempo* especificados não forem suportados e outro valor se ocorrer algum outro erro.</span><span class="sxs-lookup"><span data-stu-id="ee6e6-131">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee6e6-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee6e6-132">Remarks</span></span>

<span data-ttu-id="ee6e6-133">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="ee6e6-133">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="ee6e6-134">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="ee6e6-134">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="ee6e6-135">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="ee6e6-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ee6e6-136">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="ee6e6-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee6e6-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee6e6-137">Requirements</span></span>



| <span data-ttu-id="ee6e6-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee6e6-138">Requirement</span></span> | <span data-ttu-id="ee6e6-139">Valor</span><span class="sxs-lookup"><span data-stu-id="ee6e6-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee6e6-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee6e6-140">Minimum supported client</span></span><br/> | <span data-ttu-id="ee6e6-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ee6e6-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ee6e6-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee6e6-142">Minimum supported server</span></span><br/> | <span data-ttu-id="ee6e6-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ee6e6-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ee6e6-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="ee6e6-144">Namespace</span></span><br/>                | <span data-ttu-id="ee6e6-145">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="ee6e6-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ee6e6-146">MOF</span><span class="sxs-lookup"><span data-stu-id="ee6e6-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ee6e6-147"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ee6e6-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ee6e6-148">DLL</span><span class="sxs-lookup"><span data-stu-id="ee6e6-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee6e6-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee6e6-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee6e6-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee6e6-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee6e6-151">\_Processador CIM</span><span class="sxs-lookup"><span data-stu-id="ee6e6-151">CIM\_Processor</span></span>](setpowerstate-method-in-class-cim-processor.md)
</dt> <dt>

[<span data-ttu-id="ee6e6-152">**\_Processador CIM**</span><span class="sxs-lookup"><span data-stu-id="ee6e6-152">**CIM\_Processor**</span></span>](cim-processor.md)
</dt> </dl>

 

 




