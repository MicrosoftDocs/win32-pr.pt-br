---
description: Método StartService da classe CIM_Service (provedores WMI CIMWin32)-o método StartService coloca o serviço em um estado iniciado.
ms.assetid: 0f2880ed-1643-4211-8684-12493711b1f8
ms.tgt_platform: multiple
title: Método StartService da classe CIM_Service (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6027112323fc14abf4c4a8dc667b921025a5e652
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086164"
---
# <a name="startservice-method-of-the-cim_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="683e7-103">Método StartService da classe CIM_Service (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="683e7-103">StartService method of the CIM_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="683e7-104">O método **StartService** coloca o serviço em um estado iniciado.</span><span class="sxs-lookup"><span data-stu-id="683e7-104">The **StartService** method puts the service in a started state.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="683e7-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="683e7-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="683e7-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="683e7-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="683e7-107">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="683e7-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="683e7-108">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="683e7-108">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="683e7-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="683e7-109">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="683e7-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="683e7-110">Parameters</span></span>

<span data-ttu-id="683e7-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="683e7-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="683e7-112">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="683e7-112">Return value</span></span>

<span data-ttu-id="683e7-113">Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="683e7-113">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="683e7-114">Em uma subclasse, o conjunto de códigos de retorno possíveis pode ser especificado usando um qualificador **ValueMap** no método.</span><span class="sxs-lookup"><span data-stu-id="683e7-114">In a subclass, the set of possible return codes can be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="683e7-115">As cadeias de caracteres nas quais os conteúdos de **ValueMap** são convertidos também podem ser especificadas na subclasse como um qualificador de matriz de **valores** .</span><span class="sxs-lookup"><span data-stu-id="683e7-115">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span>

## <a name="remarks"></a><span data-ttu-id="683e7-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="683e7-116">Remarks</span></span>

<span data-ttu-id="683e7-117">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="683e7-117">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="683e7-118">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="683e7-118">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="683e7-119">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="683e7-119">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="683e7-120">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="683e7-120">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="683e7-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="683e7-121">Requirements</span></span>



| <span data-ttu-id="683e7-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="683e7-122">Requirement</span></span> | <span data-ttu-id="683e7-123">Valor</span><span class="sxs-lookup"><span data-stu-id="683e7-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="683e7-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="683e7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="683e7-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="683e7-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="683e7-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="683e7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="683e7-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="683e7-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="683e7-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="683e7-128">Namespace</span></span><br/>                | <span data-ttu-id="683e7-129">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="683e7-129">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="683e7-130">MOF</span><span class="sxs-lookup"><span data-stu-id="683e7-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="683e7-131"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="683e7-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="683e7-132">DLL</span><span class="sxs-lookup"><span data-stu-id="683e7-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="683e7-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="683e7-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="683e7-134">Consulte também</span><span class="sxs-lookup"><span data-stu-id="683e7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="683e7-135">\_Serviço CIM</span><span class="sxs-lookup"><span data-stu-id="683e7-135">CIM\_Service</span></span>](startservice-method-in-class-cim-service.md)
</dt> <dt>

[<span data-ttu-id="683e7-136">**\_Serviço CIM**</span><span class="sxs-lookup"><span data-stu-id="683e7-136">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

