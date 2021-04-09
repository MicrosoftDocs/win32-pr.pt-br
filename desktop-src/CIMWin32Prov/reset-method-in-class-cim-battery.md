---
description: O método reset da classe de \_ bateria CIM solicita uma redefinição do dispositivo lógico.
ms.assetid: 0c51bc15-e2d3-40ff-a6c4-d096ccc3978a
ms.tgt_platform: multiple
title: Método Reset da classe CIM_Battery
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Battery.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: df193b597558cebf5fed924e91b4ddd582398b70
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089231"
---
# <a name="reset-method-of-the-cim_battery-class"></a><span data-ttu-id="b650d-103">Método Reset da \_ classe da bateria CIM</span><span class="sxs-lookup"><span data-stu-id="b650d-103">Reset method of the CIM\_Battery class</span></span>

<span data-ttu-id="b650d-104">O método **Reset** da classe de \_ bateria CIM solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b650d-104">The **Reset** method of the CIM\_Battery class requests a reset of the logical device.</span></span> <span data-ttu-id="b650d-105">Esse método é herdado [**do \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b650d-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b650d-106">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="b650d-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b650d-107">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b650d-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b650d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b650d-108">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="b650d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b650d-109">Parameters</span></span>

<span data-ttu-id="b650d-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="b650d-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b650d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b650d-111">Return value</span></span>

<span data-ttu-id="b650d-112">Retornará 0 (zero) se a solicitação tiver sido executada com êxito, 1 (uma) se a solicitação não tiver suporte e algum outro valor se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="b650d-112">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="b650d-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="b650d-113">Remarks</span></span>

<span data-ttu-id="b650d-114">Atualmente, esse método não é implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="b650d-114">Currently, this method is not implemented by WMI.</span></span> <span data-ttu-id="b650d-115">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="b650d-115">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="b650d-116">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="b650d-116">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b650d-117">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="b650d-117">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b650d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b650d-118">Requirements</span></span>



| <span data-ttu-id="b650d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b650d-119">Requirement</span></span> | <span data-ttu-id="b650d-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b650d-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b650d-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b650d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b650d-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b650d-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b650d-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b650d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b650d-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b650d-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b650d-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="b650d-125">Namespace</span></span><br/>                | <span data-ttu-id="b650d-126">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b650d-126">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b650d-127">MOF</span><span class="sxs-lookup"><span data-stu-id="b650d-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b650d-128"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b650d-128"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b650d-129">DLL</span><span class="sxs-lookup"><span data-stu-id="b650d-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b650d-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b650d-130"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b650d-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="b650d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b650d-132">\_Bateria CIM</span><span class="sxs-lookup"><span data-stu-id="b650d-132">CIM\_Battery</span></span>](reset-method-in-class-cim-battery.md)
</dt> <dt>

[<span data-ttu-id="b650d-133">**\_Bateria CIM**</span><span class="sxs-lookup"><span data-stu-id="b650d-133">**CIM\_Battery**</span></span>](cim-battery.md)
</dt> </dl>

 

 




