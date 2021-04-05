---
description: Verifica a compatibilidade das informações de compatibilidade com o sistema de computador de hospedagem.
ms.assetid: 1991c58e-2d0b-4fc3-a04a-c18f358451f6
title: Método CheckSystemCompatibilityInfo da classe Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.CheckSystemCompatibilityInfo
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e47b72c6cac6e8a6061b4560b77b82cb0b845a8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826870"
---
# <a name="checksystemcompatibilityinfo-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="95f6d-103">Método CheckSystemCompatibilityInfo da \_ classe VirtualSystemMigrationService Msvm</span><span class="sxs-lookup"><span data-stu-id="95f6d-103">CheckSystemCompatibilityInfo method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="95f6d-104">Verifica a compatibilidade das informações de compatibilidade com o sistema de computador de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="95f6d-104">Checks the compatibility information for compatibility with the hosting computer system.</span></span>

## <a name="syntax"></a><span data-ttu-id="95f6d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="95f6d-105">Syntax</span></span>


```mof
uint32 CheckSystemCompatibilityInfo(
  [in]  uint8  CompatibilityInfo[],
  [out] string Reasons[]
);
```



## <a name="parameters"></a><span data-ttu-id="95f6d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="95f6d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95f6d-107">*CompatibilityInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="95f6d-107">*CompatibilityInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95f6d-108">Um blob de dados obtidos chamando o método [**GetSystemCompatibilityInfo**](getsystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) no sistema de computador de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="95f6d-108">A blob of data obtained by calling the [**GetSystemCompatibilityInfo**](getsystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) method on the hosting computer system.</span></span>

</dd> <dt>

<span data-ttu-id="95f6d-109">*Motivos* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="95f6d-109">*Reasons* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95f6d-110">Uma matriz de cadeias de caracteres que recebe as instâncias inseridas da classe de [**\_ erro Msvm**](msvm-error.md) que representam avisos ou erros.</span><span class="sxs-lookup"><span data-stu-id="95f6d-110">An array of strings that receives the embedded instances of the [**Msvm\_Error**](msvm-error.md) class that represent any warnings or errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95f6d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="95f6d-111">Return value</span></span>

<span data-ttu-id="95f6d-112">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="95f6d-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="95f6d-113">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="95f6d-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="95f6d-114">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="95f6d-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="95f6d-115">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="95f6d-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="95f6d-116">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="95f6d-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="95f6d-117">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="95f6d-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="95f6d-118">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="95f6d-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="95f6d-119">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="95f6d-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="95f6d-120">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="95f6d-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="95f6d-121">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="95f6d-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="95f6d-122">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="95f6d-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="95f6d-123">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="95f6d-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="95f6d-124">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="95f6d-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="95f6d-125">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="95f6d-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="95f6d-126">**Não compatível** (32784)</span><span class="sxs-lookup"><span data-stu-id="95f6d-126">**Not compatible** (32784)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="95f6d-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95f6d-127">Requirements</span></span>



| <span data-ttu-id="95f6d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="95f6d-128">Requirement</span></span> | <span data-ttu-id="95f6d-129">Valor</span><span class="sxs-lookup"><span data-stu-id="95f6d-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95f6d-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95f6d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="95f6d-131">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="95f6d-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="95f6d-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95f6d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="95f6d-133">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="95f6d-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="95f6d-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="95f6d-134">Namespace</span></span><br/>                | <span data-ttu-id="95f6d-135">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="95f6d-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="95f6d-136">MOF</span><span class="sxs-lookup"><span data-stu-id="95f6d-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="95f6d-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="95f6d-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="95f6d-138">DLL</span><span class="sxs-lookup"><span data-stu-id="95f6d-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95f6d-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="95f6d-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="95f6d-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="95f6d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95f6d-141">**Msvm \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="95f6d-141">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




