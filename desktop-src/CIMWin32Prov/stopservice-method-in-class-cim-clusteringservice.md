---
description: Interrompe o serviço representado pelo objeto derivado de CIM \_ ClusteringService.
ms.assetid: b8dbaeeb-819b-469b-9f5e-d658e88d1a6e
ms.tgt_platform: multiple
title: Método StopService da classe CIM_ClusteringService (Sdoias. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusteringService.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a3a55f7b0a9527092e51156d55c7513ee59c4861
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826424"
---
# <a name="stopservice-method-of-the-cim_clusteringservice-class"></a><span data-ttu-id="c3d63-103">Método StopService da \_ classe ClusteringService do CIM</span><span class="sxs-lookup"><span data-stu-id="c3d63-103">StopService method of the CIM\_ClusteringService class</span></span>

<span data-ttu-id="c3d63-104">O método **StopService** interrompe o serviço representado pelo objeto derivado de [**CIM \_ ClusteringService**](cim-clusteringservice.md).</span><span class="sxs-lookup"><span data-stu-id="c3d63-104">The **StopService** method stops the service represented by the object derived from [**CIM\_ClusteringService**](cim-clusteringservice.md).</span></span> <span data-ttu-id="c3d63-105">Esse método é herdado [**do \_ serviço CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="c3d63-105">This method is inherited from [**CIM\_Service**](cim-service.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c3d63-106">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="c3d63-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c3d63-107">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c3d63-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c3d63-108">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="c3d63-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c3d63-109">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c3d63-109">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c3d63-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c3d63-110">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="c3d63-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c3d63-111">Parameters</span></span>

<span data-ttu-id="c3d63-112">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c3d63-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c3d63-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c3d63-113">Return value</span></span>

<span data-ttu-id="c3d63-114">Retorna um valor de 0 (zero) se o serviço foi interrompido com êxito, 1 (um) se a solicitação não tiver suporte e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="c3d63-114">Returns a value of 0 (zero) if the service was successfully stopped, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3d63-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3d63-115">Remarks</span></span>

<span data-ttu-id="c3d63-116">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="c3d63-116">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="c3d63-117">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="c3d63-117">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="c3d63-118">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="c3d63-118">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c3d63-119">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="c3d63-119">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3d63-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3d63-120">Requirements</span></span>



| <span data-ttu-id="c3d63-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3d63-121">Requirement</span></span> | <span data-ttu-id="c3d63-122">Valor</span><span class="sxs-lookup"><span data-stu-id="c3d63-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3d63-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3d63-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c3d63-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c3d63-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c3d63-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3d63-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c3d63-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c3d63-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c3d63-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="c3d63-127">Namespace</span></span><br/>                | <span data-ttu-id="c3d63-128">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c3d63-128">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c3d63-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c3d63-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3d63-130"><dt>Sdoias. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3d63-130"><dt>Sdoias.h</dt></span></span> </dl>     |
| <span data-ttu-id="c3d63-131">MOF</span><span class="sxs-lookup"><span data-stu-id="c3d63-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c3d63-132"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c3d63-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c3d63-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c3d63-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3d63-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3d63-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3d63-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3d63-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3d63-136">**\_CLUSTERINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="c3d63-136">**CIM\_ClusteringService**</span></span>](stopservice-method-in-class-cim-clusteringservice.md)
</dt> <dt>

[<span data-ttu-id="c3d63-137">**\_CLUSTERINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="c3d63-137">**CIM\_ClusteringService**</span></span>](cim-clusteringservice.md)
</dt> </dl>

 

