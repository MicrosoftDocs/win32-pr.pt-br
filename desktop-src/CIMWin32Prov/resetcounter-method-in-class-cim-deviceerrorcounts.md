---
description: O método ResetCounter redefine os contadores de erro e de aviso.
ms.assetid: 5bc6c939-cd97-40ca-a16c-5227e7f27c76
ms.tgt_platform: multiple
title: Método ResetCounter da classe CIM_DeviceErrorCounts
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceErrorCounts.ResetCounter
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 386547362f5a7aa52bddfbf9df3af01949aecbdd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826183"
---
# <a name="resetcounter-method-of-the-cim_deviceerrorcounts-class"></a><span data-ttu-id="edcc2-103">Método ResetCounter da \_ classe DEVICEERRORCOUNTS CIM</span><span class="sxs-lookup"><span data-stu-id="edcc2-103">ResetCounter method of the CIM\_DeviceErrorCounts class</span></span>

<span data-ttu-id="edcc2-104">O método **ResetCounter** redefine os contadores de erro e de aviso.</span><span class="sxs-lookup"><span data-stu-id="edcc2-104">The **ResetCounter** method resets the error and warning counters.</span></span> <span data-ttu-id="edcc2-105">Um método é usado para que a instrumentação do dispositivo lógico, que tabula os erros e avisos, também possa redefinir seu processamento e contadores internos.</span><span class="sxs-lookup"><span data-stu-id="edcc2-105">A method is used so that the logical device's instrumentation, which tabulates the errors and warnings, can also reset its internal processing and counters.</span></span> <span data-ttu-id="edcc2-106">Em uma subclasse, o conjunto de códigos de retorno possíveis pode ser especificado usando um qualificador **ValueMap** no método.</span><span class="sxs-lookup"><span data-stu-id="edcc2-106">In a subclass, the set of possible return codes can be specified using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="edcc2-107">As cadeias de caracteres nas quais os conteúdos de **ValueMap** são convertidos também podem ser especificadas na subclasse como um qualificador de matriz de **valores** .</span><span class="sxs-lookup"><span data-stu-id="edcc2-107">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="edcc2-108">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="edcc2-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="edcc2-109">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="edcc2-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="edcc2-110">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="edcc2-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="edcc2-111">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="edcc2-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="edcc2-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="edcc2-112">Syntax</span></span>


```mof
uint32 ResetCounter(
  [in] uint16 SelectedCounter
);
```



## <a name="parameters"></a><span data-ttu-id="edcc2-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="edcc2-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edcc2-114">*SelectedCounter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="edcc2-114">*SelectedCounter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edcc2-115">Contador de erros a ser redefinido.</span><span class="sxs-lookup"><span data-stu-id="edcc2-115">Error counter to reset.</span></span>

<dt>

<span id="All"></span><span id="all"></span><span id="ALL"></span>

<span data-ttu-id="edcc2-116">**Todos** (0)</span><span class="sxs-lookup"><span data-stu-id="edcc2-116">**All** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Indeterminate_Error_Counter"></span><span id="indeterminate_error_counter"></span><span id="INDETERMINATE_ERROR_COUNTER"></span>

<span data-ttu-id="edcc2-117">**Contador de erros indeterminado** (1)</span><span class="sxs-lookup"><span data-stu-id="edcc2-117">**Indeterminate Error Counter** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical_Error_Counter"></span><span id="critical_error_counter"></span><span id="CRITICAL_ERROR_COUNTER"></span>

<span data-ttu-id="edcc2-118">**Contador de erros crítico** (2)</span><span class="sxs-lookup"><span data-stu-id="edcc2-118">**Critical Error Counter** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Major_Error_Counter"></span><span id="major_error_counter"></span><span id="MAJOR_ERROR_COUNTER"></span>

<span data-ttu-id="edcc2-119">**Contador de erros principal** (3)</span><span class="sxs-lookup"><span data-stu-id="edcc2-119">**Major Error Counter** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Minor_Error_Counter"></span><span id="minor_error_counter"></span><span id="MINOR_ERROR_COUNTER"></span>

<span data-ttu-id="edcc2-120">**Contador de erros secundário** (4)</span><span class="sxs-lookup"><span data-stu-id="edcc2-120">**Minor Error Counter** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning_Counter"></span><span id="warning_counter"></span><span id="WARNING_COUNTER"></span>

<span data-ttu-id="edcc2-121">**Contador de aviso** (5)</span><span class="sxs-lookup"><span data-stu-id="edcc2-121">**Warning Counter** (5)</span></span>


<span data-ttu-id="edcc2-122"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="edcc2-122"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="edcc2-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="edcc2-123">Return value</span></span>

<span data-ttu-id="edcc2-124">Retornará 0 (zero) se for bem-sucedido, 1 (um) se não houver suporte e qualquer outro valor se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="edcc2-124">Returns 0 (zero) if successful, 1 (one) if not supported, and any other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="edcc2-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="edcc2-125">Remarks</span></span>

<span data-ttu-id="edcc2-126">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="edcc2-126">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="edcc2-127">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="edcc2-127">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="edcc2-128">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="edcc2-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="edcc2-129">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="edcc2-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="edcc2-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="edcc2-130">Requirements</span></span>



| <span data-ttu-id="edcc2-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="edcc2-131">Requirement</span></span> | <span data-ttu-id="edcc2-132">Valor</span><span class="sxs-lookup"><span data-stu-id="edcc2-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="edcc2-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="edcc2-133">Minimum supported client</span></span><br/> | <span data-ttu-id="edcc2-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="edcc2-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="edcc2-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="edcc2-135">Minimum supported server</span></span><br/> | <span data-ttu-id="edcc2-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="edcc2-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="edcc2-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="edcc2-137">Namespace</span></span><br/>                | <span data-ttu-id="edcc2-138">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="edcc2-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="edcc2-139">MOF</span><span class="sxs-lookup"><span data-stu-id="edcc2-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="edcc2-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="edcc2-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="edcc2-141">DLL</span><span class="sxs-lookup"><span data-stu-id="edcc2-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="edcc2-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="edcc2-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edcc2-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="edcc2-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edcc2-144">\_DEVICEERRORCOUNTS CIM</span><span class="sxs-lookup"><span data-stu-id="edcc2-144">CIM\_DeviceErrorCounts</span></span>](resetcounter-method-in-class-cim-deviceerrorcounts.md)
</dt> <dt>

[<span data-ttu-id="edcc2-145">**\_DEVICEERRORCOUNTS CIM**</span><span class="sxs-lookup"><span data-stu-id="edcc2-145">**CIM\_DeviceErrorCounts**</span></span>](cim-deviceerrorcounts.md)
</dt> </dl>

 

