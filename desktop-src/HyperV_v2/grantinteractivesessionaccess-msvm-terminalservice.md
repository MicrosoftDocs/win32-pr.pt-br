---
description: Concede acesso à sessão interativa da máquina virtual à lista especificada de relações de confiança.
ms.assetid: 8a82170d-067b-47e5-a15f-21d6c04128d2
title: Método GrantInteractiveSessionAccess da classe Msvm_TerminalService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService.GrantInteractiveSessionAccess
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b8bd49805b5fdc5545a81e4f0b816fe35a6c37b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757817"
---
# <a name="grantinteractivesessionaccess-method-of-the-msvm_terminalservice-class"></a><span data-ttu-id="910df-103">Método GrantInteractiveSessionAccess da \_ classe TerminalService Msvm</span><span class="sxs-lookup"><span data-stu-id="910df-103">GrantInteractiveSessionAccess method of the Msvm\_TerminalService class</span></span>

<span data-ttu-id="910df-104">Concede acesso à sessão interativa da máquina virtual à lista especificada de relações de confiança.</span><span class="sxs-lookup"><span data-stu-id="910df-104">Grants access to the interactive session of the virtual machine to the specified list of trustees.</span></span>

## <a name="syntax"></a><span data-ttu-id="910df-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="910df-105">Syntax</span></span>


```mof
uint32 GrantInteractiveSessionAccess(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 Trustees[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="910df-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="910df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="910df-107">*ComputerSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="910df-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="910df-108">Uma referência a uma instância da classe [**Msvm \_ ComputerSystem**](msvm-computersystem.md) que representa a máquina virtual à qual o acesso será concedido.</span><span class="sxs-lookup"><span data-stu-id="910df-108">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine to which access will be granted.</span></span>

</dd> <dt>

<span data-ttu-id="910df-109">*Relações de confiança* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="910df-109">*Trustees* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="910df-110">Uma matriz de cadeias de caracteres, cada uma identificando um confiável que receberá acesso à sessão interativa da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="910df-110">An array of strings, each identifying a trustee that will be granted access to the interactive session of the virtual machine.</span></span> <span data-ttu-id="910df-111">Os identificadores de confiança devem ser especificados no formato compatível com o Windows SAM ou no formato de cadeia de caracteres SID do Windows.</span><span class="sxs-lookup"><span data-stu-id="910df-111">The trustee identifiers should be specified in Windows SAM-compatible format or Windows SID string format.</span></span>

</dd> <dt>

<span data-ttu-id="910df-112">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="910df-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="910df-113">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="910df-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="910df-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="910df-114">Return value</span></span>

<span data-ttu-id="910df-115">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="910df-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="910df-116">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="910df-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="910df-117">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="910df-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="910df-118">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="910df-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="910df-119">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="910df-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="910df-120">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="910df-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="910df-121">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="910df-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="910df-122">**Parâmetros incompatíveis** (6)</span><span class="sxs-lookup"><span data-stu-id="910df-122">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="910df-123">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="910df-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="910df-124">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="910df-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="910df-125">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="910df-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="910df-126">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="910df-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="910df-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="910df-127">Requirements</span></span>



| <span data-ttu-id="910df-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="910df-128">Requirement</span></span> | <span data-ttu-id="910df-129">Valor</span><span class="sxs-lookup"><span data-stu-id="910df-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="910df-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="910df-130">Minimum supported client</span></span><br/> | <span data-ttu-id="910df-131">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="910df-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="910df-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="910df-132">Minimum supported server</span></span><br/> | <span data-ttu-id="910df-133">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="910df-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="910df-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="910df-134">Namespace</span></span><br/>                | <span data-ttu-id="910df-135">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="910df-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="910df-136">MOF</span><span class="sxs-lookup"><span data-stu-id="910df-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="910df-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="910df-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="910df-138">DLL</span><span class="sxs-lookup"><span data-stu-id="910df-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="910df-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="910df-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="910df-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="910df-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="910df-141">**Msvm \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="910df-141">**Msvm\_TerminalService**</span></span>](msvm-terminalservice.md)
</dt> </dl>

 

