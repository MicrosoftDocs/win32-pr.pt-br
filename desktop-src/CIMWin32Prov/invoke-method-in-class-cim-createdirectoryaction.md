---
description: O método Invoke da classe CIM \_ Createdirectoryaction usa uma ação específica. Os detalhes sobre como o método executa a ação são específicos da implementação. Esse método é herdado da \_ ação CIM.
ms.assetid: f14e215d-31f2-46c5-b45e-3de64ce46bf2
ms.tgt_platform: multiple
title: Método Invoke da classe CIM_CreateDirectoryAction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CreateDirectoryAction.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 690a29ae0ea85e0b965d2a426703eea87aee9184
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646303"
---
# <a name="invoke-method-of-the-cim_createdirectoryaction-class"></a><span data-ttu-id="e1312-105">Método Invoke da classe CIM \_ Createdirectoryaction</span><span class="sxs-lookup"><span data-stu-id="e1312-105">Invoke method of the CIM\_CreateDirectoryAction class</span></span>

<span data-ttu-id="e1312-106">O método **Invoke** da classe [**CIM \_ createdirectoryaction**](cim-createdirectoryaction.md) usa uma ação específica.</span><span class="sxs-lookup"><span data-stu-id="e1312-106">The **Invoke** method of the [**CIM\_CreateDirectoryAction**](cim-createdirectoryaction.md) class takes a particular action.</span></span> <span data-ttu-id="e1312-107">Os detalhes sobre como o método executa a ação são específicos da implementação.</span><span class="sxs-lookup"><span data-stu-id="e1312-107">Details about how the method performs the action are implementation-specific.</span></span> <span data-ttu-id="e1312-108">Esse método é herdado [**da \_ ação CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="e1312-108">This method is inherited from [**CIM\_Action**](cim-action.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e1312-109">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="e1312-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e1312-110">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e1312-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e1312-111">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="e1312-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e1312-112">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="e1312-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e1312-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e1312-113">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="e1312-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e1312-114">Parameters</span></span>

<span data-ttu-id="e1312-115">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e1312-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e1312-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e1312-116">Return value</span></span>

<span data-ttu-id="e1312-117">Retorna um valor 0 em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="e1312-117">Returns a value of 0 on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1312-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="e1312-118">Remarks</span></span>

<span data-ttu-id="e1312-119">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="e1312-119">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="e1312-120">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="e1312-120">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="e1312-121">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="e1312-121">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e1312-122">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="e1312-122">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1312-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1312-123">Requirements</span></span>



| <span data-ttu-id="e1312-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1312-124">Requirement</span></span> | <span data-ttu-id="e1312-125">Valor</span><span class="sxs-lookup"><span data-stu-id="e1312-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1312-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e1312-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e1312-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e1312-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e1312-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e1312-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e1312-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e1312-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e1312-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="e1312-130">Namespace</span></span><br/>                | <span data-ttu-id="e1312-131">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e1312-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e1312-132">MOF</span><span class="sxs-lookup"><span data-stu-id="e1312-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e1312-133"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e1312-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e1312-134">DLL</span><span class="sxs-lookup"><span data-stu-id="e1312-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1312-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1312-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1312-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1312-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1312-137">**CIM \_ Createdirectoryaction**</span><span class="sxs-lookup"><span data-stu-id="e1312-137">**CIM\_CreateDirectoryAction**</span></span>](invoke-method-in-class-cim-createdirectoryaction.md)
</dt> <dt>

[<span data-ttu-id="e1312-138">**CIM \_ Createdirectoryaction**</span><span class="sxs-lookup"><span data-stu-id="e1312-138">**CIM\_CreateDirectoryAction**</span></span>](cim-createdirectoryaction.md)
</dt> </dl>

 

