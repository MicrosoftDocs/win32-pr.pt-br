---
description: Modifica as configurações de segurança atuais de uma máquina virtual.
ms.assetid: b3eedab6-fd69-4c54-a8bf-4e3b77207687
title: Método ModifySecuritySettings da classe Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.ModifySecuritySettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4422f04be1833d66280392704630fcb670eba810
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756922"
---
# <a name="modifysecuritysettings-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="7e2db-103">Método ModifySecuritySettings da \_ classe SecurityService Msvm</span><span class="sxs-lookup"><span data-stu-id="7e2db-103">ModifySecuritySettings method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="7e2db-104">Modifica as configurações de segurança atuais de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7e2db-104">Modifies the current security settings of a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e2db-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7e2db-105">Syntax</span></span>


```mof
uint32 ModifySecuritySettings(
  [in]  string              SecuritySettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="7e2db-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7e2db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e2db-107">*SecuritySettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7e2db-107">*SecuritySettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e2db-108">Os novos dados de configuração de segurança.</span><span class="sxs-lookup"><span data-stu-id="7e2db-108">The new security setting data.</span></span>

</dd> <dt>

<span data-ttu-id="7e2db-109">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="7e2db-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7e2db-110">Um parâmetro opcional para monitorar o progresso da operação, que é usado se o método não pôde ser executado de forma síncrona.</span><span class="sxs-lookup"><span data-stu-id="7e2db-110">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="7e2db-111">Se a operação estiver sendo executada de forma assíncrona, o valor de retorno será 4096.</span><span class="sxs-lookup"><span data-stu-id="7e2db-111">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e2db-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7e2db-112">Return value</span></span>

<span data-ttu-id="7e2db-113">Em caso de sucesso, retorna um 0; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="7e2db-113">On success, returns a 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="7e2db-114">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="7e2db-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7e2db-115">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="7e2db-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7e2db-116">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="7e2db-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7e2db-117">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="7e2db-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7e2db-118">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="7e2db-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7e2db-119">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="7e2db-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="7e2db-120">**Parâmetros incompatíveis** (6)</span><span class="sxs-lookup"><span data-stu-id="7e2db-120">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="7e2db-121">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="7e2db-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7e2db-122">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="7e2db-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="7e2db-123">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="7e2db-123">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="7e2db-124">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="7e2db-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="7e2db-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e2db-125">Requirements</span></span>



| <span data-ttu-id="7e2db-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e2db-126">Requirement</span></span> | <span data-ttu-id="7e2db-127">Valor</span><span class="sxs-lookup"><span data-stu-id="7e2db-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e2db-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7e2db-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7e2db-129">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="7e2db-129">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7e2db-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7e2db-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7e2db-131">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="7e2db-131">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="7e2db-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="7e2db-132">Namespace</span></span><br/>                | <span data-ttu-id="7e2db-133">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="7e2db-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7e2db-134">MOF</span><span class="sxs-lookup"><span data-stu-id="7e2db-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7e2db-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7e2db-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7e2db-136">DLL</span><span class="sxs-lookup"><span data-stu-id="7e2db-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e2db-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7e2db-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7e2db-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="7e2db-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e2db-139">**Msvm \_ SecurityService**</span><span class="sxs-lookup"><span data-stu-id="7e2db-139">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




