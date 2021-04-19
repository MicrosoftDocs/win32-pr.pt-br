---
description: O método Invoke da classe CIM \_ Removeaction usa uma ação específica. Os detalhes de como o método executa a ação são específicos da implementação. Esse método é herdado da \_ ação CIM.
ms.assetid: 7fc33654-a51b-41cf-a5b4-ef08fd6e40ac
ms.tgt_platform: multiple
title: Método Invoke da classe CIM_RemoveFileAction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RemoveFileAction.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a371ad1f7b1da874b6a049b04d5f50ec694cf181
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753808"
---
# <a name="invoke-method-of-the-cim_removefileaction-class"></a><span data-ttu-id="0f281-105">Método Invoke da classe CIM \_ Removeaction</span><span class="sxs-lookup"><span data-stu-id="0f281-105">Invoke method of the CIM\_RemoveFileAction class</span></span>

<span data-ttu-id="0f281-106">O método **Invoke** da classe [**CIM \_ removeaction**](cim-removefileaction.md) usa uma ação específica.</span><span class="sxs-lookup"><span data-stu-id="0f281-106">The **Invoke** method of the [**CIM\_RemoveFileAction**](cim-removefileaction.md) class takes a particular action.</span></span> <span data-ttu-id="0f281-107">Os detalhes de como o método executa a ação são específicos da implementação.</span><span class="sxs-lookup"><span data-stu-id="0f281-107">The details of how the method performs the action is implementation specific.</span></span> <span data-ttu-id="0f281-108">Esse método é herdado [**da \_ ação CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="0f281-108">This method is inherited from [**CIM\_Action**](cim-action.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0f281-109">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="0f281-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0f281-110">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0f281-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0f281-111">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="0f281-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0f281-112">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="0f281-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0f281-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0f281-113">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="0f281-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0f281-114">Parameters</span></span>

<span data-ttu-id="0f281-115">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="0f281-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0f281-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0f281-116">Return value</span></span>

<span data-ttu-id="0f281-117">Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="0f281-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f281-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="0f281-118">Remarks</span></span>

<span data-ttu-id="0f281-119">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="0f281-119">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="0f281-120">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="0f281-120">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="0f281-121">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="0f281-121">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0f281-122">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="0f281-122">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f281-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f281-123">Requirements</span></span>



| <span data-ttu-id="0f281-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f281-124">Requirement</span></span> | <span data-ttu-id="0f281-125">Valor</span><span class="sxs-lookup"><span data-stu-id="0f281-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f281-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0f281-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0f281-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0f281-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0f281-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0f281-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0f281-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0f281-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0f281-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="0f281-130">Namespace</span></span><br/>                | <span data-ttu-id="0f281-131">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="0f281-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0f281-132">MOF</span><span class="sxs-lookup"><span data-stu-id="0f281-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0f281-133"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0f281-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0f281-134">DLL</span><span class="sxs-lookup"><span data-stu-id="0f281-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f281-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f281-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f281-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="0f281-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f281-137">\_RemoveFile CIM</span><span class="sxs-lookup"><span data-stu-id="0f281-137">CIM\_RemoveFileAction</span></span>](invoke-method-in-class-cim-removefileaction.md)
</dt> <dt>

[<span data-ttu-id="0f281-138">**\_RemoveFile CIM**</span><span class="sxs-lookup"><span data-stu-id="0f281-138">**CIM\_RemoveFileAction**</span></span>](cim-removefileaction.md)
</dt> </dl>

 

