---
description: Interrompe o serviço representado pelo objeto derivado do serviço CIM \_ .
ms.assetid: f9eedde7-8d71-40a2-b1e9-7ba97e634f64
ms.tgt_platform: multiple
title: Método StopService da classe CIM_Service (Sdoias. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 14a7d378b514a93906c3be4f711bd6ab5b88bf17
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089221"
---
# <a name="stopservice-method-of-the-cim_service-class-sdoiash"></a><span data-ttu-id="ebf25-103">Método StopService da classe CIM_Service (Sdoias. h)</span><span class="sxs-lookup"><span data-stu-id="ebf25-103">StopService method of the CIM_Service class (Sdoias.h)</span></span>

<span data-ttu-id="ebf25-104">O método **StopService** interrompe o serviço representado pelo objeto derivado do [**\_ serviço CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="ebf25-104">The **StopService** method stops the service represented by the object derived from [**CIM\_Service**](cim-service.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ebf25-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="ebf25-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ebf25-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ebf25-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ebf25-107">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="ebf25-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ebf25-108">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ebf25-108">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ebf25-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ebf25-109">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="ebf25-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ebf25-110">Parameters</span></span>

<span data-ttu-id="ebf25-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ebf25-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ebf25-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ebf25-112">Return value</span></span>

<span data-ttu-id="ebf25-113">Retorna um valor de 0 (zero) se o serviço foi interrompido com êxito, 1 (um) se a solicitação não tiver suporte e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="ebf25-113">Returns a value of 0 (zero) if the service was successfully stopped, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebf25-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ebf25-114">Remarks</span></span>

<span data-ttu-id="ebf25-115">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="ebf25-115">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="ebf25-116">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="ebf25-116">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="ebf25-117">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="ebf25-117">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ebf25-118">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="ebf25-118">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebf25-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ebf25-119">Requirements</span></span>



| <span data-ttu-id="ebf25-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebf25-120">Requirement</span></span> | <span data-ttu-id="ebf25-121">Valor</span><span class="sxs-lookup"><span data-stu-id="ebf25-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ebf25-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ebf25-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ebf25-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ebf25-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ebf25-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ebf25-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ebf25-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ebf25-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ebf25-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="ebf25-126">Namespace</span></span><br/>                | <span data-ttu-id="ebf25-127">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="ebf25-127">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ebf25-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ebf25-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebf25-129"><dt>Sdoias. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebf25-129"><dt>Sdoias.h</dt></span></span> </dl>     |
| <span data-ttu-id="ebf25-130">MOF</span><span class="sxs-lookup"><span data-stu-id="ebf25-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ebf25-131"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ebf25-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ebf25-132">DLL</span><span class="sxs-lookup"><span data-stu-id="ebf25-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ebf25-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebf25-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebf25-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="ebf25-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebf25-135">\_Serviço CIM</span><span class="sxs-lookup"><span data-stu-id="ebf25-135">CIM\_Service</span></span>](stopservice-method-in-class-cim-service.md)
</dt> <dt>

[<span data-ttu-id="ebf25-136">**\_Serviço CIM**</span><span class="sxs-lookup"><span data-stu-id="ebf25-136">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

