---
description: O método reset da classe CIM \_ PCVideoController solicita uma redefinição do dispositivo lógico.
ms.assetid: 0dbed7af-6c7a-4bbb-b1ae-d768d2f88697
ms.tgt_platform: multiple
title: Método Reset da classe CIM_PCVideoController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PCVideoController.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b156f4c440e98ebc51618ca8350696f23b55074b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754819"
---
# <a name="reset-method-of-the-cim_pcvideocontroller-class"></a><span data-ttu-id="e34a8-103">Método Reset da classe CIM \_ PCVideoController</span><span class="sxs-lookup"><span data-stu-id="e34a8-103">Reset method of the CIM\_PCVideoController class</span></span>

<span data-ttu-id="e34a8-104">O método **Reset** da classe CIM \_ PCVideoController solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e34a8-104">The **Reset** method of the CIM\_PCVideoController class requests a reset of the logical device.</span></span> <span data-ttu-id="e34a8-105">Esse método é herdado [**do \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e34a8-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e34a8-106">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="e34a8-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e34a8-107">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e34a8-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="e34a8-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e34a8-108">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="e34a8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e34a8-109">Parameters</span></span>

<span data-ttu-id="e34a8-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e34a8-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e34a8-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e34a8-111">Return value</span></span>

<span data-ttu-id="e34a8-112">Retornará 0 (zero) se a solicitação tiver sido executada com êxito, 1 (uma) se a solicitação não tiver suporte e algum outro valor se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="e34a8-112">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="e34a8-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="e34a8-113">Remarks</span></span>

<span data-ttu-id="e34a8-114">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="e34a8-114">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="e34a8-115">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="e34a8-115">To use this method, you must implement it in your own provider.</span></span> <span data-ttu-id="e34a8-116">Para classes WMI derivadas do [**CIM \_ PCVideoController**](cim-pcvideocontroller.md), consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="e34a8-116">For WMI classes derived from [**CIM\_PCVideoController**](cim-pcvideocontroller.md), see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="e34a8-117">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="e34a8-117">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e34a8-118">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="e34a8-118">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e34a8-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e34a8-119">Requirements</span></span>



| <span data-ttu-id="e34a8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e34a8-120">Requirement</span></span> | <span data-ttu-id="e34a8-121">Valor</span><span class="sxs-lookup"><span data-stu-id="e34a8-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e34a8-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e34a8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e34a8-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e34a8-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e34a8-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e34a8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e34a8-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e34a8-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e34a8-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="e34a8-126">Namespace</span></span><br/>                | <span data-ttu-id="e34a8-127">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e34a8-127">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e34a8-128">MOF</span><span class="sxs-lookup"><span data-stu-id="e34a8-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e34a8-129"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e34a8-129"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e34a8-130">DLL</span><span class="sxs-lookup"><span data-stu-id="e34a8-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e34a8-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e34a8-131"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e34a8-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="e34a8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e34a8-133">\_PCVIDEOCONTROLLER CIM</span><span class="sxs-lookup"><span data-stu-id="e34a8-133">CIM\_PCVideoController</span></span>](reset-method-in-class-cim-pcvideocontroller.md)
</dt> <dt>

[<span data-ttu-id="e34a8-134">**\_PCVIDEOCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="e34a8-134">**CIM\_PCVideoController**</span></span>](cim-pcvideocontroller.md)
</dt> </dl>

 

 




