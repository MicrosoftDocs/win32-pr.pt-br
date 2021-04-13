---
description: O método reset da classe CIM \_ sensor solicita uma redefinição do dispositivo lógico.
ms.assetid: c764da9a-561b-4a0b-9cdf-6b4af50f1df0
ms.tgt_platform: multiple
title: Método Reset da classe CIM_TemperatureSensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TemperatureSensor.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 050836529b95d610c25902eee9b36d4720dc639e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370370"
---
# <a name="reset-method-of-the-cim_temperaturesensor-class"></a><span data-ttu-id="4f990-103">Método Reset da classe CIM \_ sensor</span><span class="sxs-lookup"><span data-stu-id="4f990-103">Reset method of the CIM\_TemperatureSensor class</span></span>

<span data-ttu-id="4f990-104">O método **Reset** da classe CIM \_ sensor solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="4f990-104">The **Reset** method of the CIM\_TemperatureSensor class requests a reset of the logical device.</span></span> <span data-ttu-id="4f990-105">Esse método é herdado [**do \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4f990-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4f990-106">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="4f990-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4f990-107">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4f990-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="4f990-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4f990-108">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="4f990-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4f990-109">Parameters</span></span>

<span data-ttu-id="4f990-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4f990-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4f990-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4f990-111">Return value</span></span>

<span data-ttu-id="4f990-112">Retornará 0 (zero) se a solicitação tiver sido executada com êxito, 1 (uma) se a solicitação não tiver suporte e algum outro valor se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="4f990-112">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f990-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="4f990-113">Remarks</span></span>

<span data-ttu-id="4f990-114">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="4f990-114">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="4f990-115">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="4f990-115">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="4f990-116">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="4f990-116">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4f990-117">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="4f990-117">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f990-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f990-118">Requirements</span></span>



| <span data-ttu-id="4f990-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f990-119">Requirement</span></span> | <span data-ttu-id="4f990-120">Valor</span><span class="sxs-lookup"><span data-stu-id="4f990-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f990-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f990-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4f990-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4f990-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4f990-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f990-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4f990-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4f990-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4f990-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="4f990-125">Namespace</span></span><br/>                | <span data-ttu-id="4f990-126">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="4f990-126">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4f990-127">MOF</span><span class="sxs-lookup"><span data-stu-id="4f990-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4f990-128"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4f990-128"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4f990-129">DLL</span><span class="sxs-lookup"><span data-stu-id="4f990-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f990-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f990-130"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f990-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="4f990-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f990-132">\_Sensor CIM</span><span class="sxs-lookup"><span data-stu-id="4f990-132">CIM\_TemperatureSensor</span></span>](reset-method-in-class-cim-temperaturesensor.md)
</dt> <dt>

[<span data-ttu-id="4f990-133">**\_Sensor CIM**</span><span class="sxs-lookup"><span data-stu-id="4f990-133">**CIM\_TemperatureSensor**</span></span>](cim-temperaturesensor.md)
</dt> </dl>

 

 




