---
description: Modifica uma entrada de autorização para um servidor de recuperação.
ms.assetid: fbdf3ecd-42de-49a8-85b8-51fc9c9fcf26
title: Método ModifyAuthorizationEntry da classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ModifyAuthorizationEntry
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 17f5ff1a0e4e1cca95dc5f7764d2f8e2bf9d2c73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782815"
---
# <a name="modifyauthorizationentry-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="41f4e-103">Método ModifyAuthorizationEntry da \_ classe ReplicationService Msvm</span><span class="sxs-lookup"><span data-stu-id="41f4e-103">ModifyAuthorizationEntry method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="41f4e-104">Modifica uma entrada de autorização para um servidor de recuperação.</span><span class="sxs-lookup"><span data-stu-id="41f4e-104">Modifies an authorization entry for a recovery server.</span></span>

## <a name="syntax"></a><span data-ttu-id="41f4e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="41f4e-105">Syntax</span></span>


```mof
uint32 ModifyAuthorizationEntry(
  [in]  string              AuthorizationEntry,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="41f4e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="41f4e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41f4e-107">*AuthorizationEntry* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="41f4e-107">*AuthorizationEntry* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41f4e-108">Uma representação de cadeia de caracteres de uma instância da classe [**Msvm \_ ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md) que define a entrada de autorização a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="41f4e-108">A string representation of an instance of the [**Msvm\_ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md) class that defines the authorization entry to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="41f4e-109">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="41f4e-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41f4e-110">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="41f4e-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41f4e-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="41f4e-111">Return value</span></span>

<span data-ttu-id="41f4e-112">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="41f4e-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="41f4e-113">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="41f4e-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="41f4e-114">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="41f4e-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="41f4e-115">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="41f4e-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="41f4e-116">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="41f4e-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="41f4e-117">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="41f4e-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="41f4e-118">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="41f4e-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="41f4e-119">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="41f4e-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="41f4e-120">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="41f4e-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="41f4e-121">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="41f4e-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="41f4e-122">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="41f4e-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="41f4e-123">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="41f4e-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="41f4e-124">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="41f4e-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="41f4e-125">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="41f4e-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="41f4e-126">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="41f4e-126">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="41f4e-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41f4e-127">Requirements</span></span>



| <span data-ttu-id="41f4e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="41f4e-128">Requirement</span></span> | <span data-ttu-id="41f4e-129">Valor</span><span class="sxs-lookup"><span data-stu-id="41f4e-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41f4e-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41f4e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="41f4e-131">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="41f4e-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="41f4e-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41f4e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="41f4e-133">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="41f4e-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="41f4e-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="41f4e-134">Namespace</span></span><br/>                | <span data-ttu-id="41f4e-135">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="41f4e-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="41f4e-136">MOF</span><span class="sxs-lookup"><span data-stu-id="41f4e-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="41f4e-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="41f4e-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="41f4e-138">DLL</span><span class="sxs-lookup"><span data-stu-id="41f4e-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41f4e-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="41f4e-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="41f4e-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="41f4e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41f4e-141">**AddAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="41f4e-141">**AddAuthorizationEntry**</span></span>](addauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="41f4e-142">**RemoveAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="41f4e-142">**RemoveAuthorizationEntry**</span></span>](removeauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="41f4e-143">**SetAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="41f4e-143">**SetAuthorizationEntry**</span></span>](setauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="41f4e-144">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="41f4e-144">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

