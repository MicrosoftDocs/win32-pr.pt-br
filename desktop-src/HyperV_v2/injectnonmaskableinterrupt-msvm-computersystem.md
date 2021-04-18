---
description: Injeta uma interrupção não mascarável na máquina virtual.
ms.assetid: 897AD1B9-0EDD-4DCE-963D-D5DE03AF55A9
title: 'Método Msvm_ComputerSystem:: InjectNonMaskableInterrupt'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem.InjectNonMaskableInterrupt
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5798079a8866d9fb67356adff43c0ac1e993e6fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778755"
---
# <a name="msvm_computersysteminjectnonmaskableinterrupt-method"></a><span data-ttu-id="58312-103">\_Método Msvm ComputerSystem:: InjectNonMaskableInterrupt</span><span class="sxs-lookup"><span data-stu-id="58312-103">Msvm\_ComputerSystem::InjectNonMaskableInterrupt method</span></span>

<span data-ttu-id="58312-104">Injeta uma interrupção não mascarável na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="58312-104">Injects a non-maskable interrupt into the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="58312-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="58312-105">Syntax</span></span>


```C++
uint32 InjectNonMaskableInterrupt(
  [out] CIM_ConcreteJob Job
);
```



## <a name="parameters"></a><span data-ttu-id="58312-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="58312-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58312-107">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="58312-107">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="58312-108">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)) para acompanhar o status da injeção de interrupção.</span><span class="sxs-lookup"><span data-stu-id="58312-108">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)) to track the status of the interrupt injection.</span></span> <span data-ttu-id="58312-109">Essa referência poderá ser **nula** se a tarefa for concluída.</span><span class="sxs-lookup"><span data-stu-id="58312-109">This reference can be **NULL** if the task is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58312-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="58312-110">Return value</span></span>

<span data-ttu-id="58312-111">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="58312-111">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="58312-112">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="58312-112">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="58312-113">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="58312-113">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="58312-114">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="58312-114">**Access Denied** (32769)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="58312-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58312-115">Requirements</span></span>



| <span data-ttu-id="58312-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="58312-116">Requirement</span></span> | <span data-ttu-id="58312-117">Valor</span><span class="sxs-lookup"><span data-stu-id="58312-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58312-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58312-118">Minimum supported client</span></span><br/> | <span data-ttu-id="58312-119">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="58312-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="58312-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58312-120">Minimum supported server</span></span><br/> | <span data-ttu-id="58312-121">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="58312-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="58312-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="58312-122">Namespace</span></span><br/>                | <span data-ttu-id="58312-123">\\\\\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="58312-123">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="58312-124">MOF</span><span class="sxs-lookup"><span data-stu-id="58312-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="58312-125"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="58312-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="58312-126">DLL</span><span class="sxs-lookup"><span data-stu-id="58312-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58312-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="58312-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="58312-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="58312-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58312-129">**Msvm \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="58312-129">**Msvm\_ComputerSystem**</span></span>](msvm-computersystem.md)
</dt> </dl>

 

