---
description: Restaura novamente para o último protetor de chave válido conhecido.
ms.assetid: 0d1ea5d8-d25e-400c-be65-afe1bd65b1f0
title: Método RestoreLastKnownGoodKeyProtector da classe Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.RestoreLastKnownGoodKeyProtector
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2e82fb3b40f4b85e74f92ed2690a411932af2eb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759402"
---
# <a name="restorelastknowngoodkeyprotector-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="08645-103">Método RestoreLastKnownGoodKeyProtector da \_ classe SecurityService Msvm</span><span class="sxs-lookup"><span data-stu-id="08645-103">RestoreLastKnownGoodKeyProtector method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="08645-104">Restaura novamente para o último protetor de chave válido conhecido.</span><span class="sxs-lookup"><span data-stu-id="08645-104">Restores back to the last known good key protector.</span></span>

## <a name="syntax"></a><span data-ttu-id="08645-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="08645-105">Syntax</span></span>


```mof
uint32 RestoreLastKnownGoodKeyProtector(
  [in]  string              SecuritySettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="08645-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="08645-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08645-107">*SecuritySettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="08645-107">*SecuritySettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08645-108">A cadeia de caracteres contém uma instância inserida da classe [**Msvm \_ SecuritySettingData**](msvm-securitysettingdata.md) que representa as configurações de segurança de um sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="08645-108">String contains an embedded instance of the [**Msvm\_SecuritySettingData**](msvm-securitysettingdata.md) class representing the security settings of a virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="08645-109">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="08645-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="08645-110">Um parâmetro opcional para monitorar o progresso da operação, que é usado se o método não pôde ser executado de forma síncrona.</span><span class="sxs-lookup"><span data-stu-id="08645-110">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="08645-111">Se a operação estiver sendo executada de forma assíncrona, o valor de retorno será 4096.</span><span class="sxs-lookup"><span data-stu-id="08645-111">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08645-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="08645-112">Return value</span></span>

<span data-ttu-id="08645-113">Em caso de sucesso, retorna 0 ou 4096; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="08645-113">On success, returns a 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="08645-114">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="08645-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="08645-115">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="08645-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="08645-116">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="08645-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="08645-117">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="08645-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="08645-118">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="08645-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="08645-119">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="08645-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="08645-120">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="08645-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="08645-121">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="08645-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="08645-122">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="08645-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="08645-123">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="08645-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="08645-124">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="08645-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="08645-125">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="08645-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="08645-126">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="08645-126">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="08645-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08645-127">Requirements</span></span>



| <span data-ttu-id="08645-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="08645-128">Requirement</span></span> | <span data-ttu-id="08645-129">Valor</span><span class="sxs-lookup"><span data-stu-id="08645-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08645-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="08645-130">Minimum supported client</span></span><br/> | <span data-ttu-id="08645-131">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="08645-131">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="08645-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="08645-132">Minimum supported server</span></span><br/> | <span data-ttu-id="08645-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="08645-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="08645-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="08645-134">Namespace</span></span><br/>                | <span data-ttu-id="08645-135">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="08645-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="08645-136">MOF</span><span class="sxs-lookup"><span data-stu-id="08645-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="08645-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="08645-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="08645-138">DLL</span><span class="sxs-lookup"><span data-stu-id="08645-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08645-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="08645-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="08645-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="08645-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08645-141">**Msvm \_ SecurityService**</span><span class="sxs-lookup"><span data-stu-id="08645-141">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




