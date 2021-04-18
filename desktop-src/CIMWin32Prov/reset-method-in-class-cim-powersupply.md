---
description: O método reset da classe CIM \_ powersupply solicita uma redefinição do dispositivo lógico.
ms.assetid: 55fa8408-215b-4e24-a92a-96f44f28c589
ms.tgt_platform: multiple
title: Método Reset da classe CIM_PowerSupply
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PowerSupply.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c1bb483c35c56f8d50a16ff50f5b44e1b9ac52db
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751992"
---
# <a name="reset-method-of-the-cim_powersupply-class"></a><span data-ttu-id="6d1b0-103">Método Reset da classe CIM \_ powersupply</span><span class="sxs-lookup"><span data-stu-id="6d1b0-103">Reset method of the CIM\_PowerSupply class</span></span>

<span data-ttu-id="6d1b0-104">O método **Reset** da classe CIM \_ powersupply solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="6d1b0-104">The **Reset** method of the CIM\_PowerSupply class requests a reset of the logical device.</span></span> <span data-ttu-id="6d1b0-105">Esse método é herdado [**do \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6d1b0-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6d1b0-106">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="6d1b0-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6d1b0-107">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6d1b0-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="6d1b0-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6d1b0-108">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="6d1b0-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d1b0-109">Parameters</span></span>

<span data-ttu-id="6d1b0-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="6d1b0-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6d1b0-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6d1b0-111">Return value</span></span>

<span data-ttu-id="6d1b0-112">Retornará 0 (zero) se a solicitação tiver sido executada com êxito, 1 (zero) se a solicitação não tiver suporte e algum outro valor se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="6d1b0-112">Returns 0 (zero) if the request was successfully executed, 1 (zero) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d1b0-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="6d1b0-113">Remarks</span></span>

<span data-ttu-id="6d1b0-114">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="6d1b0-114">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="6d1b0-115">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="6d1b0-115">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="6d1b0-116">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="6d1b0-116">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6d1b0-117">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="6d1b0-117">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d1b0-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d1b0-118">Requirements</span></span>



| <span data-ttu-id="6d1b0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d1b0-119">Requirement</span></span> | <span data-ttu-id="6d1b0-120">Valor</span><span class="sxs-lookup"><span data-stu-id="6d1b0-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d1b0-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d1b0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6d1b0-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6d1b0-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6d1b0-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d1b0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6d1b0-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6d1b0-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6d1b0-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="6d1b0-125">Namespace</span></span><br/>                | <span data-ttu-id="6d1b0-126">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="6d1b0-126">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6d1b0-127">MOF</span><span class="sxs-lookup"><span data-stu-id="6d1b0-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6d1b0-128"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6d1b0-128"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6d1b0-129">DLL</span><span class="sxs-lookup"><span data-stu-id="6d1b0-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d1b0-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d1b0-130"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d1b0-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="6d1b0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d1b0-132">Fonte de \_ alimentação CIM</span><span class="sxs-lookup"><span data-stu-id="6d1b0-132">CIM\_PowerSupply</span></span>](reset-method-in-class-cim-powersupply.md)
</dt> <dt>

[<span data-ttu-id="6d1b0-133">**Fonte de \_ alimentação CIM**</span><span class="sxs-lookup"><span data-stu-id="6d1b0-133">**CIM\_PowerSupply**</span></span>](cim-powersupply.md)
</dt> </dl>

 

 




