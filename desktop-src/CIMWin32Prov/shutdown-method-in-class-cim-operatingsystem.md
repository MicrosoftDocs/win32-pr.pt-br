---
description: O método Shutdown solicita um desligamento do sistema operacional.
ms.assetid: f2a2a98b-2f4f-4aa1-9f54-515660273c8d
ms.tgt_platform: multiple
title: Método Shutdown da classe CIM_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OperatingSystem.Shutdown
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 78a11f325b8682b0024ff281a48989b837d3073a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826148"
---
# <a name="shutdown-method-of-the-cim_operatingsystem-class"></a><span data-ttu-id="f8f3b-103">Método Shutdown da classe CIM \_ OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="f8f3b-103">Shutdown method of the CIM\_OperatingSystem class</span></span>

<span data-ttu-id="f8f3b-104">O método **Shutdown** solicita um desligamento do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="f8f3b-104">The **Shutdown** method requests a shutdown of the operating system.</span></span> <span data-ttu-id="f8f3b-105">A implementação ou subclasse do sistema operacional pode estabelecer dependências entre os métodos de **desligamento** e [**reinicialização**](reboot-method-in-class-cim-operatingsystem.md) .</span><span class="sxs-lookup"><span data-stu-id="f8f3b-105">The implementation or subclass of the operating system can establish dependencies between the **Shutdown** and [**Reboot**](reboot-method-in-class-cim-operatingsystem.md) methods.</span></span> <span data-ttu-id="f8f3b-106">Por exemplo, recursos mais sofisticados podem ser fornecidos, como um desligamento e reinicialização agendados.</span><span class="sxs-lookup"><span data-stu-id="f8f3b-106">For example, more sophisticated capabilities can be provided, such as a scheduled shutdown and reboot.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f8f3b-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="f8f3b-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f8f3b-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f8f3b-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f8f3b-109">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="f8f3b-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f8f3b-110">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f8f3b-110">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f8f3b-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f8f3b-111">Syntax</span></span>


```mof
uint32 Shutdown();
```



## <a name="parameters"></a><span data-ttu-id="f8f3b-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f8f3b-112">Parameters</span></span>

<span data-ttu-id="f8f3b-113">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f8f3b-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f8f3b-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f8f3b-114">Return value</span></span>

<span data-ttu-id="f8f3b-115">Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="f8f3b-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8f3b-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="f8f3b-116">Remarks</span></span>

<span data-ttu-id="f8f3b-117">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="f8f3b-117">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="f8f3b-118">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="f8f3b-118">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="f8f3b-119">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="f8f3b-119">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f8f3b-120">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="f8f3b-120">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8f3b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8f3b-121">Requirements</span></span>



| <span data-ttu-id="f8f3b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8f3b-122">Requirement</span></span> | <span data-ttu-id="f8f3b-123">Valor</span><span class="sxs-lookup"><span data-stu-id="f8f3b-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8f3b-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f8f3b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f8f3b-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f8f3b-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f8f3b-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f8f3b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f8f3b-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f8f3b-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f8f3b-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="f8f3b-128">Namespace</span></span><br/>                | <span data-ttu-id="f8f3b-129">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f8f3b-129">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f8f3b-130">MOF</span><span class="sxs-lookup"><span data-stu-id="f8f3b-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f8f3b-131"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f8f3b-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f8f3b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f8f3b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8f3b-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8f3b-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8f3b-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="f8f3b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8f3b-135">Sistema \_ operacional CIM</span><span class="sxs-lookup"><span data-stu-id="f8f3b-135">CIM\_OperatingSystem</span></span>](shutdown-method-in-class-cim-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="f8f3b-136">**Sistema \_ operacional CIM**</span><span class="sxs-lookup"><span data-stu-id="f8f3b-136">**CIM\_OperatingSystem**</span></span>](cim-operatingsystem.md)
</dt> </dl>

 

