---
description: O método reset da classe CIM \_ TapeDrive solicita uma redefinição do dispositivo lógico.
ms.assetid: 48097e0d-7986-46b9-884d-7534f3848dd7
ms.tgt_platform: multiple
title: Método Reset da classe CIM_TapeDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TapeDrive.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e5fd76d038e743ba5148f4c82555d50f0a5dde5d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826641"
---
# <a name="reset-method-of-the-cim_tapedrive-class"></a><span data-ttu-id="98b90-103">Método Reset da classe CIM \_ TapeDrive</span><span class="sxs-lookup"><span data-stu-id="98b90-103">Reset method of the CIM\_TapeDrive class</span></span>

<span data-ttu-id="98b90-104">O método **Reset** da classe CIM \_ TapeDrive solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="98b90-104">The **Reset** method of the CIM\_TapeDrive class requests a reset of the logical device.</span></span> <span data-ttu-id="98b90-105">Esse método é herdado [**do \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="98b90-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="98b90-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="98b90-106">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="98b90-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="98b90-107">Parameters</span></span>

<span data-ttu-id="98b90-108">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="98b90-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="98b90-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="98b90-109">Return value</span></span>

<span data-ttu-id="98b90-110">Retornará 0 (zero) se a solicitação tiver sido executada com êxito, 1 (uma) se a solicitação não tiver suporte e algum outro valor se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="98b90-110">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="98b90-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="98b90-111">Remarks</span></span>

<span data-ttu-id="98b90-112">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="98b90-112">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="98b90-113">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="98b90-113">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="98b90-114">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="98b90-114">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="98b90-115">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="98b90-115">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="98b90-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98b90-116">Requirements</span></span>



| <span data-ttu-id="98b90-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="98b90-117">Requirement</span></span> | <span data-ttu-id="98b90-118">Valor</span><span class="sxs-lookup"><span data-stu-id="98b90-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="98b90-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="98b90-119">Minimum supported client</span></span><br/> | <span data-ttu-id="98b90-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="98b90-120">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="98b90-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="98b90-121">Minimum supported server</span></span><br/> | <span data-ttu-id="98b90-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="98b90-122">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="98b90-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="98b90-123">Namespace</span></span><br/>                | <span data-ttu-id="98b90-124">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="98b90-124">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="98b90-125">MOF</span><span class="sxs-lookup"><span data-stu-id="98b90-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="98b90-126"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="98b90-126"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="98b90-127">DLL</span><span class="sxs-lookup"><span data-stu-id="98b90-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98b90-128"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98b90-128"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98b90-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="98b90-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98b90-130">\_TAPEDRIVE CIM</span><span class="sxs-lookup"><span data-stu-id="98b90-130">CIM\_TapeDrive</span></span>](reset-method-in-class-cim-tapedrive.md)
</dt> <dt>

[<span data-ttu-id="98b90-131">**\_TAPEDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="98b90-131">**CIM\_TapeDrive**</span></span>](cim-tapedrive.md)
</dt> </dl>

 

 




