---
description: Interrompe o serviço representado pelo objeto derivado de CIM \_ DS.
ms.assetid: 443a2afa-ed46-4378-a06f-5f9f94af51c9
ms.tgt_platform: multiple
title: Método StopService da classe CIM_BootService (Sdoias. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BootService.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c054a9d05410ddbe7ee7d11c5bd4adba9e0ce83b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500960"
---
# <a name="stopservice-method-of-the-cim_bootservice-class"></a><span data-ttu-id="778f6-103">Método StopService da \_ classe DS do CIM</span><span class="sxs-lookup"><span data-stu-id="778f6-103">StopService method of the CIM\_BootService class</span></span>

<span data-ttu-id="778f6-104">O método **StopService** interrompe o serviço representado pelo objeto derivado de [**CIM \_ DS**](cim-bootservice.md).</span><span class="sxs-lookup"><span data-stu-id="778f6-104">The **StopService** method stops the service represented by the object derived from [**CIM\_BootService**](cim-bootservice.md).</span></span> <span data-ttu-id="778f6-105">Esse método é herdado [**do \_ serviço CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="778f6-105">This method is inherited from [**CIM\_Service**](cim-service.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="778f6-106">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="778f6-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="778f6-107">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="778f6-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="778f6-108">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="778f6-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="778f6-109">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="778f6-109">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="778f6-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="778f6-110">Syntax</span></span>


```mof
Integer StopService();
```



## <a name="parameters"></a><span data-ttu-id="778f6-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="778f6-111">Parameters</span></span>

<span data-ttu-id="778f6-112">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="778f6-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="778f6-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="778f6-113">Return value</span></span>

<span data-ttu-id="778f6-114">Retorna um valor de 0 (zero) em caso de sucesso, 1 (um) se a solicitação não tiver suporte e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="778f6-114">Returns a value of 0 (zero) on success, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="778f6-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="778f6-115">Remarks</span></span>

<span data-ttu-id="778f6-116">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="778f6-116">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="778f6-117">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="778f6-117">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="778f6-118">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="778f6-118">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="778f6-119">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="778f6-119">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="778f6-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="778f6-120">Requirements</span></span>



| <span data-ttu-id="778f6-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="778f6-121">Requirement</span></span> | <span data-ttu-id="778f6-122">Valor</span><span class="sxs-lookup"><span data-stu-id="778f6-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="778f6-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="778f6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="778f6-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="778f6-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="778f6-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="778f6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="778f6-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="778f6-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="778f6-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="778f6-127">Namespace</span></span><br/>                | <span data-ttu-id="778f6-128">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="778f6-128">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="778f6-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="778f6-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="778f6-130"><dt>Sdoias. h</dt></span><span class="sxs-lookup"><span data-stu-id="778f6-130"><dt>Sdoias.h</dt></span></span> </dl>     |
| <span data-ttu-id="778f6-131">MOF</span><span class="sxs-lookup"><span data-stu-id="778f6-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="778f6-132"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="778f6-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="778f6-133">DLL</span><span class="sxs-lookup"><span data-stu-id="778f6-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="778f6-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="778f6-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="778f6-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="778f6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="778f6-136">\_DS CIM</span><span class="sxs-lookup"><span data-stu-id="778f6-136">CIM\_BootService</span></span>](stopservice-method-in-class-cim-bootservice.md)
</dt> <dt>

[<span data-ttu-id="778f6-137">**\_DS CIM**</span><span class="sxs-lookup"><span data-stu-id="778f6-137">**CIM\_BootService**</span></span>](cim-bootservice.md)
</dt> </dl>

 

