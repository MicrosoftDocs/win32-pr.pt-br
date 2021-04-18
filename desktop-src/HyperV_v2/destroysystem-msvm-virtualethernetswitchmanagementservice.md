---
description: Destrói um comutador virtual.
ms.assetid: f0b6b4cc-e9b7-4255-a9e1-a2a826b8f119
title: Método DestroySystem da classe Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.DestroySystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d8f01a3f72d15fba908c7891f76b4128a1ee8200
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105767647"
---
# <a name="destroysystem-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="a43a1-103">Método DestroySystem da \_ classe VirtualEthernetSwitchManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="a43a1-103">DestroySystem method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="a43a1-104">Destrói um comutador virtual.</span><span class="sxs-lookup"><span data-stu-id="a43a1-104">Destroys a virtual switch.</span></span>

## <a name="syntax"></a><span data-ttu-id="a43a1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a43a1-105">Syntax</span></span>


```mof
uint32 DestroySystem(
  [in]  CIM_ComputerSystem REF AffectedSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="a43a1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a43a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a43a1-107">*AffectedSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a43a1-107">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a43a1-108">Uma referência a uma instância da classe [**Msvm \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) que representa o comutador virtual que deve ser destruído.</span><span class="sxs-lookup"><span data-stu-id="a43a1-108">A reference to an instance of the [**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) class that represents the virtual switch that is to be destroyed.</span></span>

</dd> <dt>

<span data-ttu-id="a43a1-109">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="a43a1-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a43a1-110">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a43a1-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a43a1-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a43a1-111">Return value</span></span>

<span data-ttu-id="a43a1-112">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="a43a1-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="a43a1-113">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="a43a1-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a43a1-114">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="a43a1-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a43a1-115">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="a43a1-115">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a43a1-116">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="a43a1-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a43a1-117">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="a43a1-117">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a43a1-118">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="a43a1-118">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a43a1-119">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="a43a1-119">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a43a1-120">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="a43a1-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a43a1-121">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="a43a1-121">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="a43a1-122">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="a43a1-122">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="a43a1-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a43a1-123">Requirements</span></span>



| <span data-ttu-id="a43a1-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a43a1-124">Requirement</span></span> | <span data-ttu-id="a43a1-125">Valor</span><span class="sxs-lookup"><span data-stu-id="a43a1-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a43a1-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a43a1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a43a1-127">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a43a1-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a43a1-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a43a1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a43a1-129">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a43a1-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a43a1-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="a43a1-130">Namespace</span></span><br/>                | <span data-ttu-id="a43a1-131">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="a43a1-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a43a1-132">MOF</span><span class="sxs-lookup"><span data-stu-id="a43a1-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a43a1-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a43a1-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a43a1-134">DLL</span><span class="sxs-lookup"><span data-stu-id="a43a1-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a43a1-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a43a1-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a43a1-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="a43a1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a43a1-137">**Msvm \_ VirtualEthernetSwitchManagementService**</span><span class="sxs-lookup"><span data-stu-id="a43a1-137">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

