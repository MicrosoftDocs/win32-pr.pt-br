---
description: O método Invoke da classe CIM \_ VersionCompatibilityCheck avalia uma verificação específica.
ms.assetid: d1ccc248-340e-4277-9696-063e1e2bf915
ms.tgt_platform: multiple
title: Método Invoke da classe CIM_VersionCompatibilityCheck
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VersionCompatibilityCheck.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bccbb6072ae84a238b60247daf6b81cfaa74e608
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826294"
---
# <a name="invoke-method-of-the-cim_versioncompatibilitycheck-class"></a><span data-ttu-id="4de7c-103">Método Invoke da classe CIM \_ VersionCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="4de7c-103">Invoke method of the CIM\_VersionCompatibilityCheck class</span></span>

<span data-ttu-id="4de7c-104">O método **Invoke** da classe [**CIM \_ VersionCompatibilityCheck**](cim-versioncompatibilitycheck.md) avalia uma verificação específica.</span><span class="sxs-lookup"><span data-stu-id="4de7c-104">The **Invoke** method of the [**CIM\_VersionCompatibilityCheck**](cim-versioncompatibilitycheck.md) class evaluates a particular check.</span></span> <span data-ttu-id="4de7c-105">Os detalhes de como o método avalia uma verificação específica em um contexto CIM são descritos pelas subclasses de [**\_ verificação CIM**](cim-check.md) não abstratas.</span><span class="sxs-lookup"><span data-stu-id="4de7c-105">The details of how the method evaluates a particular check in a CIM context are described by the non-abstract [**CIM\_Check**](cim-check.md) subclasses.</span></span> <span data-ttu-id="4de7c-106">Esse método é herdado **da \_ verificação CIM**.</span><span class="sxs-lookup"><span data-stu-id="4de7c-106">This method is inherited from **CIM\_Check**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4de7c-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="4de7c-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4de7c-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4de7c-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4de7c-109">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="4de7c-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4de7c-110">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="4de7c-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4de7c-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4de7c-111">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="4de7c-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4de7c-112">Parameters</span></span>

<span data-ttu-id="4de7c-113">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4de7c-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4de7c-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4de7c-114">Return value</span></span>

<span data-ttu-id="4de7c-115">Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="4de7c-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="4de7c-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="4de7c-116">Remarks</span></span>

<span data-ttu-id="4de7c-117">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="4de7c-117">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="4de7c-118">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="4de7c-118">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="4de7c-119">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="4de7c-119">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4de7c-120">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="4de7c-120">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4de7c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4de7c-121">Requirements</span></span>



| <span data-ttu-id="4de7c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="4de7c-122">Requirement</span></span> | <span data-ttu-id="4de7c-123">Valor</span><span class="sxs-lookup"><span data-stu-id="4de7c-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4de7c-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4de7c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4de7c-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4de7c-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4de7c-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4de7c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4de7c-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4de7c-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4de7c-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="4de7c-128">Namespace</span></span><br/>                | <span data-ttu-id="4de7c-129">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="4de7c-129">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4de7c-130">MOF</span><span class="sxs-lookup"><span data-stu-id="4de7c-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4de7c-131"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4de7c-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4de7c-132">DLL</span><span class="sxs-lookup"><span data-stu-id="4de7c-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4de7c-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4de7c-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4de7c-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="4de7c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4de7c-135">\_VERSIONCOMPATIBILITYCHECK CIM</span><span class="sxs-lookup"><span data-stu-id="4de7c-135">CIM\_VersionCompatibilityCheck</span></span>](invoke-method-in-class-cim-versioncompatibilitycheck.md)
</dt> <dt>

[<span data-ttu-id="4de7c-136">**\_VERSIONCOMPATIBILITYCHECK CIM**</span><span class="sxs-lookup"><span data-stu-id="4de7c-136">**CIM\_VersionCompatibilityCheck**</span></span>](cim-versioncompatibilitycheck.md)
</dt> </dl>

 

