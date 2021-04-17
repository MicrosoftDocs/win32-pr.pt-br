---
description: Adiciona uma entrada de autorização a um servidor de recuperação.
ms.assetid: edc11c5b-b1a1-45e0-a920-2f1f1b0b8779
title: Método AddAuthorizationEntry da classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.AddAuthorizationEntry
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fd4c47bd4468d5804ec7e096d35db271726c92b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105775746"
---
# <a name="addauthorizationentry-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="72513-103">Método AddAuthorizationEntry da \_ classe ReplicationService Msvm</span><span class="sxs-lookup"><span data-stu-id="72513-103">AddAuthorizationEntry method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="72513-104">Adiciona uma entrada de autorização a um servidor de recuperação.</span><span class="sxs-lookup"><span data-stu-id="72513-104">Adds an authorization entry to a recovery server.</span></span> <span data-ttu-id="72513-105">Essas entradas são usadas para autorizar conexões com o servidor de recuperação.</span><span class="sxs-lookup"><span data-stu-id="72513-105">These entries are used for authorizing connections to the recovery server.</span></span>

## <a name="syntax"></a><span data-ttu-id="72513-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="72513-106">Syntax</span></span>


```mof
uint32 AddAuthorizationEntry(
  [in]  string              AuthorizationEntry,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="72513-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="72513-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72513-108">*AuthorizationEntry* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="72513-108">*AuthorizationEntry* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72513-109">Uma representação de cadeia de caracteres de uma instância da classe [**Msvm \_ ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md) que define a entrada de autorização a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="72513-109">A string representation of an instance of the [**Msvm\_ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md) class that defines the authorization entry to be added.</span></span>

</dd> <dt>

<span data-ttu-id="72513-110">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="72513-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="72513-111">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="72513-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72513-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="72513-112">Return value</span></span>

<span data-ttu-id="72513-113">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="72513-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="72513-114">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="72513-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="72513-115">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="72513-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="72513-116">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="72513-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="72513-117">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="72513-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="72513-118">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="72513-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="72513-119">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="72513-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="72513-120">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="72513-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="72513-121">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="72513-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="72513-122">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="72513-122">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="72513-123">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="72513-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="72513-124">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="72513-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="72513-125">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="72513-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="72513-126">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="72513-126">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="72513-127">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="72513-127">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="72513-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72513-128">Requirements</span></span>



| <span data-ttu-id="72513-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="72513-129">Requirement</span></span> | <span data-ttu-id="72513-130">Valor</span><span class="sxs-lookup"><span data-stu-id="72513-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72513-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72513-131">Minimum supported client</span></span><br/> | <span data-ttu-id="72513-132">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="72513-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="72513-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72513-133">Minimum supported server</span></span><br/> | <span data-ttu-id="72513-134">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="72513-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="72513-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="72513-135">Namespace</span></span><br/>                | <span data-ttu-id="72513-136">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="72513-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="72513-137">MOF</span><span class="sxs-lookup"><span data-stu-id="72513-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72513-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="72513-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="72513-139">DLL</span><span class="sxs-lookup"><span data-stu-id="72513-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72513-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="72513-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="72513-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="72513-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72513-142">**ModifyAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="72513-142">**ModifyAuthorizationEntry**</span></span>](modifyauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="72513-143">**RemoveAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="72513-143">**RemoveAuthorizationEntry**</span></span>](removeauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="72513-144">**SetAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="72513-144">**SetAuthorizationEntry**</span></span>](setauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="72513-145">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="72513-145">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

