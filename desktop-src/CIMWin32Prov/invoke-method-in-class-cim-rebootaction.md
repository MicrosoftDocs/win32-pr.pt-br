---
description: O método Invoke da classe CIM \_ rebootaction usa uma ação específica. Os detalhes de como o método executa a ação são específicos da implementação. Esse método é herdado da \_ ação CIM.
ms.assetid: 27b6571e-94fe-423e-89ab-5ba2bc632882
ms.tgt_platform: multiple
title: Método Invoke da classe CIM_RebootAction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RebootAction.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e68849a486cc6a5b61dc55cf86e259e2f58435e8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756043"
---
# <a name="invoke-method-of-the-cim_rebootaction-class"></a><span data-ttu-id="59c10-105">Método Invoke da classe CIM \_ rebootaction</span><span class="sxs-lookup"><span data-stu-id="59c10-105">Invoke method of the CIM\_RebootAction class</span></span>

<span data-ttu-id="59c10-106">O método **Invoke** da classe [**CIM \_ rebootaction**](cim-rebootaction.md) usa uma ação específica.</span><span class="sxs-lookup"><span data-stu-id="59c10-106">The **Invoke** method of the [**CIM\_RebootAction**](cim-rebootaction.md) class takes a particular action.</span></span> <span data-ttu-id="59c10-107">Os detalhes de como o método executa a ação são específicos da implementação.</span><span class="sxs-lookup"><span data-stu-id="59c10-107">The details of how the method performs the action are implementation specific.</span></span> <span data-ttu-id="59c10-108">Esse método é herdado [**da \_ ação CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="59c10-108">This method is inherited from [**CIM\_Action**](cim-action.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="59c10-109">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="59c10-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="59c10-110">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="59c10-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="59c10-111">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="59c10-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="59c10-112">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="59c10-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="59c10-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="59c10-113">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="59c10-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="59c10-114">Parameters</span></span>

<span data-ttu-id="59c10-115">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="59c10-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="59c10-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="59c10-116">Return value</span></span>

<span data-ttu-id="59c10-117">Retorna um valor inteiro de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="59c10-117">Returns an integer value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="59c10-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="59c10-118">Remarks</span></span>

<span data-ttu-id="59c10-119">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="59c10-119">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="59c10-120">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="59c10-120">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="59c10-121">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="59c10-121">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="59c10-122">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="59c10-122">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="59c10-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59c10-123">Requirements</span></span>



| <span data-ttu-id="59c10-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="59c10-124">Requirement</span></span> | <span data-ttu-id="59c10-125">Valor</span><span class="sxs-lookup"><span data-stu-id="59c10-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="59c10-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59c10-126">Minimum supported client</span></span><br/> | <span data-ttu-id="59c10-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="59c10-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="59c10-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59c10-128">Minimum supported server</span></span><br/> | <span data-ttu-id="59c10-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="59c10-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="59c10-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="59c10-130">Namespace</span></span><br/>                | <span data-ttu-id="59c10-131">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="59c10-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="59c10-132">MOF</span><span class="sxs-lookup"><span data-stu-id="59c10-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="59c10-133"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="59c10-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="59c10-134">DLL</span><span class="sxs-lookup"><span data-stu-id="59c10-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59c10-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59c10-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59c10-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="59c10-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59c10-137">Reinicialização de CIM \_</span><span class="sxs-lookup"><span data-stu-id="59c10-137">CIM\_RebootAction</span></span>](invoke-method-in-class-cim-rebootaction.md)
</dt> <dt>

[<span data-ttu-id="59c10-138">**Reinicialização de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="59c10-138">**CIM\_RebootAction**</span></span>](cim-rebootaction.md)
</dt> </dl>

 

