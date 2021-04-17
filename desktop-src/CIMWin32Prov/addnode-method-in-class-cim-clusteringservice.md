---
description: Coloca um novo sistema de computador em um cluster.
ms.assetid: 26d9428e-99de-4dcb-96ed-d773f28e015a
ms.tgt_platform: multiple
title: Método AddNode da classe CIM_ClusteringService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusteringService.AddNode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1769ebb876fd2ae99c800a61b80d339a850ab232
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754022"
---
# <a name="addnode-method-of-the-cim_clusteringservice-class"></a><span data-ttu-id="dcf43-103">Método AddNode da \_ classe ClusteringService do CIM</span><span class="sxs-lookup"><span data-stu-id="dcf43-103">AddNode method of the CIM\_ClusteringService class</span></span>

<span data-ttu-id="dcf43-104">O método **AddNode** traz um novo sistema de computador para um cluster.</span><span class="sxs-lookup"><span data-stu-id="dcf43-104">The **AddNode** method brings a new computer system into a cluster.</span></span> <span data-ttu-id="dcf43-105">O nó a ser adicionado é especificado como um parâmetro para o método.</span><span class="sxs-lookup"><span data-stu-id="dcf43-105">The node to be added is specified as a parameter to the method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dcf43-106">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="dcf43-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="dcf43-107">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="dcf43-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="dcf43-108">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="dcf43-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="dcf43-109">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="dcf43-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="dcf43-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dcf43-110">Syntax</span></span>


```mof
uint32 AddNode(
  [in] CIM_ComputerSystem REF CS
);
```



## <a name="parameters"></a><span data-ttu-id="dcf43-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dcf43-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcf43-112">*Cs* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dcf43-112">*CS* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcf43-113">Referência ao sistema de computador para adicionar ao cluster.</span><span class="sxs-lookup"><span data-stu-id="dcf43-113">Reference to the computer system to add to the cluster.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcf43-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dcf43-114">Return value</span></span>

<span data-ttu-id="dcf43-115">Retorna um valor de 0 (zero) em êxito, 1 (um) se a operação não tiver suporte e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="dcf43-115">Returns a value of 0 (zero) on success, 1 (one) if the operation is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcf43-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="dcf43-116">Remarks</span></span>

<span data-ttu-id="dcf43-117">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="dcf43-117">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="dcf43-118">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="dcf43-118">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="dcf43-119">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="dcf43-119">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="dcf43-120">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="dcf43-120">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcf43-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dcf43-121">Requirements</span></span>



| <span data-ttu-id="dcf43-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcf43-122">Requirement</span></span> | <span data-ttu-id="dcf43-123">Valor</span><span class="sxs-lookup"><span data-stu-id="dcf43-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dcf43-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dcf43-124">Minimum supported client</span></span><br/> | <span data-ttu-id="dcf43-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dcf43-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dcf43-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dcf43-126">Minimum supported server</span></span><br/> | <span data-ttu-id="dcf43-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dcf43-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dcf43-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="dcf43-128">Namespace</span></span><br/>                | <span data-ttu-id="dcf43-129">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="dcf43-129">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dcf43-130">MOF</span><span class="sxs-lookup"><span data-stu-id="dcf43-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dcf43-131"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dcf43-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dcf43-132">DLL</span><span class="sxs-lookup"><span data-stu-id="dcf43-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dcf43-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dcf43-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcf43-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="dcf43-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcf43-135">**\_CLUSTERINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="dcf43-135">**CIM\_ClusteringService**</span></span>](addnode-method-in-class-cim-clusteringservice.md)
</dt> <dt>

[<span data-ttu-id="dcf43-136">**\_CLUSTERINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="dcf43-136">**CIM\_ClusteringService**</span></span>](cim-clusteringservice.md)
</dt> </dl>

 

