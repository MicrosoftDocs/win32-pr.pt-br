---
description: O método SetPowerState da classe CIM \_ DiskPartition define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.
ms.assetid: cfc68ad3-819c-438f-baca-bed6e2592369
ms.tgt_platform: multiple
title: Método SetPowerState da classe CIM_DiskPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DiskPartition.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a8316dbf0bc0c6aa438b2881c691cde6976501c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752958"
---
# <a name="setpowerstate-method-of-the-cim_diskpartition-class"></a><span data-ttu-id="5b0db-103">Método SetPowerState da classe CIM \_ DiskPartition</span><span class="sxs-lookup"><span data-stu-id="5b0db-103">SetPowerState method of the CIM\_DiskPartition class</span></span>

<span data-ttu-id="5b0db-104">O método **SetPowerState** da classe CIM \_ DiskPartition define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="5b0db-104">The **SetPowerState** method of the CIM\_DiskPartition class sets the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="5b0db-105">Em uma subclasse, o conjunto de códigos de retorno possíveis deve ser especificado usando um qualificador **ValueMap** no método.</span><span class="sxs-lookup"><span data-stu-id="5b0db-105">In a subclass, the set of possible return codes should be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="5b0db-106">As cadeias de caracteres nas quais o conteúdo de **ValueMap** são traduzidos também devem ser especificadas na subclasse como um qualificador de matriz de **valores** .</span><span class="sxs-lookup"><span data-stu-id="5b0db-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5b0db-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="5b0db-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5b0db-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5b0db-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="5b0db-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5b0db-109">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="5b0db-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5b0db-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b0db-111">*PowerState* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5b0db-111">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b0db-112">Um valor de **ValueMap** que especifica o estado de energia desejado para esse dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5b0db-112">A **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span data-ttu-id="5b0db-113">1</span><span class="sxs-lookup"><span data-stu-id="5b0db-113">1</span></span>
</dt> <dd>

<span data-ttu-id="5b0db-114">Potência total.</span><span class="sxs-lookup"><span data-stu-id="5b0db-114">Full power.</span></span>

</dd> <dt>

<span data-ttu-id="5b0db-115">2</span><span class="sxs-lookup"><span data-stu-id="5b0db-115">2</span></span>
</dt> <dd>

<span data-ttu-id="5b0db-116">Economia de energia no modo de baixa energia.</span><span class="sxs-lookup"><span data-stu-id="5b0db-116">Power save   low-power mode.</span></span>

</dd> <dt>

<span data-ttu-id="5b0db-117">3</span><span class="sxs-lookup"><span data-stu-id="5b0db-117">3</span></span>
</dt> <dd>

<span data-ttu-id="5b0db-118">Power Save em espera.</span><span class="sxs-lookup"><span data-stu-id="5b0db-118">Power save   standby.</span></span>

</dd> <dt>

<span data-ttu-id="5b0db-119">4</span><span class="sxs-lookup"><span data-stu-id="5b0db-119">4</span></span>
</dt> <dd>

<span data-ttu-id="5b0db-120">Economia de energia diferente.</span><span class="sxs-lookup"><span data-stu-id="5b0db-120">Power save   other.</span></span>

</dd> <dt>

<span data-ttu-id="5b0db-121">5</span><span class="sxs-lookup"><span data-stu-id="5b0db-121">5</span></span>
</dt> <dd>

<span data-ttu-id="5b0db-122">Ciclo de energia.</span><span class="sxs-lookup"><span data-stu-id="5b0db-122">Power cycle.</span></span>

</dd> <dt>

<span data-ttu-id="5b0db-123">6</span><span class="sxs-lookup"><span data-stu-id="5b0db-123">6</span></span>
</dt> <dd>

<span data-ttu-id="5b0db-124">Desligar.</span><span class="sxs-lookup"><span data-stu-id="5b0db-124">Power off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="5b0db-125">*Tempo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5b0db-125">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b0db-126">Especifica quando o estado de energia deve ser definido, seja como um valor de data/hora regular ou como um valor de intervalo (em que o intervalo começa quando a invocação do método é recebida).</span><span class="sxs-lookup"><span data-stu-id="5b0db-126">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="5b0db-127">Quando o parâmetro *PowerState* é igual a 5 ("ciclo de energia"), o parâmetro *time* indica quando o dispositivo deve ligar novamente.</span><span class="sxs-lookup"><span data-stu-id="5b0db-127">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="5b0db-128">A desligamento é imediata.</span><span class="sxs-lookup"><span data-stu-id="5b0db-128">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b0db-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5b0db-129">Return value</span></span>

<span data-ttu-id="5b0db-130">Retornará 0 (zero) se for bem-sucedido, 1 (um) se o *PowerState* e a solicitação de *tempo* especificados não forem suportados e outro valor se ocorrer algum outro erro.</span><span class="sxs-lookup"><span data-stu-id="5b0db-130">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b0db-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="5b0db-131">Remarks</span></span>

<span data-ttu-id="5b0db-132">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="5b0db-132">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="5b0db-133">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="5b0db-133">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="5b0db-134">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="5b0db-134">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5b0db-135">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="5b0db-135">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b0db-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b0db-136">Requirements</span></span>



| <span data-ttu-id="5b0db-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b0db-137">Requirement</span></span> | <span data-ttu-id="5b0db-138">Valor</span><span class="sxs-lookup"><span data-stu-id="5b0db-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b0db-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b0db-139">Minimum supported client</span></span><br/> | <span data-ttu-id="5b0db-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5b0db-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5b0db-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b0db-141">Minimum supported server</span></span><br/> | <span data-ttu-id="5b0db-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5b0db-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5b0db-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="5b0db-143">Namespace</span></span><br/>                | <span data-ttu-id="5b0db-144">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5b0db-144">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5b0db-145">MOF</span><span class="sxs-lookup"><span data-stu-id="5b0db-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5b0db-146"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5b0db-146"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5b0db-147">DLL</span><span class="sxs-lookup"><span data-stu-id="5b0db-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b0db-148"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b0db-148"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b0db-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b0db-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b0db-150">\_DISKPARTITION CIM</span><span class="sxs-lookup"><span data-stu-id="5b0db-150">CIM\_DiskPartition</span></span>](setpowerstate-method-in-class-cim-diskpartition.md)
</dt> <dt>

[<span data-ttu-id="5b0db-151">**\_DISKPARTITION CIM**</span><span class="sxs-lookup"><span data-stu-id="5b0db-151">**CIM\_DiskPartition**</span></span>](cim-diskpartition.md)
</dt> </dl>

 

 




