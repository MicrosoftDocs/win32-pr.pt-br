---
description: O método seturgência define o nível de urgência desejado para um alarme.
ms.assetid: ac2e7fda-1317-440a-adbd-1ef0844d124c
ms.tgt_platform: multiple
title: Método seturgência da classe CIM_AlarmDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AlarmDevice.SetUrgency
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 35918677e210ac2fe7ac4798a04db9dc628f5fa1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920365"
---
# <a name="seturgency-method-of-the-cim_alarmdevice-class"></a><span data-ttu-id="044c5-103">Método seturgência da \_ classe AlarmDevice do CIM</span><span class="sxs-lookup"><span data-stu-id="044c5-103">SetUrgency method of the CIM\_AlarmDevice class</span></span>

<span data-ttu-id="044c5-104">O método **seturgência** define o nível de urgência desejado para um alarme.</span><span class="sxs-lookup"><span data-stu-id="044c5-104">The **SetUrgency** method sets the desired urgency level for an alarm.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="044c5-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="044c5-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="044c5-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="044c5-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="044c5-107">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="044c5-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="044c5-108">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="044c5-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="044c5-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="044c5-109">Syntax</span></span>


```mof
uint32 SetUrgency(
  [in] uint16 RequestedUrgency
);
```



## <a name="parameters"></a><span data-ttu-id="044c5-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="044c5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="044c5-111">*RequestedUrgency* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="044c5-111">*RequestedUrgency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="044c5-112">A frequência relativa na qual o alarme pisca, vibra ou emite tons audíveis.</span><span class="sxs-lookup"><span data-stu-id="044c5-112">Relative frequency at which the alarm flashes, vibrates, or emits audible tones.</span></span> <span data-ttu-id="044c5-113">Os valores a seguir são da propriedade **urgência** no [**CIM \_ AlarmDevice**](cim-alarmdevice.md).</span><span class="sxs-lookup"><span data-stu-id="044c5-113">The following values are from the **Urgency** property in [**CIM\_AlarmDevice**](cim-alarmdevice.md).</span></span>

<dt>

<span data-ttu-id="044c5-114">0</span><span class="sxs-lookup"><span data-stu-id="044c5-114">0</span></span>
</dt> <dd>

<span data-ttu-id="044c5-115">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="044c5-115">Unknown.</span></span>

</dd> <dt>

<span data-ttu-id="044c5-116">1</span><span class="sxs-lookup"><span data-stu-id="044c5-116">1</span></span>
</dt> <dd>

<span data-ttu-id="044c5-117">Outros.</span><span class="sxs-lookup"><span data-stu-id="044c5-117">Other.</span></span>

</dd> <dt>

<span data-ttu-id="044c5-118">2</span><span class="sxs-lookup"><span data-stu-id="044c5-118">2</span></span>
</dt> <dd>

<span data-ttu-id="044c5-119">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="044c5-119">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="044c5-120">3</span><span class="sxs-lookup"><span data-stu-id="044c5-120">3</span></span>
</dt> <dd>

<span data-ttu-id="044c5-121">Informativa.</span><span class="sxs-lookup"><span data-stu-id="044c5-121">Informational.</span></span>

</dd> <dt>

<span data-ttu-id="044c5-122">4</span><span class="sxs-lookup"><span data-stu-id="044c5-122">4</span></span>
</dt> <dd>

<span data-ttu-id="044c5-123">Não crítico.</span><span class="sxs-lookup"><span data-stu-id="044c5-123">Non-critical.</span></span>

</dd> <dt>

<span data-ttu-id="044c5-124">5</span><span class="sxs-lookup"><span data-stu-id="044c5-124">5</span></span>
</dt> <dd>

<span data-ttu-id="044c5-125">Crítica.</span><span class="sxs-lookup"><span data-stu-id="044c5-125">Critical.</span></span>

</dd> <dt>

<span data-ttu-id="044c5-126">6</span><span class="sxs-lookup"><span data-stu-id="044c5-126">6</span></span>
</dt> <dd>

<span data-ttu-id="044c5-127">Irrecuperável.</span><span class="sxs-lookup"><span data-stu-id="044c5-127">Unrecoverable.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="044c5-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="044c5-128">Return value</span></span>

<span data-ttu-id="044c5-129">Retorna um valor de 0 (zero) em êxito, 1 (um) se o nível de urgência solicitado não for suportado e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="044c5-129">Returns a value of 0 (zero) on success, 1 (one) if the requested urgency level is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="044c5-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="044c5-130">Remarks</span></span>

<span data-ttu-id="044c5-131">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="044c5-131">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="044c5-132">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="044c5-132">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="044c5-133">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="044c5-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="044c5-134">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="044c5-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="044c5-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="044c5-135">Requirements</span></span>



| <span data-ttu-id="044c5-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="044c5-136">Requirement</span></span> | <span data-ttu-id="044c5-137">Valor</span><span class="sxs-lookup"><span data-stu-id="044c5-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="044c5-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="044c5-138">Minimum supported client</span></span><br/> | <span data-ttu-id="044c5-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="044c5-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="044c5-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="044c5-140">Minimum supported server</span></span><br/> | <span data-ttu-id="044c5-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="044c5-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="044c5-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="044c5-142">Namespace</span></span><br/>                | <span data-ttu-id="044c5-143">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="044c5-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="044c5-144">MOF</span><span class="sxs-lookup"><span data-stu-id="044c5-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="044c5-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="044c5-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="044c5-146">DLL</span><span class="sxs-lookup"><span data-stu-id="044c5-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="044c5-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="044c5-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="044c5-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="044c5-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="044c5-149">\_ALARMDEVICE CIM</span><span class="sxs-lookup"><span data-stu-id="044c5-149">CIM\_AlarmDevice</span></span>](seturgency-method-in-class-cim-alarmdevice.md)
</dt> <dt>

[<span data-ttu-id="044c5-150">**\_ALARMDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="044c5-150">**CIM\_AlarmDevice**</span></span>](cim-alarmdevice.md)
</dt> </dl>

 

