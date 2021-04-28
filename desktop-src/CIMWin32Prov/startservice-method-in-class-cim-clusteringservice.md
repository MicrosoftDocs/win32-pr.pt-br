---
description: Método StartService da classe CIM_ClusteringService-o método StartService coloca o serviço em um estado iniciado.
ms.assetid: 2efd2a06-a03c-4f4c-b2fa-889f84faac0f
ms.tgt_platform: multiple
title: Método StartService da classe CIM_ClusteringService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusteringService.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: dcd18af37da9302256776cfee844fd83f989c9b7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086184"
---
# <a name="startservice-method-of-the-cim_clusteringservice-class"></a><span data-ttu-id="4be0e-103">Método StartService da \_ classe ClusteringService do CIM</span><span class="sxs-lookup"><span data-stu-id="4be0e-103">StartService method of the CIM\_ClusteringService class</span></span>

<span data-ttu-id="4be0e-104">O método **StartService** coloca o serviço em um estado iniciado.</span><span class="sxs-lookup"><span data-stu-id="4be0e-104">The **StartService** method puts the service in a started state.</span></span> <span data-ttu-id="4be0e-105">Em uma subclasse, o conjunto de códigos de retorno possíveis pode ser especificado usando um qualificador **ValueMap** no método.</span><span class="sxs-lookup"><span data-stu-id="4be0e-105">In a subclass, the set of possible return codes can be specified using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="4be0e-106">As cadeias de caracteres nas quais os conteúdos de **ValueMap** são convertidos também podem ser especificadas na subclasse como um qualificador de matriz de **valores** .</span><span class="sxs-lookup"><span data-stu-id="4be0e-106">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="4be0e-107">Esse método é herdado [**do \_ serviço CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="4be0e-107">This method is inherited from [**CIM\_Service**](cim-service.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4be0e-108">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="4be0e-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4be0e-109">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4be0e-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4be0e-110">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="4be0e-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4be0e-111">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="4be0e-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4be0e-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4be0e-112">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="4be0e-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4be0e-113">Parameters</span></span>

<span data-ttu-id="4be0e-114">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4be0e-114">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4be0e-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="4be0e-115">Return value</span></span>

<span data-ttu-id="4be0e-116">Retorna um valor de 0 (zero) se o serviço foi iniciado com êxito, 1 (um) se a solicitação não tiver suporte e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="4be0e-116">Returns a value of 0 (zero) if the service was successfully started, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="4be0e-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="4be0e-117">Remarks</span></span>

<span data-ttu-id="4be0e-118">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="4be0e-118">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="4be0e-119">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="4be0e-119">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="4be0e-120">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="4be0e-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4be0e-121">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="4be0e-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4be0e-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4be0e-122">Requirements</span></span>



| <span data-ttu-id="4be0e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4be0e-123">Requirement</span></span> | <span data-ttu-id="4be0e-124">Valor</span><span class="sxs-lookup"><span data-stu-id="4be0e-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4be0e-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4be0e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4be0e-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4be0e-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4be0e-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4be0e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4be0e-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4be0e-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4be0e-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="4be0e-129">Namespace</span></span><br/>                | <span data-ttu-id="4be0e-130">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="4be0e-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4be0e-131">MOF</span><span class="sxs-lookup"><span data-stu-id="4be0e-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4be0e-132"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4be0e-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4be0e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="4be0e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4be0e-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4be0e-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4be0e-135">Consulte também</span><span class="sxs-lookup"><span data-stu-id="4be0e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4be0e-136">\_CLUSTERINGSERVICE CIM</span><span class="sxs-lookup"><span data-stu-id="4be0e-136">CIM\_ClusteringService</span></span>](startservice-method-in-class-cim-clusteringservice.md)
</dt> <dt>

[<span data-ttu-id="4be0e-137">**\_CLUSTERINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="4be0e-137">**CIM\_ClusteringService**</span></span>](cim-clusteringservice.md)
</dt> </dl>

 

