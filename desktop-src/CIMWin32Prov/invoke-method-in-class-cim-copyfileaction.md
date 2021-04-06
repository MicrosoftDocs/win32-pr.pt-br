---
description: O método Invoke da classe CIM \_ CopyAction usa uma ação específica. Os detalhes sobre como o método executa a ação são específicos da implementação. Esse método é herdado da \_ ação CIM.
ms.assetid: b948e9ed-332d-4ac5-be7f-88b7f46f5f1d
ms.tgt_platform: multiple
title: Método Invoke da classe CIM_CopyFileAction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CopyFileAction.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b88ddafd0420a40af8b815aab26849572cb7c019
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826299"
---
# <a name="invoke-method-of-the-cim_copyfileaction-class"></a><span data-ttu-id="84078-105">Método Invoke da classe CIM \_ CopyValue</span><span class="sxs-lookup"><span data-stu-id="84078-105">Invoke method of the CIM\_CopyFileAction class</span></span>

<span data-ttu-id="84078-106">O método **Invoke** da classe [**CIM \_ CopyAction**](cim-copyfileaction.md) usa uma ação específica.</span><span class="sxs-lookup"><span data-stu-id="84078-106">The **Invoke** method of the [**CIM\_CopyFileAction**](cim-copyfileaction.md) class takes a particular action.</span></span> <span data-ttu-id="84078-107">Os detalhes sobre como o método executa a ação são específicos da implementação.</span><span class="sxs-lookup"><span data-stu-id="84078-107">Details about how the method performs the action are implementation-specific.</span></span> <span data-ttu-id="84078-108">Esse método é herdado [**da \_ ação CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="84078-108">This method is inherited from [**CIM\_Action**](cim-action.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="84078-109">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="84078-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="84078-110">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="84078-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="84078-111">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="84078-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="84078-112">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="84078-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="84078-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="84078-113">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="84078-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="84078-114">Parameters</span></span>

<span data-ttu-id="84078-115">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="84078-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="84078-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="84078-116">Return value</span></span>

<span data-ttu-id="84078-117">Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="84078-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="84078-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="84078-118">Remarks</span></span>

<span data-ttu-id="84078-119">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="84078-119">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="84078-120">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="84078-120">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="84078-121">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="84078-121">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="84078-122">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="84078-122">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="84078-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84078-123">Requirements</span></span>



| <span data-ttu-id="84078-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="84078-124">Requirement</span></span> | <span data-ttu-id="84078-125">Valor</span><span class="sxs-lookup"><span data-stu-id="84078-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="84078-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84078-126">Minimum supported client</span></span><br/> | <span data-ttu-id="84078-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="84078-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="84078-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84078-128">Minimum supported server</span></span><br/> | <span data-ttu-id="84078-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="84078-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="84078-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="84078-130">Namespace</span></span><br/>                | <span data-ttu-id="84078-131">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="84078-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="84078-132">MOF</span><span class="sxs-lookup"><span data-stu-id="84078-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84078-133"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="84078-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="84078-134">DLL</span><span class="sxs-lookup"><span data-stu-id="84078-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84078-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84078-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84078-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="84078-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84078-137">**CIM \_ CopyAction**</span><span class="sxs-lookup"><span data-stu-id="84078-137">**CIM\_CopyFileAction**</span></span>](invoke-method-in-class-cim-copyfileaction.md)
</dt> <dt>

[<span data-ttu-id="84078-138">**CIM \_ CopyAction**</span><span class="sxs-lookup"><span data-stu-id="84078-138">**CIM\_CopyFileAction**</span></span>](cim-copyfileaction.md)
</dt> </dl>

 

