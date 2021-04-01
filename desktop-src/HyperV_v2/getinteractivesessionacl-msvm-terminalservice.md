---
description: Recupera a lista de controle de acesso discricional (DACL) atual que controla o acesso à sessão interativa de uma máquina virtual.
ms.assetid: 9b81f6d5-20fa-4277-b943-756d85359fd2
title: Método GetInteractiveSessionACL da classe Msvm_TerminalService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService.GetInteractiveSessionACL
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f08c8514a2f65a08b4b9350b38988da8e49b4985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647333"
---
# <a name="getinteractivesessionacl-method-of-the-msvm_terminalservice-class"></a><span data-ttu-id="8c85f-103">Método GetInteractiveSessionACL da \_ classe TerminalService Msvm</span><span class="sxs-lookup"><span data-stu-id="8c85f-103">GetInteractiveSessionACL method of the Msvm\_TerminalService class</span></span>

<span data-ttu-id="8c85f-104">Recupera a *lista de controle de acesso discricional* (DACL) atual que controla o acesso à sessão interativa de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8c85f-104">Retrieves the current *discretionary access control list* (DACL) that controls access to the interactive session of a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c85f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8c85f-105">Syntax</span></span>


```mof
uint32 GetInteractiveSessionACL(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] string                 AccessControlList[]
);
```



## <a name="parameters"></a><span data-ttu-id="8c85f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8c85f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c85f-107">*ComputerSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8c85f-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c85f-108">Uma referência a uma instância da classe [**Msvm \_ ComputerSystem**](msvm-computersystem.md) que representa a máquina virtual cuja DACL será recuperada.</span><span class="sxs-lookup"><span data-stu-id="8c85f-108">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine whose DACL will be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="8c85f-109">*AccessControlList* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8c85f-109">*AccessControlList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c85f-110">Uma matriz de cadeias de caracteres, cada uma contendo uma instância inserida da classe [**Msvm \_ InteractiveSessionACE**](msvm-interactivesessionace.md) que representa uma ACE ( *entrada de controle de acesso* ) na DACL da sessão interativa da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8c85f-110">An array of strings, each containing an embedded instance of the [**Msvm\_InteractiveSessionACE**](msvm-interactivesessionace.md) class that represents an *access control entry* (ACE) in the virtual machine interactive session DACL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c85f-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8c85f-111">Return value</span></span>

<span data-ttu-id="8c85f-112">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="8c85f-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="8c85f-113">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="8c85f-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8c85f-114">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="8c85f-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8c85f-115">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="8c85f-115">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8c85f-116">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="8c85f-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8c85f-117">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="8c85f-117">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8c85f-118">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="8c85f-118">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="8c85f-119">**Parâmetros incompatíveis** (6)</span><span class="sxs-lookup"><span data-stu-id="8c85f-119">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="8c85f-120">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="8c85f-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8c85f-121">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="8c85f-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="8c85f-122">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="8c85f-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="8c85f-123">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="8c85f-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="8c85f-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c85f-124">Requirements</span></span>



| <span data-ttu-id="8c85f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c85f-125">Requirement</span></span> | <span data-ttu-id="8c85f-126">Valor</span><span class="sxs-lookup"><span data-stu-id="8c85f-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c85f-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8c85f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8c85f-128">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8c85f-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8c85f-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8c85f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8c85f-130">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8c85f-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8c85f-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="8c85f-131">Namespace</span></span><br/>                | <span data-ttu-id="8c85f-132">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="8c85f-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8c85f-133">MOF</span><span class="sxs-lookup"><span data-stu-id="8c85f-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8c85f-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8c85f-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8c85f-135">DLL</span><span class="sxs-lookup"><span data-stu-id="8c85f-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c85f-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8c85f-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8c85f-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="8c85f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c85f-138">**Msvm \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="8c85f-138">**Msvm\_TerminalService**</span></span>](msvm-terminalservice.md)
</dt> </dl>

 

 




