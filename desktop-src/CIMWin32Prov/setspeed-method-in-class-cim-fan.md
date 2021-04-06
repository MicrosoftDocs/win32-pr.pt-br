---
description: O método SETSPEED solicita que a velocidade do ventilador seja definida com o valor especificado no parâmetro de entrada do método.
ms.assetid: 7dd1cd57-66c5-4b50-9a73-31caf0b824e6
ms.tgt_platform: multiple
title: Método SETSPEED da classe CIM_Fan
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Fan.SetSpeed
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 16d90dbef3a9318ad144303e5720cea0abbde03e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826694"
---
# <a name="setspeed-method-of-the-cim_fan-class"></a><span data-ttu-id="cca39-103">Método SETSPEED da classe de \_ ventilador CIM</span><span class="sxs-lookup"><span data-stu-id="cca39-103">SetSpeed method of the CIM\_Fan class</span></span>

<span data-ttu-id="cca39-104">O método **SETSPEED** solicita que a velocidade do ventilador seja definida com o valor especificado no parâmetro de entrada do método.</span><span class="sxs-lookup"><span data-stu-id="cca39-104">The **SetSpeed** method requests that the fan speed be set to the value specified in the method's input parameter.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cca39-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="cca39-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cca39-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="cca39-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cca39-107">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="cca39-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="cca39-108">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="cca39-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="cca39-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cca39-109">Syntax</span></span>


```mof
uint32 SetSpeed(
  [in] uint64 DesiredSpeed
);
```



## <a name="parameters"></a><span data-ttu-id="cca39-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cca39-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cca39-111">*DesiredSpeed* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cca39-111">*DesiredSpeed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cca39-112">Velocidade de ventilador solicitada, em rotações por minuto.</span><span class="sxs-lookup"><span data-stu-id="cca39-112">Requested fan speed, in revolutions per minute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cca39-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cca39-113">Return value</span></span>

<span data-ttu-id="cca39-114">Retorna um valor de 0 (zero) em caso de sucesso, 1 (um) se a solicitação não tiver suporte e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="cca39-114">Returns a value of 0 (zero) on success, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="cca39-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="cca39-115">Remarks</span></span>

<span data-ttu-id="cca39-116">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="cca39-116">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="cca39-117">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="cca39-117">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="cca39-118">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="cca39-118">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cca39-119">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="cca39-119">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cca39-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cca39-120">Requirements</span></span>



| <span data-ttu-id="cca39-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="cca39-121">Requirement</span></span> | <span data-ttu-id="cca39-122">Valor</span><span class="sxs-lookup"><span data-stu-id="cca39-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cca39-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cca39-123">Minimum supported client</span></span><br/> | <span data-ttu-id="cca39-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cca39-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cca39-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cca39-125">Minimum supported server</span></span><br/> | <span data-ttu-id="cca39-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cca39-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cca39-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="cca39-127">Namespace</span></span><br/>                | <span data-ttu-id="cca39-128">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="cca39-128">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cca39-129">MOF</span><span class="sxs-lookup"><span data-stu-id="cca39-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cca39-130"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cca39-130"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cca39-131">DLL</span><span class="sxs-lookup"><span data-stu-id="cca39-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cca39-132"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cca39-132"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cca39-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="cca39-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cca39-134">\_Ventilador CIM</span><span class="sxs-lookup"><span data-stu-id="cca39-134">CIM\_Fan</span></span>](setspeed-method-in-class-cim-fan.md)
</dt> <dt>

[<span data-ttu-id="cca39-135">**\_Ventilador CIM**</span><span class="sxs-lookup"><span data-stu-id="cca39-135">**CIM\_Fan**</span></span>](cim-fan.md)
</dt> </dl>

 

