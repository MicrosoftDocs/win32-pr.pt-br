---
description: Recupera o tamanho total dos arquivos do sistema da máquina virtual.
ms.assetid: 492aa0df-1562-4d83-a0ea-43776b12c1b1
title: Método GetSizeOfSystemFiles da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetSizeOfSystemFiles
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ed9fcf93093e17c2989121bf33ee5f5fbf09bab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647329"
---
# <a name="getsizeofsystemfiles-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="dc467-103">Método GetSizeOfSystemFiles da \_ classe VirtualSystemManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="dc467-103">GetSizeOfSystemFiles method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="dc467-104">Recupera o tamanho total dos arquivos do sistema da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dc467-104">Retrieves the total size of the system files of virtual machine.</span></span> <span data-ttu-id="dc467-105">Isso inclui os arquivos de configuração e de estado salvo.</span><span class="sxs-lookup"><span data-stu-id="dc467-105">These include the configuration and saved state files.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc467-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dc467-106">Syntax</span></span>


```mof
uint32 GetSizeOfSystemFiles(
  [in]  CIM_VirtualSystemSettingData REF Vssd,
  [out] uint64                           Size
);
```



## <a name="parameters"></a><span data-ttu-id="dc467-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dc467-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc467-108">*VSSD* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dc467-108">*Vssd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc467-109">Uma referência à instância do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) cujo tamanho dos arquivos do sistema deve ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="dc467-109">A reference to the [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) instance whose system files size are to be retrieved.</span></span> <span data-ttu-id="dc467-110">Essa instância pode representar a instanciação atual da máquina virtual ou uma instância de um instantâneo da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dc467-110">This instance may represent either the current instantiation of the virtual machine, or an instance of a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="dc467-111">*Tamanho* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="dc467-111">*Size* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc467-112">O tamanho total, em bytes, dos arquivos do sistema.</span><span class="sxs-lookup"><span data-stu-id="dc467-112">The total size, in bytes, of system files.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc467-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dc467-113">Return value</span></span>

<span data-ttu-id="dc467-114">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="dc467-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="dc467-115">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="dc467-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dc467-116">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="dc467-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="dc467-117">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="dc467-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="dc467-118">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="dc467-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="dc467-119">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="dc467-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="dc467-120">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="dc467-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="dc467-121">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="dc467-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="dc467-122">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="dc467-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="dc467-123">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="dc467-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="dc467-124">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="dc467-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="dc467-125">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="dc467-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="dc467-126">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="dc467-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="dc467-127">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="dc467-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="dc467-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc467-128">Requirements</span></span>



| <span data-ttu-id="dc467-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc467-129">Requirement</span></span> | <span data-ttu-id="dc467-130">Valor</span><span class="sxs-lookup"><span data-stu-id="dc467-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc467-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dc467-131">Minimum supported client</span></span><br/> | <span data-ttu-id="dc467-132">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="dc467-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="dc467-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dc467-133">Minimum supported server</span></span><br/> | <span data-ttu-id="dc467-134">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="dc467-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dc467-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="dc467-135">Namespace</span></span><br/>                | <span data-ttu-id="dc467-136">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="dc467-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="dc467-137">MOF</span><span class="sxs-lookup"><span data-stu-id="dc467-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dc467-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dc467-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dc467-139">DLL</span><span class="sxs-lookup"><span data-stu-id="dc467-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc467-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dc467-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dc467-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="dc467-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc467-142">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="dc467-142">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

