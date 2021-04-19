---
description: O método Invoke da classe CIM \_ DiskSpaceCheck avalia uma verificação específica. Os detalhes de como o método avalia uma verificação específica em um contexto CIM são descritos pela subclasse de verificação CIM não abstrata \_ .
ms.assetid: 1f06b0c4-3f39-4a6f-9205-2aa309fb06bb
ms.tgt_platform: multiple
title: Método Invoke da classe CIM_DiskSpaceCheck
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DiskSpaceCheck.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bbcef752bf412ea255891dd0f5abdf7563f0e078
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811157"
---
# <a name="invoke-method-of-the-cim_diskspacecheck-class"></a><span data-ttu-id="3abeb-104">Método Invoke da classe CIM \_ DiskSpaceCheck</span><span class="sxs-lookup"><span data-stu-id="3abeb-104">Invoke method of the CIM\_DiskSpaceCheck class</span></span>

<span data-ttu-id="3abeb-105">O método **Invoke** da classe [**CIM \_ DiskSpaceCheck**](cim-diskspacecheck.md) avalia uma verificação específica.</span><span class="sxs-lookup"><span data-stu-id="3abeb-105">The **Invoke** method of the [**CIM\_DiskSpaceCheck**](cim-diskspacecheck.md) class evaluates a particular check.</span></span> <span data-ttu-id="3abeb-106">Os detalhes de como o método avalia uma verificação específica em um contexto CIM são descritos pela subclasse de [**\_ verificação CIM**](cim-check.md) não abstrata.</span><span class="sxs-lookup"><span data-stu-id="3abeb-106">The details of how the method evaluates a particular check in a CIM context is described by the non-abstract [**CIM\_Check**](cim-check.md) subclass.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3abeb-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="3abeb-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3abeb-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3abeb-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3abeb-109">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="3abeb-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3abeb-110">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="3abeb-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3abeb-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3abeb-111">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="3abeb-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3abeb-112">Parameters</span></span>

<span data-ttu-id="3abeb-113">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="3abeb-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3abeb-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3abeb-114">Return value</span></span>

<span data-ttu-id="3abeb-115">Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="3abeb-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="3abeb-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="3abeb-116">Remarks</span></span>

<span data-ttu-id="3abeb-117">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="3abeb-117">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="3abeb-118">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="3abeb-118">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="3abeb-119">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="3abeb-119">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3abeb-120">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="3abeb-120">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3abeb-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3abeb-121">Requirements</span></span>



| <span data-ttu-id="3abeb-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3abeb-122">Requirement</span></span> | <span data-ttu-id="3abeb-123">Valor</span><span class="sxs-lookup"><span data-stu-id="3abeb-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3abeb-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3abeb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3abeb-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3abeb-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3abeb-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3abeb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3abeb-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3abeb-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3abeb-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="3abeb-128">Namespace</span></span><br/>                | <span data-ttu-id="3abeb-129">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3abeb-129">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3abeb-130">MOF</span><span class="sxs-lookup"><span data-stu-id="3abeb-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3abeb-131"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3abeb-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3abeb-132">DLL</span><span class="sxs-lookup"><span data-stu-id="3abeb-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3abeb-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3abeb-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3abeb-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="3abeb-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3abeb-135">\_DISKSPACECHECK CIM</span><span class="sxs-lookup"><span data-stu-id="3abeb-135">CIM\_DiskSpaceCheck</span></span>](invoke-method-in-class-cim-diskspacecheck.md)
</dt> <dt>

[<span data-ttu-id="3abeb-136">**\_DISKSPACECHECK CIM**</span><span class="sxs-lookup"><span data-stu-id="3abeb-136">**CIM\_DiskSpaceCheck**</span></span>](cim-diskspacecheck.md)
</dt> </dl>

 

