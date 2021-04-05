---
description: O método Invoke da \_ classe directoryaction do CIM usa uma ação específica. Os detalhes de como o método executa a ação são específicos da implementação. Esse método é herdado da \_ ação CIM.
ms.assetid: e919dfdb-a52d-4bcb-abff-e1273c406226
ms.tgt_platform: multiple
title: Método Invoke da classe CIM_DirectoryAction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DirectoryAction.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f30184fe46cd8e8b9a595545ccba9a7d738af18e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826297"
---
# <a name="invoke-method-of-the-cim_directoryaction-class"></a><span data-ttu-id="1189b-105">Método Invoke da \_ classe directoryaction do CIM</span><span class="sxs-lookup"><span data-stu-id="1189b-105">Invoke method of the CIM\_DirectoryAction class</span></span>

<span data-ttu-id="1189b-106">O método **Invoke** da classe [**\_ directoryaction do CIM**](cim-directoryaction.md) usa uma ação específica.</span><span class="sxs-lookup"><span data-stu-id="1189b-106">The **Invoke** method of the [**CIM\_DirectoryAction**](cim-directoryaction.md) class takes a particular action.</span></span> <span data-ttu-id="1189b-107">Os detalhes de como o método executa a ação são específicos da implementação.</span><span class="sxs-lookup"><span data-stu-id="1189b-107">Details of how the method performs the action are implementation-specific.</span></span> <span data-ttu-id="1189b-108">Esse método é herdado [**da \_ ação CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="1189b-108">This method is inherited from [**CIM\_Action**](cim-action.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1189b-109">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="1189b-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1189b-110">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1189b-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1189b-111">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="1189b-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1189b-112">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1189b-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1189b-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1189b-113">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="1189b-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1189b-114">Parameters</span></span>

<span data-ttu-id="1189b-115">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="1189b-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1189b-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1189b-116">Return value</span></span>

<span data-ttu-id="1189b-117">Retorna um valor de 0 (zero) em êxito, 1 (um) se o método não tiver suporte e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="1189b-117">Returns a value of 0 (zero) on success, 1 (one) if the method is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="1189b-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="1189b-118">Remarks</span></span>

<span data-ttu-id="1189b-119">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="1189b-119">WMI does not implement this class.</span></span>

<span data-ttu-id="1189b-120">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="1189b-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1189b-121">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="1189b-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1189b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1189b-122">Requirements</span></span>



| <span data-ttu-id="1189b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1189b-123">Requirement</span></span> | <span data-ttu-id="1189b-124">Valor</span><span class="sxs-lookup"><span data-stu-id="1189b-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1189b-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1189b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1189b-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1189b-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1189b-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1189b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1189b-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1189b-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1189b-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="1189b-129">Namespace</span></span><br/>                | <span data-ttu-id="1189b-130">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="1189b-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1189b-131">MOF</span><span class="sxs-lookup"><span data-stu-id="1189b-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1189b-132"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1189b-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1189b-133">DLL</span><span class="sxs-lookup"><span data-stu-id="1189b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1189b-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1189b-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1189b-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="1189b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1189b-136">\_Directoryaction do CIM</span><span class="sxs-lookup"><span data-stu-id="1189b-136">CIM\_DirectoryAction</span></span>](invoke-method-in-class-cim-directoryaction.md)
</dt> <dt>

[<span data-ttu-id="1189b-137">**\_Directoryaction do CIM**</span><span class="sxs-lookup"><span data-stu-id="1189b-137">**CIM\_DirectoryAction**</span></span>](cim-directoryaction.md)
</dt> </dl>

 

