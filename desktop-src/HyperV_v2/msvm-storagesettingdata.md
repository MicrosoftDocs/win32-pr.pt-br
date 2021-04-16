---
description: Representa as configurações específicas de armazenamento para um sistema virtual.
ms.assetid: 0b3fcd78-7e9a-4a94-ad18-0ca72b3cfd73
title: Classe Msvm_StorageSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageSettingData
- Msvm_StorageSettingData.VirtualProcessorsPerChannel
- Msvm_StorageSettingData.DisableInterruptBatching
- Msvm_StorageSettingData.ThreadCountPerChannel
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: db061d048ce45a4d6fa076a5b0367e794cdf16e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750269"
---
# <a name="msvm_storagesettingdata-class"></a><span data-ttu-id="d01ac-103">\_Classe Msvm StorageSettingData</span><span class="sxs-lookup"><span data-stu-id="d01ac-103">Msvm\_StorageSettingData class</span></span>

<span data-ttu-id="d01ac-104">Representa as configurações específicas de armazenamento para um sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="d01ac-104">Represents the storage-specific settings for a virtual system.</span></span>

<span data-ttu-id="d01ac-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d01ac-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d01ac-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d01ac-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_StorageSettingData : Msvm_SystemComponentSettingData
{
  uint16  VirtualProcessorsPerChannel;
  boolean DisableInterruptBatching;
  uint16  ThreadCountPerChannel;
};
```

## <a name="members"></a><span data-ttu-id="d01ac-107">Membros</span><span class="sxs-lookup"><span data-stu-id="d01ac-107">Members</span></span>

<span data-ttu-id="d01ac-108">A classe **Msvm \_ StorageSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d01ac-108">The **Msvm\_StorageSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="d01ac-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d01ac-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d01ac-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d01ac-110">Properties</span></span>

<span data-ttu-id="d01ac-111">A classe **Msvm \_ StorageSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d01ac-111">The **Msvm\_StorageSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d01ac-112">**DisableInterruptBatching**</span><span class="sxs-lookup"><span data-stu-id="d01ac-112">**DisableInterruptBatching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d01ac-113">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="d01ac-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d01ac-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d01ac-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d01ac-115">Especifica se o envio em lote de interrupção deve ser desabilitado.</span><span class="sxs-lookup"><span data-stu-id="d01ac-115">Specifies whether interrupt batching should be disabled.</span></span>

<span data-ttu-id="d01ac-116">Esta é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) da classe WMI [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="d01ac-116">This is a read-only property, but it can be changed using the [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) method of the Wmi [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="d01ac-117">**ThreadCountPerChannel**</span><span class="sxs-lookup"><span data-stu-id="d01ac-117">**ThreadCountPerChannel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d01ac-118">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d01ac-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d01ac-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d01ac-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d01ac-120">O número de threads por canal de armazenamento para processar e/s.</span><span class="sxs-lookup"><span data-stu-id="d01ac-120">The number of threads per storage channel to process IO.</span></span>

<span data-ttu-id="d01ac-121">Esta é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="d01ac-121">This is a read-only property, but it can be changed using the [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="d01ac-122"><span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>**Padrão** (0)</span><span class="sxs-lookup"><span data-stu-id="d01ac-122"><span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>**Default** (0)</span></span>


</dt> <dd>

<span data-ttu-id="d01ac-123">Comportamento padrão</span><span class="sxs-lookup"><span data-stu-id="d01ac-123">Default behavior</span></span>

</dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="d01ac-124"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Baixo** (1)</span><span class="sxs-lookup"><span data-stu-id="d01ac-124"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Low** (1)</span></span>


</dt> <dd>

<span data-ttu-id="d01ac-125">Número baixo de threads por canal de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d01ac-125">Low number of threads per storage channel.</span></span>

</dd> <dt>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>

<span data-ttu-id="d01ac-126"><span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>**Médio** (2)</span><span class="sxs-lookup"><span data-stu-id="d01ac-126"><span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>**Medium** (2)</span></span>


</dt> <dd>

<span data-ttu-id="d01ac-127">Número médio de threads por canal de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d01ac-127">Medium number of threads per storage channel.</span></span>

</dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="d01ac-128"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**Alta** (3)</span><span class="sxs-lookup"><span data-stu-id="d01ac-128"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**High** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d01ac-129">Número alto de threads por canal de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d01ac-129">High number of threads per storage channel.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d01ac-130">**VirtualProcessorsPerChannel**</span><span class="sxs-lookup"><span data-stu-id="d01ac-130">**VirtualProcessorsPerChannel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d01ac-131">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d01ac-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d01ac-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d01ac-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d01ac-133">O número de processadores por canal de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d01ac-133">The number of processors per storage channel.</span></span> <span data-ttu-id="d01ac-134">O número de canais a serem abertos é fornecido por (contagem de processadores lógicos no host/**VirtualProcessorsPerChannel**).</span><span class="sxs-lookup"><span data-stu-id="d01ac-134">The number of channels to be opened is given by (Count of logical processors on the host /**VirtualProcessorsPerChannel**).</span></span>

<span data-ttu-id="d01ac-135">Esta é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="d01ac-135">This is a read-only property, but it can be changed using the [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d01ac-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d01ac-136">Requirements</span></span>



| <span data-ttu-id="d01ac-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="d01ac-137">Requirement</span></span> | <span data-ttu-id="d01ac-138">Valor</span><span class="sxs-lookup"><span data-stu-id="d01ac-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d01ac-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d01ac-139">Minimum supported client</span></span><br/> | <span data-ttu-id="d01ac-140">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="d01ac-140">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d01ac-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d01ac-141">Minimum supported server</span></span><br/> | <span data-ttu-id="d01ac-142">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d01ac-142">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="d01ac-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="d01ac-143">Namespace</span></span><br/>                | <span data-ttu-id="d01ac-144">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="d01ac-144">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d01ac-145">MOF</span><span class="sxs-lookup"><span data-stu-id="d01ac-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d01ac-146"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d01ac-146"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d01ac-147">DLL</span><span class="sxs-lookup"><span data-stu-id="d01ac-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d01ac-148"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d01ac-148"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d01ac-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="d01ac-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d01ac-150">**Msvm \_ SystemComponentSettingData**</span><span class="sxs-lookup"><span data-stu-id="d01ac-150">**Msvm\_SystemComponentSettingData**</span></span>](msvm-systemcomponentsettingdata.md)
</dt> </dl>

 

 




