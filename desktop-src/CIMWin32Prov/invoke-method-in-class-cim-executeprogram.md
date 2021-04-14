---
description: O método Invoke da classe CIM \_ ExecuteProgram executa uma ação específica. Os detalhes de como o método executa a ação são específicos da implementação. Esse método é herdado da \_ ação CIM.
ms.assetid: 14a12fae-14a6-412a-a778-8dd34a5843d1
ms.tgt_platform: multiple
title: Método Invoke da classe CIM_ExecuteProgram
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ExecuteProgram.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bdf9a4edb78bb47c0354991d161339099e4dc49f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370408"
---
# <a name="invoke-method-of-the-cim_executeprogram-class"></a><span data-ttu-id="1bc7f-105">Método Invoke da classe CIM \_ ExecuteProgram</span><span class="sxs-lookup"><span data-stu-id="1bc7f-105">Invoke method of the CIM\_ExecuteProgram class</span></span>

<span data-ttu-id="1bc7f-106">O método **Invoke** da classe [**CIM \_ ExecuteProgram**](cim-executeprogram.md) executa uma ação específica.</span><span class="sxs-lookup"><span data-stu-id="1bc7f-106">The **Invoke** method of the [**CIM\_ExecuteProgram**](cim-executeprogram.md) class takes a particular action.</span></span> <span data-ttu-id="1bc7f-107">Os detalhes de como o método executa a ação são específicos da implementação.</span><span class="sxs-lookup"><span data-stu-id="1bc7f-107">The details of how the method performs the action are implementation specific.</span></span> <span data-ttu-id="1bc7f-108">Esse método é herdado [**da \_ ação CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="1bc7f-108">This method is inherited from [**CIM\_Action**](cim-action.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1bc7f-109">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="1bc7f-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1bc7f-110">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1bc7f-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1bc7f-111">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="1bc7f-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1bc7f-112">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1bc7f-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1bc7f-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1bc7f-113">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="1bc7f-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1bc7f-114">Parameters</span></span>

<span data-ttu-id="1bc7f-115">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="1bc7f-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1bc7f-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1bc7f-116">Return value</span></span>

<span data-ttu-id="1bc7f-117">Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="1bc7f-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="1bc7f-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="1bc7f-118">Remarks</span></span>

<span data-ttu-id="1bc7f-119">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="1bc7f-119">WMI does not implement this class.</span></span>

<span data-ttu-id="1bc7f-120">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="1bc7f-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1bc7f-121">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="1bc7f-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bc7f-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1bc7f-122">Requirements</span></span>



| <span data-ttu-id="1bc7f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1bc7f-123">Requirement</span></span> | <span data-ttu-id="1bc7f-124">Valor</span><span class="sxs-lookup"><span data-stu-id="1bc7f-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1bc7f-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1bc7f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1bc7f-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1bc7f-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1bc7f-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1bc7f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1bc7f-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1bc7f-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1bc7f-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="1bc7f-129">Namespace</span></span><br/>                | <span data-ttu-id="1bc7f-130">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="1bc7f-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1bc7f-131">MOF</span><span class="sxs-lookup"><span data-stu-id="1bc7f-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1bc7f-132"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1bc7f-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1bc7f-133">DLL</span><span class="sxs-lookup"><span data-stu-id="1bc7f-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1bc7f-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1bc7f-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1bc7f-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="1bc7f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bc7f-136">\_EXECUTEPROGRAM CIM</span><span class="sxs-lookup"><span data-stu-id="1bc7f-136">CIM\_ExecuteProgram</span></span>](invoke-method-in-class-cim-executeprogram.md)
</dt> <dt>

[<span data-ttu-id="1bc7f-137">**\_EXECUTEPROGRAM CIM**</span><span class="sxs-lookup"><span data-stu-id="1bc7f-137">**CIM\_ExecuteProgram**</span></span>](cim-executeprogram.md)
</dt> </dl>

 

