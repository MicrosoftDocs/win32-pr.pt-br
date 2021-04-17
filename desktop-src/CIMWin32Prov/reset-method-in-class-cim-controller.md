---
description: O método reset da classe do \_ controlador CIM solicita uma redefinição do dispositivo lógico.
ms.assetid: 98ec2010-4ce1-4aa8-941f-947714de8e7b
ms.tgt_platform: multiple
title: Método Reset da classe CIM_Controller
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Controller.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a1585f153e16e7ffa7133871064f4ff7e1277243
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754391"
---
# <a name="reset-method-of-the-cim_controller-class"></a><span data-ttu-id="833a2-103">Método Reset da classe do \_ controlador CIM</span><span class="sxs-lookup"><span data-stu-id="833a2-103">Reset method of the CIM\_Controller class</span></span>

<span data-ttu-id="833a2-104">O método **Reset** da classe do \_ controlador CIM solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="833a2-104">The **Reset** method of the CIM\_Controller class requests a reset of the logical device.</span></span> <span data-ttu-id="833a2-105">Esse método é herdado [**do \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="833a2-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="833a2-106">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="833a2-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="833a2-107">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="833a2-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="833a2-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="833a2-108">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="833a2-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="833a2-109">Parameters</span></span>

<span data-ttu-id="833a2-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="833a2-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="833a2-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="833a2-111">Return value</span></span>

<span data-ttu-id="833a2-112">Retornará 0 (zero) se a solicitação tiver sido executada com êxito, 1 (uma) se a solicitação não tiver suporte e algum outro valor se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="833a2-112">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="833a2-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="833a2-113">Remarks</span></span>

<span data-ttu-id="833a2-114">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="833a2-114">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="833a2-115">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="833a2-115">To use this method, you must implement it in your own provider.</span></span> <span data-ttu-id="833a2-116">Para obter mais informações, consulte [CREATING WMI Providers](/windows/desktop/WmiSdk/creating-wmi-providers).</span><span class="sxs-lookup"><span data-stu-id="833a2-116">For more information, see [Creating WMI Providers](/windows/desktop/WmiSdk/creating-wmi-providers).</span></span>

<span data-ttu-id="833a2-117">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="833a2-117">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="833a2-118">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="833a2-118">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="833a2-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="833a2-119">Requirements</span></span>



| <span data-ttu-id="833a2-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="833a2-120">Requirement</span></span> | <span data-ttu-id="833a2-121">Valor</span><span class="sxs-lookup"><span data-stu-id="833a2-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="833a2-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="833a2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="833a2-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="833a2-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="833a2-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="833a2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="833a2-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="833a2-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="833a2-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="833a2-126">Namespace</span></span><br/>                | <span data-ttu-id="833a2-127">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="833a2-127">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="833a2-128">MOF</span><span class="sxs-lookup"><span data-stu-id="833a2-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="833a2-129"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="833a2-129"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="833a2-130">DLL</span><span class="sxs-lookup"><span data-stu-id="833a2-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="833a2-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="833a2-131"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="833a2-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="833a2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="833a2-133">\_Controlador CIM</span><span class="sxs-lookup"><span data-stu-id="833a2-133">CIM\_Controller</span></span>](reset-method-in-class-cim-controller.md)
</dt> <dt>

[<span data-ttu-id="833a2-134">**\_Controlador CIM**</span><span class="sxs-lookup"><span data-stu-id="833a2-134">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> </dl>

 

