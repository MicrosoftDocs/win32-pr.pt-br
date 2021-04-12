---
description: O método reset da classe CIM \_ ProtectedSpaceExtent solicita uma redefinição do dispositivo lógico.
ms.assetid: 601e6b0d-4f3c-4a99-aec1-1a769213cf6e
ms.tgt_platform: multiple
title: Método Reset da classe CIM_ProtectedSpaceExtent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProtectedSpaceExtent.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a89d234fc4a134d81485f0e507873fc3cc111305
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089614"
---
# <a name="reset-method-of-the-cim_protectedspaceextent-class"></a><span data-ttu-id="df536-103">Método Reset da classe CIM \_ ProtectedSpaceExtent</span><span class="sxs-lookup"><span data-stu-id="df536-103">Reset method of the CIM\_ProtectedSpaceExtent class</span></span>

<span data-ttu-id="df536-104">O método **Reset** da classe CIM \_ ProtectedSpaceExtent solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="df536-104">The **Reset** method of the CIM\_ProtectedSpaceExtent class requests a reset of the logical device.</span></span> <span data-ttu-id="df536-105">Esse método é herdado [**do \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="df536-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="df536-106">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="df536-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="df536-107">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="df536-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="df536-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="df536-108">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="df536-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="df536-109">Parameters</span></span>

<span data-ttu-id="df536-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="df536-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="df536-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="df536-111">Return value</span></span>

<span data-ttu-id="df536-112">Retornará 0 (zero) se a solicitação tiver sido executada com êxito, 1 (uma) se a solicitação não tiver suporte e algum outro valor se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="df536-112">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="df536-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="df536-113">Remarks</span></span>

<span data-ttu-id="df536-114">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="df536-114">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="df536-115">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="df536-115">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="df536-116">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="df536-116">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="df536-117">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="df536-117">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="df536-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df536-118">Requirements</span></span>



| <span data-ttu-id="df536-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="df536-119">Requirement</span></span> | <span data-ttu-id="df536-120">Valor</span><span class="sxs-lookup"><span data-stu-id="df536-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="df536-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df536-121">Minimum supported client</span></span><br/> | <span data-ttu-id="df536-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="df536-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="df536-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df536-123">Minimum supported server</span></span><br/> | <span data-ttu-id="df536-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="df536-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="df536-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="df536-125">Namespace</span></span><br/>                | <span data-ttu-id="df536-126">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="df536-126">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="df536-127">MOF</span><span class="sxs-lookup"><span data-stu-id="df536-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="df536-128"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="df536-128"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="df536-129">DLL</span><span class="sxs-lookup"><span data-stu-id="df536-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df536-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df536-130"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df536-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="df536-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df536-132">\_PROTECTEDSPACEEXTENT CIM</span><span class="sxs-lookup"><span data-stu-id="df536-132">CIM\_ProtectedSpaceExtent</span></span>](reset-method-in-class-cim-protectedspaceextent.md)
</dt> <dt>

[<span data-ttu-id="df536-133">**\_PROTECTEDSPACEEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="df536-133">**CIM\_ProtectedSpaceExtent**</span></span>](cim-protectedspaceextent.md)
</dt> </dl>

 

 




