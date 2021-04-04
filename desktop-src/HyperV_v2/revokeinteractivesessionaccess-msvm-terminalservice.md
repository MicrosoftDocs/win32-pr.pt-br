---
description: Revoga o acesso à sessão interativa da máquina virtual da lista especificada de relações de confiança.
ms.assetid: c6d3df04-c31e-404a-9a04-3e8653bdc14f
title: Método RevokeInteractiveSessionAccess da classe Msvm_TerminalService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService.RevokeInteractiveSessionAccess
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ab92f375f082d3af1f04b3fe52db5cb7964e3d4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662155"
---
# <a name="revokeinteractivesessionaccess-method-of-the-msvm_terminalservice-class"></a><span data-ttu-id="98f21-103">Método RevokeInteractiveSessionAccess da \_ classe TerminalService Msvm</span><span class="sxs-lookup"><span data-stu-id="98f21-103">RevokeInteractiveSessionAccess method of the Msvm\_TerminalService class</span></span>

<span data-ttu-id="98f21-104">Revoga o acesso à sessão interativa da máquina virtual da lista especificada de relações de confiança.</span><span class="sxs-lookup"><span data-stu-id="98f21-104">Revokes access to the interactive session of the virtual machine from the specified list of trustees.</span></span>

## <a name="syntax"></a><span data-ttu-id="98f21-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="98f21-105">Syntax</span></span>


```mof
uint32 RevokeInteractiveSessionAccess(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 Trustees[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="98f21-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="98f21-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98f21-107">*ComputerSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="98f21-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98f21-108">Uma referência a uma instância da classe [**de \_ sistema**](cim-computersystem.md) de computador CIM que representa a máquina virtual para a qual o acesso será revogado.</span><span class="sxs-lookup"><span data-stu-id="98f21-108">A reference to an instance of the [**CIM\_ComputerSystem**](cim-computersystem.md) class that represents the virtual machine to which access will be revoked.</span></span>

</dd> <dt>

<span data-ttu-id="98f21-109">*Relações de confiança* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="98f21-109">*Trustees* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98f21-110">Uma matriz de cadeias de caracteres, cada uma identificando um confiável cujos direitos de acesso serão revogados.</span><span class="sxs-lookup"><span data-stu-id="98f21-110">An array of strings, each identifying a trustee whose access rights will be revoked.</span></span> <span data-ttu-id="98f21-111">Os identificadores de confiança devem ser especificados no formato compatível com o Windows SAM ou no formato de cadeia de caracteres SID do Windows.</span><span class="sxs-lookup"><span data-stu-id="98f21-111">The trustee identifiers should be specified in Windows SAM-compatible format or Windows SID string format.</span></span>

</dd> <dt>

<span data-ttu-id="98f21-112">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="98f21-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="98f21-113">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="98f21-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98f21-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="98f21-114">Return value</span></span>

<span data-ttu-id="98f21-115">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="98f21-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="98f21-116">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="98f21-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="98f21-117">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="98f21-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="98f21-118">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="98f21-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="98f21-119">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="98f21-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="98f21-120">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="98f21-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="98f21-121">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="98f21-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="98f21-122">**Parâmetros incompatíveis** (6)</span><span class="sxs-lookup"><span data-stu-id="98f21-122">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="98f21-123">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="98f21-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="98f21-124">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="98f21-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="98f21-125">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="98f21-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="98f21-126">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="98f21-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="98f21-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98f21-127">Requirements</span></span>



| <span data-ttu-id="98f21-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="98f21-128">Requirement</span></span> | <span data-ttu-id="98f21-129">Valor</span><span class="sxs-lookup"><span data-stu-id="98f21-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98f21-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="98f21-130">Minimum supported client</span></span><br/> | <span data-ttu-id="98f21-131">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="98f21-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="98f21-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="98f21-132">Minimum supported server</span></span><br/> | <span data-ttu-id="98f21-133">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="98f21-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="98f21-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="98f21-134">Namespace</span></span><br/>                | <span data-ttu-id="98f21-135">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="98f21-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="98f21-136">MOF</span><span class="sxs-lookup"><span data-stu-id="98f21-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="98f21-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="98f21-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="98f21-138">DLL</span><span class="sxs-lookup"><span data-stu-id="98f21-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98f21-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="98f21-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="98f21-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="98f21-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98f21-141">**Msvm \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="98f21-141">**Msvm\_TerminalService**</span></span>](msvm-terminalservice.md)
</dt> </dl>

 

