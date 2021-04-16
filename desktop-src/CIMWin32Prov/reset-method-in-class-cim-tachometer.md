---
description: O método reset da classe do \_ tacômetro CIM solicita uma redefinição do dispositivo lógico.
ms.assetid: c8806511-6796-49e9-bdcd-959e5c5f9da0
ms.tgt_platform: multiple
title: Método Reset da classe CIM_Tachometer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Tachometer.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 368c764ed0f20d8da0e4f08d53e788592809e29d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500838"
---
# <a name="reset-method-of-the-cim_tachometer-class"></a><span data-ttu-id="15336-103">Método Reset da classe do \_ tacômetro CIM</span><span class="sxs-lookup"><span data-stu-id="15336-103">Reset method of the CIM\_Tachometer class</span></span>

<span data-ttu-id="15336-104">O método **Reset** da classe do \_ tacômetro CIM solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="15336-104">The **Reset** method of the CIM\_Tachometer class requests a reset of the logical device.</span></span> <span data-ttu-id="15336-105">Esse método é herdado [**do \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="15336-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="15336-106">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="15336-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="15336-107">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="15336-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="15336-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="15336-108">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="15336-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15336-109">Parameters</span></span>

<span data-ttu-id="15336-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="15336-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="15336-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="15336-111">Return value</span></span>

<span data-ttu-id="15336-112">Retornará 0 (zero) se a solicitação tiver sido executada com êxito, 1 (uma) se a solicitação não tiver suporte e algum outro valor se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="15336-112">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="15336-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="15336-113">Remarks</span></span>

<span data-ttu-id="15336-114">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="15336-114">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="15336-115">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="15336-115">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="15336-116">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="15336-116">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="15336-117">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="15336-117">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="15336-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15336-118">Requirements</span></span>



| <span data-ttu-id="15336-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="15336-119">Requirement</span></span> | <span data-ttu-id="15336-120">Valor</span><span class="sxs-lookup"><span data-stu-id="15336-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="15336-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15336-121">Minimum supported client</span></span><br/> | <span data-ttu-id="15336-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="15336-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="15336-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15336-123">Minimum supported server</span></span><br/> | <span data-ttu-id="15336-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="15336-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="15336-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="15336-125">Namespace</span></span><br/>                | <span data-ttu-id="15336-126">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="15336-126">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="15336-127">MOF</span><span class="sxs-lookup"><span data-stu-id="15336-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15336-128"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="15336-128"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="15336-129">DLL</span><span class="sxs-lookup"><span data-stu-id="15336-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15336-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15336-130"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15336-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="15336-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15336-132">\_Tacômetro CIM</span><span class="sxs-lookup"><span data-stu-id="15336-132">CIM\_Tachometer</span></span>](reset-method-in-class-cim-tachometer.md)
</dt> <dt>

[<span data-ttu-id="15336-133">**\_Tacômetro CIM**</span><span class="sxs-lookup"><span data-stu-id="15336-133">**CIM\_Tachometer**</span></span>](cim-tachometer.md)
</dt> </dl>

 

 




