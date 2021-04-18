---
description: O método reboot solicita uma reinicialização do sistema operacional.
ms.assetid: 2ce766dd-51a4-4ffb-a45a-40399f1110f6
ms.tgt_platform: multiple
title: Método reboot da classe CIM_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OperatingSystem.Reboot
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e498dd16372503b23aa56471224faf4d5d0ff012
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756248"
---
# <a name="reboot-method-of-the-cim_operatingsystem-class"></a><span data-ttu-id="a3d8b-103">Método reboot da \_ classe CIM OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="a3d8b-103">Reboot method of the CIM\_OperatingSystem class</span></span>

<span data-ttu-id="a3d8b-104">O método **reboot** solicita uma reinicialização do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a3d8b-104">The **Reboot** method requests a reboot of the operating system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a3d8b-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="a3d8b-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a3d8b-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a3d8b-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a3d8b-107">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="a3d8b-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a3d8b-108">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a3d8b-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a3d8b-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a3d8b-109">Syntax</span></span>


```mof
uint32 Reboot();
```



## <a name="parameters"></a><span data-ttu-id="a3d8b-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a3d8b-110">Parameters</span></span>

<span data-ttu-id="a3d8b-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="a3d8b-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a3d8b-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a3d8b-112">Return value</span></span>

<span data-ttu-id="a3d8b-113">Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="a3d8b-113">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3d8b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a3d8b-114">Remarks</span></span>

<span data-ttu-id="a3d8b-115">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="a3d8b-115">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="a3d8b-116">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="a3d8b-116">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="a3d8b-117">Para classes WMI que são derivadas do [**sistema \_ operacional CIM**](cim-operatingsystem.md), consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a3d8b-117">For WMI classes that are derived from [**CIM\_OperatingSystem**](cim-operatingsystem.md), see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="a3d8b-118">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="a3d8b-118">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a3d8b-119">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="a3d8b-119">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

<span data-ttu-id="a3d8b-120">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="a3d8b-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a3d8b-121">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="a3d8b-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3d8b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3d8b-122">Requirements</span></span>



| <span data-ttu-id="a3d8b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3d8b-123">Requirement</span></span> | <span data-ttu-id="a3d8b-124">Valor</span><span class="sxs-lookup"><span data-stu-id="a3d8b-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3d8b-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a3d8b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a3d8b-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a3d8b-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a3d8b-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a3d8b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a3d8b-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a3d8b-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a3d8b-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="a3d8b-129">Namespace</span></span><br/>                | <span data-ttu-id="a3d8b-130">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a3d8b-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a3d8b-131">MOF</span><span class="sxs-lookup"><span data-stu-id="a3d8b-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a3d8b-132"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a3d8b-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a3d8b-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a3d8b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3d8b-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3d8b-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3d8b-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="a3d8b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3d8b-136">Sistema \_ operacional CIM</span><span class="sxs-lookup"><span data-stu-id="a3d8b-136">CIM\_OperatingSystem</span></span>](reboot-method-in-class-cim-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="a3d8b-137">**Sistema \_ operacional CIM**</span><span class="sxs-lookup"><span data-stu-id="a3d8b-137">**CIM\_OperatingSystem**</span></span>](cim-operatingsystem.md)
</dt> </dl>

 

