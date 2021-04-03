---
description: O método EvictNode remove um sistema de computador de um cluster. O nó a ser removido é especificado como um parâmetro para o método.
ms.assetid: 4691d536-ade3-4a02-bc28-e31ebaf5d9e4
ms.tgt_platform: multiple
title: Método EvictNode da classe CIM_ClusteringService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusteringService.EvictNode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d68ddc1adc0af335dcf2d4139cf7c1f0a381d986
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646309"
---
# <a name="evictnode-method-of-the-cim_clusteringservice-class"></a><span data-ttu-id="cd136-104">Método EvictNode da \_ classe CLUSTERINGSERVICE CIM</span><span class="sxs-lookup"><span data-stu-id="cd136-104">EvictNode method of the CIM\_ClusteringService class</span></span>

<span data-ttu-id="cd136-105">O método **EvictNode** remove um sistema de computador de um cluster.</span><span class="sxs-lookup"><span data-stu-id="cd136-105">The **EvictNode** method removes a computer system from a cluster.</span></span> <span data-ttu-id="cd136-106">O nó a ser removido é especificado como um parâmetro para o método.</span><span class="sxs-lookup"><span data-stu-id="cd136-106">The node to be evicted is specified as a parameter to the method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cd136-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="cd136-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cd136-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="cd136-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cd136-109">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="cd136-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="cd136-110">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="cd136-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="cd136-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cd136-111">Syntax</span></span>


```mof
uint32 EvictNode(
  [in] CIM_ComputerSystem REF CS
);
```



## <a name="parameters"></a><span data-ttu-id="cd136-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cd136-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd136-113">*Cs* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cd136-113">*CS* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd136-114">Referência ao sistema de computador a ser removido do cluster.</span><span class="sxs-lookup"><span data-stu-id="cd136-114">Reference to the computer system to remove from the cluster.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd136-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cd136-115">Return value</span></span>

<span data-ttu-id="cd136-116">Retornará 0 (zero) se o sistema de computador for removido com êxito, 1 (um) se o método não tiver suporte e qualquer outro número se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="cd136-116">Returns 0 (zero) if the computer system is successfully evicted, 1 (one) if the method is not supported, and any other number if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd136-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="cd136-117">Remarks</span></span>

<span data-ttu-id="cd136-118">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="cd136-118">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="cd136-119">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="cd136-119">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="cd136-120">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="cd136-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cd136-121">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="cd136-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd136-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd136-122">Requirements</span></span>



| <span data-ttu-id="cd136-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd136-123">Requirement</span></span> | <span data-ttu-id="cd136-124">Valor</span><span class="sxs-lookup"><span data-stu-id="cd136-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd136-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd136-125">Minimum supported client</span></span><br/> | <span data-ttu-id="cd136-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cd136-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cd136-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd136-127">Minimum supported server</span></span><br/> | <span data-ttu-id="cd136-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cd136-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cd136-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="cd136-129">Namespace</span></span><br/>                | <span data-ttu-id="cd136-130">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="cd136-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cd136-131">MOF</span><span class="sxs-lookup"><span data-stu-id="cd136-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd136-132"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cd136-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cd136-133">DLL</span><span class="sxs-lookup"><span data-stu-id="cd136-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd136-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd136-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd136-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="cd136-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd136-136">**\_CLUSTERINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="cd136-136">**CIM\_ClusteringService**</span></span>](evictnode-method-in-class-cim-clusteringservice.md)
</dt> <dt>

[<span data-ttu-id="cd136-137">**\_CLUSTERINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="cd136-137">**CIM\_ClusteringService**</span></span>](cim-clusteringservice.md)
</dt> </dl>

 

