---
description: O método SetPowerState da classe de \_ exibição CIM define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.
ms.assetid: 949c300c-b01b-4c91-a902-41e940667ee6
ms.tgt_platform: multiple
title: Método SetPowerState da classe CIM_Display
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Display.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 35bcf49419b934e98c63b2151dcdaf3cb55f8d97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089085"
---
# <a name="setpowerstate-method-of-the-cim_display-class"></a><span data-ttu-id="f1318-103">Método SetPowerState da classe de \_ exibição CIM</span><span class="sxs-lookup"><span data-stu-id="f1318-103">SetPowerState method of the CIM\_Display class</span></span>

<span data-ttu-id="f1318-104">O método **SetPowerState** da classe de \_ exibição CIM define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="f1318-104">The **SetPowerState** method of the CIM\_Display class sets the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="f1318-105">Em uma subclasse, o conjunto de códigos de retorno possíveis deve ser especificado usando um qualificador **ValueMap** no método.</span><span class="sxs-lookup"><span data-stu-id="f1318-105">In a subclass, the set of possible return codes should be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="f1318-106">As cadeias de caracteres nas quais o conteúdo de **ValueMap** são traduzidos também devem ser especificadas na subclasse como um qualificador de matriz de **valores** .</span><span class="sxs-lookup"><span data-stu-id="f1318-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f1318-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="f1318-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f1318-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f1318-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="f1318-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f1318-109">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="f1318-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f1318-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1318-111">*PowerState* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f1318-111">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1318-112">Um valor de **ValueMap** que especifica o estado de energia desejado para esse dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="f1318-112">A **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span data-ttu-id="f1318-113">1</span><span class="sxs-lookup"><span data-stu-id="f1318-113">1</span></span>
</dt> <dd>

<span data-ttu-id="f1318-114">Potência total.</span><span class="sxs-lookup"><span data-stu-id="f1318-114">Full power.</span></span>

</dd> <dt>

<span data-ttu-id="f1318-115">2</span><span class="sxs-lookup"><span data-stu-id="f1318-115">2</span></span>
</dt> <dd>

<span data-ttu-id="f1318-116">Economia de energia no modo de baixa energia.</span><span class="sxs-lookup"><span data-stu-id="f1318-116">Power save   low-power mode.</span></span>

</dd> <dt>

<span data-ttu-id="f1318-117">3</span><span class="sxs-lookup"><span data-stu-id="f1318-117">3</span></span>
</dt> <dd>

<span data-ttu-id="f1318-118">Power Save em espera.</span><span class="sxs-lookup"><span data-stu-id="f1318-118">Power save   standby.</span></span>

</dd> <dt>

<span data-ttu-id="f1318-119">4</span><span class="sxs-lookup"><span data-stu-id="f1318-119">4</span></span>
</dt> <dd>

<span data-ttu-id="f1318-120">Economia de energia diferente.</span><span class="sxs-lookup"><span data-stu-id="f1318-120">Power save   other.</span></span>

</dd> <dt>

<span data-ttu-id="f1318-121">5</span><span class="sxs-lookup"><span data-stu-id="f1318-121">5</span></span>
</dt> <dd>

<span data-ttu-id="f1318-122">Ciclo de energia.</span><span class="sxs-lookup"><span data-stu-id="f1318-122">Power cycle.</span></span>

</dd> <dt>

<span data-ttu-id="f1318-123">6</span><span class="sxs-lookup"><span data-stu-id="f1318-123">6</span></span>
</dt> <dd>

<span data-ttu-id="f1318-124">Desligar.</span><span class="sxs-lookup"><span data-stu-id="f1318-124">Power off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f1318-125">*Tempo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f1318-125">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1318-126">Especifica quando o estado de energia deve ser definido, seja como um valor de data/hora regular ou como um valor de intervalo (em que o intervalo começa quando a invocação do método é recebida).</span><span class="sxs-lookup"><span data-stu-id="f1318-126">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="f1318-127">Quando o parâmetro *PowerState* é igual a 5 ("ciclo de energia"), o parâmetro *time* indica quando o dispositivo deve ligar novamente.</span><span class="sxs-lookup"><span data-stu-id="f1318-127">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="f1318-128">A desligamento é imediata.</span><span class="sxs-lookup"><span data-stu-id="f1318-128">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1318-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f1318-129">Return value</span></span>

<span data-ttu-id="f1318-130">Retornará 0 (zero) se for bem-sucedido, 1 (um) se o *PowerState* e a solicitação de *tempo* especificados não forem suportados e outro valor se ocorrer algum outro erro.</span><span class="sxs-lookup"><span data-stu-id="f1318-130">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1318-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="f1318-131">Remarks</span></span>

<span data-ttu-id="f1318-132">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="f1318-132">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="f1318-133">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="f1318-133">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="f1318-134">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="f1318-134">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f1318-135">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="f1318-135">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1318-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1318-136">Requirements</span></span>



| <span data-ttu-id="f1318-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1318-137">Requirement</span></span> | <span data-ttu-id="f1318-138">Valor</span><span class="sxs-lookup"><span data-stu-id="f1318-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1318-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1318-139">Minimum supported client</span></span><br/> | <span data-ttu-id="f1318-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f1318-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f1318-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1318-141">Minimum supported server</span></span><br/> | <span data-ttu-id="f1318-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f1318-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f1318-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="f1318-143">Namespace</span></span><br/>                | <span data-ttu-id="f1318-144">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f1318-144">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f1318-145">MOF</span><span class="sxs-lookup"><span data-stu-id="f1318-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1318-146"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f1318-146"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f1318-147">DLL</span><span class="sxs-lookup"><span data-stu-id="f1318-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1318-148"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1318-148"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1318-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="f1318-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1318-150">Exibição de CIM \_</span><span class="sxs-lookup"><span data-stu-id="f1318-150">CIM\_Display</span></span>](setpowerstate-method-in-class-cim-display.md)
</dt> <dt>

[<span data-ttu-id="f1318-151">**Exibição de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="f1318-151">**CIM\_Display**</span></span>](cim-display.md)
</dt> </dl>

 

 




