---
description: Solicita uma redefinição do dispositivo lógico. Esse método é herdado do \_ LOGICALDEVICE CIM.
ms.assetid: 2ad40b35-608f-4918-ac66-e3dc53ebe0bb
ms.tgt_platform: multiple
title: Método Reset da classe Win32_DiskPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DiskPartition.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: eb316a72b801a696b5c5f76376036af75a8beb54
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089466"
---
# <a name="reset-method-of-the-win32_diskpartition-class"></a><span data-ttu-id="c87bd-104">Método Reset da classe Win32 \_ DiskPartition</span><span class="sxs-lookup"><span data-stu-id="c87bd-104">Reset method of the Win32\_DiskPartition class</span></span>

<span data-ttu-id="c87bd-105">Solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c87bd-105">Requests a reset of the logical device.</span></span> <span data-ttu-id="c87bd-106">Esse método é herdado [**do \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c87bd-106">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c87bd-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="c87bd-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c87bd-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c87bd-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c87bd-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c87bd-109">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="c87bd-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c87bd-110">Parameters</span></span>

<span data-ttu-id="c87bd-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c87bd-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c87bd-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c87bd-112">Return value</span></span>

<span data-ttu-id="c87bd-113">Retornará 0 (zero) se a solicitação tiver sido executada com êxito, 1 (uma) se a solicitação não tiver suporte e algum outro valor se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="c87bd-113">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="c87bd-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c87bd-114">Remarks</span></span>

<span data-ttu-id="c87bd-115">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="c87bd-115">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="c87bd-116">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="c87bd-116">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="c87bd-117">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="c87bd-117">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c87bd-118">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="c87bd-118">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c87bd-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c87bd-119">Requirements</span></span>



| <span data-ttu-id="c87bd-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c87bd-120">Requirement</span></span> | <span data-ttu-id="c87bd-121">Valor</span><span class="sxs-lookup"><span data-stu-id="c87bd-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c87bd-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c87bd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c87bd-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c87bd-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c87bd-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c87bd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c87bd-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c87bd-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c87bd-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="c87bd-126">Namespace</span></span><br/>                | <span data-ttu-id="c87bd-127">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c87bd-127">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c87bd-128">MOF</span><span class="sxs-lookup"><span data-stu-id="c87bd-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c87bd-129"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c87bd-129"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c87bd-130">DLL</span><span class="sxs-lookup"><span data-stu-id="c87bd-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c87bd-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c87bd-131"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c87bd-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="c87bd-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c87bd-133">**\_DISKPARTITION CIM**</span><span class="sxs-lookup"><span data-stu-id="c87bd-133">**CIM\_DiskPartition**</span></span>](cim-diskpartition.md)
</dt> <dt>

[<span data-ttu-id="c87bd-134">**\_DiskPartition Win32**</span><span class="sxs-lookup"><span data-stu-id="c87bd-134">**Win32\_DiskPartition**</span></span>](win32-diskpartition.md)
</dt> </dl>

 

 




