---
description: O método SetPowerState define o estado de energia desejado para um dispositivo lógico e quando o dispositivo deve ser colocado nesse estado.
ms.assetid: 1a1a8d5e-d685-4b7e-99fb-61fa2e7bdafa
ms.tgt_platform: multiple
title: Método SetPowerState da classe CIM_AggregatePExtent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregatePExtent.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 47c97f30da1c8b6f2fe9a6032ef9be9ae87a7d6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920411"
---
# <a name="setpowerstate-method-of-the-cim_aggregatepextent-class"></a><span data-ttu-id="b14aa-103">Método SetPowerState da classe CIM \_ AggregatePExtent</span><span class="sxs-lookup"><span data-stu-id="b14aa-103">SetPowerState method of the CIM\_AggregatePExtent class</span></span>

<span data-ttu-id="b14aa-104">O método **SetPowerState** define o estado de energia desejado para um dispositivo lógico e quando o dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="b14aa-104">The **SetPowerState** method sets the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="b14aa-105">Em uma subclasse, o conjunto de códigos de retorno possíveis deve ser especificado usando um qualificador **ValueMap** no método.</span><span class="sxs-lookup"><span data-stu-id="b14aa-105">In a subclass, the set of possible return codes should be specified using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="b14aa-106">As cadeias de caracteres nas quais o conteúdo de **ValueMap** são traduzidos também devem ser especificadas na subclasse como um qualificador de matriz de **valores** .</span><span class="sxs-lookup"><span data-stu-id="b14aa-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="b14aa-107">Esse método é herdado [**do \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b14aa-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="b14aa-108">Para obter mais informações sobre como usar esse método com C/C++, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b14aa-108">For more information about using this method with C/C++, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b14aa-109">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="b14aa-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b14aa-110">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b14aa-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b14aa-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b14aa-111">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="b14aa-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b14aa-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b14aa-113">*PowerState* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b14aa-113">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b14aa-114">O valor de **ValueMap** que especifica o estado de energia desejado para esse dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b14aa-114">The **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span data-ttu-id="b14aa-115">1</span><span class="sxs-lookup"><span data-stu-id="b14aa-115">1</span></span>
</dt> <dd>

<span data-ttu-id="b14aa-116">Potência total</span><span class="sxs-lookup"><span data-stu-id="b14aa-116">Full power</span></span>

</dd> <dt>

<span data-ttu-id="b14aa-117">2</span><span class="sxs-lookup"><span data-stu-id="b14aa-117">2</span></span>
</dt> <dd>

<span data-ttu-id="b14aa-118">Economia de energia – modo de baixa energia</span><span class="sxs-lookup"><span data-stu-id="b14aa-118">Power-save   low-power mode</span></span>

</dd> <dt>

<span data-ttu-id="b14aa-119">3</span><span class="sxs-lookup"><span data-stu-id="b14aa-119">3</span></span>
</dt> <dd>

<span data-ttu-id="b14aa-120">Energia-salvar em espera</span><span class="sxs-lookup"><span data-stu-id="b14aa-120">Power-save   standby</span></span>

</dd> <dt>

<span data-ttu-id="b14aa-121">4</span><span class="sxs-lookup"><span data-stu-id="b14aa-121">4</span></span>
</dt> <dd>

<span data-ttu-id="b14aa-122">Salvar outra energia</span><span class="sxs-lookup"><span data-stu-id="b14aa-122">Power-save   other</span></span>

</dd> <dt>

<span data-ttu-id="b14aa-123">5</span><span class="sxs-lookup"><span data-stu-id="b14aa-123">5</span></span>
</dt> <dd>

<span data-ttu-id="b14aa-124">Ciclo de energia</span><span class="sxs-lookup"><span data-stu-id="b14aa-124">Power cycle</span></span>

</dd> <dt>

<span data-ttu-id="b14aa-125">6</span><span class="sxs-lookup"><span data-stu-id="b14aa-125">6</span></span>
</dt> <dd>

<span data-ttu-id="b14aa-126">Desligar</span><span class="sxs-lookup"><span data-stu-id="b14aa-126">Power off</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b14aa-127">*Tempo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b14aa-127">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b14aa-128">Quando o estado de energia deve ser definido, seja como um valor de data/hora regular ou como um valor de intervalo (em que o intervalo começa quando a invocação do método é recebida).</span><span class="sxs-lookup"><span data-stu-id="b14aa-128">When the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="b14aa-129">Quando o parâmetro *PowerState* é igual a 5 (ciclo de energia), o parâmetro *time* indica quando o dispositivo deve ligar novamente.</span><span class="sxs-lookup"><span data-stu-id="b14aa-129">When the *PowerState* parameter is equal to 5 (power cycle), the *Time* parameter indicates when the device should power-on again.</span></span> <span data-ttu-id="b14aa-130">A desligamento é imediata.</span><span class="sxs-lookup"><span data-stu-id="b14aa-130">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b14aa-131">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b14aa-131">Return value</span></span>

<span data-ttu-id="b14aa-132">Retornará 0 (zero) se for bem-sucedido, 1 (um) se o *PowerState* e a solicitação de *tempo* especificados não forem suportados e outro valor se ocorrer algum outro erro.</span><span class="sxs-lookup"><span data-stu-id="b14aa-132">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="b14aa-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="b14aa-133">Remarks</span></span>

<span data-ttu-id="b14aa-134">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="b14aa-134">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="b14aa-135">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="b14aa-135">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="b14aa-136">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="b14aa-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b14aa-137">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="b14aa-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b14aa-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b14aa-138">Requirements</span></span>



| <span data-ttu-id="b14aa-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="b14aa-139">Requirement</span></span> | <span data-ttu-id="b14aa-140">Valor</span><span class="sxs-lookup"><span data-stu-id="b14aa-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b14aa-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b14aa-141">Minimum supported client</span></span><br/> | <span data-ttu-id="b14aa-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b14aa-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b14aa-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b14aa-143">Minimum supported server</span></span><br/> | <span data-ttu-id="b14aa-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b14aa-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b14aa-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="b14aa-145">Namespace</span></span><br/>                | <span data-ttu-id="b14aa-146">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b14aa-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b14aa-147">MOF</span><span class="sxs-lookup"><span data-stu-id="b14aa-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b14aa-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b14aa-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b14aa-149">DLL</span><span class="sxs-lookup"><span data-stu-id="b14aa-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b14aa-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b14aa-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b14aa-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="b14aa-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b14aa-152">**\_AGGREGATEPEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="b14aa-152">**CIM\_AggregatePExtent**</span></span>](setpowerstate-method-in-class-cim-aggregatepextent.md)
</dt> <dt>

[<span data-ttu-id="b14aa-153">**\_AGGREGATEPEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="b14aa-153">**CIM\_AggregatePExtent**</span></span>](cim-aggregatepextent.md)
</dt> </dl>

 

