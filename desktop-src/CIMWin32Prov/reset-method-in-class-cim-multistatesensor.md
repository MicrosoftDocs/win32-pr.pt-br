---
description: Método Reset da classe CIM_MultiStateSensor – o método reset solicita uma redefinição do dispositivo lógico. Esse método é herdado do \_ LOGICALDEVICE CIM.
ms.assetid: 51234db3-496a-4750-a185-84a5945228b9
ms.tgt_platform: multiple
title: Método Reset da classe CIM_MultiStateSensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MultiStateSensor.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 41694086537fac64cc5c6eb3019a079649c1b248
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096894"
---
# <a name="reset-method-of-the-cim_multistatesensor-class"></a><span data-ttu-id="bd0ff-104">Método Reset da classe CIM \_ MultiStateSensor</span><span class="sxs-lookup"><span data-stu-id="bd0ff-104">Reset method of the CIM\_MultiStateSensor class</span></span>

<span data-ttu-id="bd0ff-105">O método **Reset** solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="bd0ff-105">The **Reset** method requests a reset of the logical device.</span></span> <span data-ttu-id="bd0ff-106">Esse método é herdado [**do \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bd0ff-106">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bd0ff-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="bd0ff-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="bd0ff-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="bd0ff-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="bd0ff-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bd0ff-109">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="bd0ff-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bd0ff-110">Parameters</span></span>

<span data-ttu-id="bd0ff-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="bd0ff-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bd0ff-112">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="bd0ff-112">Return value</span></span>

<span data-ttu-id="bd0ff-113">Retornará 0 (zero) se a solicitação tiver sido executada com êxito, 1 (uma) se a solicitação não tiver suporte e algum outro valor se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="bd0ff-113">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd0ff-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="bd0ff-114">Remarks</span></span>

<span data-ttu-id="bd0ff-115">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="bd0ff-115">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="bd0ff-116">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="bd0ff-116">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="bd0ff-117">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="bd0ff-117">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="bd0ff-118">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="bd0ff-118">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd0ff-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd0ff-119">Requirements</span></span>



| <span data-ttu-id="bd0ff-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd0ff-120">Requirement</span></span> | <span data-ttu-id="bd0ff-121">Valor</span><span class="sxs-lookup"><span data-stu-id="bd0ff-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd0ff-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd0ff-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bd0ff-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bd0ff-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bd0ff-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd0ff-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bd0ff-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bd0ff-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bd0ff-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="bd0ff-126">Namespace</span></span><br/>                | <span data-ttu-id="bd0ff-127">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="bd0ff-127">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bd0ff-128">MOF</span><span class="sxs-lookup"><span data-stu-id="bd0ff-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bd0ff-129"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bd0ff-129"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bd0ff-130">DLL</span><span class="sxs-lookup"><span data-stu-id="bd0ff-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd0ff-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd0ff-131"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd0ff-132">Consulte também</span><span class="sxs-lookup"><span data-stu-id="bd0ff-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd0ff-133">\_MULTISTATESENSOR CIM</span><span class="sxs-lookup"><span data-stu-id="bd0ff-133">CIM\_MultiStateSensor</span></span>](reset-method-in-class-cim-multistatesensor.md)
</dt> <dt>

[<span data-ttu-id="bd0ff-134">**\_MULTISTATESENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="bd0ff-134">**CIM\_MultiStateSensor**</span></span>](cim-multistatesensor.md)
</dt> </dl>

 

 




