---
description: O método Invoke da \_ classe fileaction do CIM usa uma ação específica. Os detalhes de como o método executa a ação são específicos da implementação. Esse método é herdado da \_ ação CIM.
ms.assetid: f7514d67-4141-4d1a-bdfd-83aa062291aa
ms.tgt_platform: multiple
title: Método Invoke da classe CIM_FileAction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FileAction.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b1d0a877936a27a681a20e5ffd73da9dda77dcf4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104163988"
---
# <a name="invoke-method-of-the-cim_fileaction-class"></a><span data-ttu-id="28a87-105">Método Invoke da \_ classe fileaction do CIM</span><span class="sxs-lookup"><span data-stu-id="28a87-105">Invoke method of the CIM\_FileAction class</span></span>

<span data-ttu-id="28a87-106">O método **Invoke** da classe [**\_ fileaction do CIM**](cim-fileaction.md) usa uma ação específica.</span><span class="sxs-lookup"><span data-stu-id="28a87-106">The **Invoke** method of the [**CIM\_FileAction**](cim-fileaction.md) class takes a particular action.</span></span> <span data-ttu-id="28a87-107">Os detalhes de como o método executa a ação são específicos da implementação.</span><span class="sxs-lookup"><span data-stu-id="28a87-107">Details of how the method performs the action are implementation specific.</span></span> <span data-ttu-id="28a87-108">Esse método é herdado [**da \_ ação CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="28a87-108">This method is inherited from [**CIM\_Action**](cim-action.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="28a87-109">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="28a87-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="28a87-110">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="28a87-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="28a87-111">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="28a87-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="28a87-112">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="28a87-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="28a87-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="28a87-113">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="28a87-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="28a87-114">Parameters</span></span>

<span data-ttu-id="28a87-115">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="28a87-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="28a87-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="28a87-116">Return value</span></span>

<span data-ttu-id="28a87-117">Retorna um valor de 0 (zero) em êxito, 1 (um) se o método não tiver suporte e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="28a87-117">Returns a value of 0 (zero) on success, 1 (one) if the method is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="28a87-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="28a87-118">Remarks</span></span>

<span data-ttu-id="28a87-119">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="28a87-119">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="28a87-120">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="28a87-120">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="28a87-121">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="28a87-121">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="28a87-122">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="28a87-122">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="28a87-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28a87-123">Requirements</span></span>



| <span data-ttu-id="28a87-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="28a87-124">Requirement</span></span> | <span data-ttu-id="28a87-125">Valor</span><span class="sxs-lookup"><span data-stu-id="28a87-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="28a87-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="28a87-126">Minimum supported client</span></span><br/> | <span data-ttu-id="28a87-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="28a87-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="28a87-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="28a87-128">Minimum supported server</span></span><br/> | <span data-ttu-id="28a87-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="28a87-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="28a87-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="28a87-130">Namespace</span></span><br/>                | <span data-ttu-id="28a87-131">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="28a87-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="28a87-132">MOF</span><span class="sxs-lookup"><span data-stu-id="28a87-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="28a87-133"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="28a87-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="28a87-134">DLL</span><span class="sxs-lookup"><span data-stu-id="28a87-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28a87-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28a87-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28a87-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="28a87-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28a87-137">\_Arquivo de arquivos CIM</span><span class="sxs-lookup"><span data-stu-id="28a87-137">CIM\_FileAction</span></span>](invoke-method-in-class-cim-fileaction.md)
</dt> <dt>

[<span data-ttu-id="28a87-138">**\_Arquivo de arquivos CIM**</span><span class="sxs-lookup"><span data-stu-id="28a87-138">**CIM\_FileAction**</span></span>](cim-fileaction.md)
</dt> </dl>

 

